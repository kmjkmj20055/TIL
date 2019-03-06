#Rownum 하는 방법
##리스트에 no를 보여줘야 할 때
Http://ohgyun.com/39

SELECT QNA_BOARD_NO as qna_board_no, QNA_BOARD_FILE as qna_board_file,
QNA_BOARD_TITLE as qna_board_title,
QNA_BOARD_CONTENT as qna_board_content,
QNA_BOARD_ANSWER_STATUS as qna_board_answer_status,
SUBSTR(QNA_BOARD_INSERT_DATE, 0, 10) as qna_board_insert_date,
ROW_NUMBER() OVER(ORDER BY QNA_BOARD_INSERT_DATE) NO
FROM QNA_BOARD
ORDER BY NO DESC 
