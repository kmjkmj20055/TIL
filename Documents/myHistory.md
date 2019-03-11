#rownum 하는 방법

####리스트에 no 보여줘야할 때

######기억은 안나는데 mysql이였던듯?

[참고했던 블로그] (<http://ohgyun.com/39>)

> SELECT QNA_BOARD_NO AS qna_board_no,
>
> ​        QNA_BOARD_FIELD AS qna_board_field,
>
> ​        QNA_BOARD_TITLE AS qna_board_title,
>
> ​        QNA_BOARD_CONTENT AS qna_board_content,
>
> ​        QNA_BOARD_ANSWER_STATUS AS qna_board_answer_status,
>
> ​        SUBSTR(QNA_BOARD_INSERT_DATE, 0, 10) AS
>
> qna_board_insert_date, ROW_NUMBER() OVER(ORDER BY QNA_BOARD_INSERT_DATE ) NO
>
> ​        FROM QNA_BOARD
>
> ​        ORDER BY NO DESC

