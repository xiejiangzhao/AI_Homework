# 接口说明
```angular2html
extern "C" {
void deploy(int *pos);
void ai_move(int *pos);
void ran_move(int *pos);
void reload();
};
```
- deploy接收一个长度为5的int数组，第一第二个元素为下子坐标，第五个元素为下子颜色，1为黑棋，-1为白棋，这个是测试程序给AI的更新棋盘信息
- ai_move接收一个长度为5的int数组，第三第四个元素为AI计算出来的下子坐标，第五个元素为下子颜色，1为黑棋，-1为白棋，这个是AI根据自己棋盘状况计算出来后给测试程序的下棋位置
- ran_move接收一个长度为5的int数组，第三第四个元素为AI计算出来的下子坐标，第五个元素为下子颜色，1为黑棋，-1为白棋，这个是AI根据棋盘状况给测试程序的下棋位置，必须合理
- reload 初始化AI的所有棋盘信息，清除上一次下棋信息，恢复到最开始的状态