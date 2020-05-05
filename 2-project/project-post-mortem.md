## Project Post Mortem
Post mortems are important to understand about what happened in a project and actively think about what you learned.

Post-mortems are meant to be a blame-less space open to objective conversation about what went well and what could be improved.

Even in the examples below, where tens of millions of dollars could be lost, the best approach is to think through the series of events that led to the outcome.

Large mistakes are almost never the fault of the developer, but of the sytems and processes in place to prevent errors and problems.

[https://github.com/danluu/post-mortems](https://github.com/danluu/post-mortems)
https://blog.codinghorror.com/the-project-postmortem/



### What to Bring
Please answer the following questions. Take at least 30 minutes to prepare.

#### Approach and Process

1. What in my process and approach to this project would I do differently next time?

1. What in my process and approach to this project went well that I would repeat next time?

--

#### Code and Code Design

1. What in my code and program design in the project would I do differently next time?

  I would use the components part for the react views.

1. What in my code and program design in the project went well? Is there anything I would do the same next time?

  For each, please include code examples.
  1. Code snippet up to 20 lines.
  2. Code design documents or architecture drawings / diagrams.

 //FIRST PART
 let values = request;
 let query = 'select *,profile.name AS username FROM user_match inner join profile ON(profile.id = user1_id) inner join                     game ON(game_id = game.id) where user1_id IN(select user2_id from user_match where user1_id = $1) and                         user2_id = $1'
      
  1. Sql checking matches is working as intended, this part can be used in the future for similar project.

  //SECOND PART
  let index = (request, response) => {
        console.log(request.body)
        let username = request.cookies['username']
        let profileid = request.cookies['profileid']
        response.cookie('profileid',request.params.id)
        let loggedIn = false
        if( request.cookies['logged in'] === 'true'){
            loggedIn = true;
        }
        let values = [request.params.id, request.params.gameid]
    }
    
    2. I will try to include more data in sql, and query the data out, instead of storing them in cookies.

#### WDI Unit 2 Post Mortem
1. What habits did I use during this unit that helped me?
   I does more commit than usual, better at using sql database, spent more time styling my webpage.
  
2. What habits did I have during this unit that I can improve on?
   I rely on cookies too much, better store data in database.
   
3. How is the overall level of the course during this unit? (instruction, course materials, etc.)
   Overall courses is great, is pretty amazing how we can build a full stack web application by ourselves, even though is far from perfection. 
