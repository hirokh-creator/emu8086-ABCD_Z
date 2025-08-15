# emu8086-ABCD_Z



.model small
.stack 100h 

.data
str db 10, 13, "Hello world:$"


 
.code 

main proc 
    
      mov ax,@data
     mov ds,ax
     
          mov cx,26
          mov bl,"A"
          
          HelloLabel:
          mov dl,bl
          mov ah,2
          int 21h
          add bl,1; inc bl
          
          loop HelloLabel
  
  
     
    
    main endp
end main
