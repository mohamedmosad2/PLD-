# PLD-
programming languages design
"Start Symbol" = <program>

!-------terminal------
id={letter}
 digit={digit} 
!---------rules-------
<program> ::= Start <stmt_list> End 
<stmt_list> ::=<concept> 
             |<concept> <stmt_list>
            
         
<concept>::=<assign> 
          |<if_stmt>
          |<for_stmt>

!------assign-----
<assign> ::=<id>'='<expr> ';'
         
<id> ::=Id 
     
<expr> ::=<expr>'+'<term>
       |<expr>'-'<term>
       |<term>
       
<term> ::=<term>'*'<factor>
       |<term>'/'<factor>
       |<term>'@'<factor>
       |<factor>
<factor> ::=<factor>'**'<expr>
         |<expr>
         
<expr> ::='('<expr>')'|<id>|<digit>
       
<digit>::=Digit
           
 !-----IF STMT-----
<if_stmt> ::=if'('<cond>')' Start <stmt_list> End 
          |if'('<cond>')' Start<stmt_list>End else <stmt_list>
          
<cond>  ::=<expr> <op> <expr>
       
<op>::= '<'|'>'|'=='|'!='

!-------for_stmt-----         
<for_stmt> ::=For'('<data><assign>';'<cond>';'<step>')''{'<stmt_list>'}'
           
<data> ::=int |float |double |string
       
<step>::= '--'<id>
       |<id>'--'
       |'++'<id>
       |<id>'++'
       |<assign>
