



-input의 길이를 제한하고 그 길이가 넘으면 다른 input으로 focus 되게 하는 예제


    <script>
    function focusme()
      {
        if(document.all.input1.value.length > 6)        //input의 값의 길이가 6이므로 value.length 라고 꼭 해줘야 된다.. 
        {
          document.all.input2.focus();
        }
      }

    </script>
    <body>
      <input type=text name=input1 onkeyup=focusme()>-<input type=text name=input2 maxlength=1>
    </body>
    
    
-length
   요소의 길이를 뜻함 값의 길이를 알고 싶거나 비교할 경우 사용해야함
   
-onkeypress
  onclick과 마찬가지인 이벤트의 한종류 나중에 이벤트를 한꺼번에 정리하겠다
  
-focus
  마우스의 커서가 자동으로 이동하도록 하는 함수
