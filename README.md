# WeChatPYAPI介绍



《WeChatPYAPI》是基于PC端的Python接口，开发者可通过Python轻松调用。可进行二次开发，实现微信机器人、群管理等强大的功能！



- 稳定，可用于生产环境
- 支持多开、多控
- 售后有保障！持续更新迭代



## 使用教程

1. 克隆该项目<span style="color: red">（请关闭你的杀毒软件，否则可能会误删dll文件）</span>
2. 选择对应python解释器环境（如果你是32位的python，请打开32位文件夹）
3. 目前已支持最新版的微信版本，使用前请先把你的微信升级到最新版即3.3.0.115
4. 执行文件夹中的demo.py

> 或者下载对应版本的微信：https://pan.baidu.com/s/1mWWV449fTdY5KeSw4cw-Qg 
>
> 提取码：mevk 



## 疑问解答、联系方式

- QQ群：54995858
- 作者QQ：437382693
- 进群解决一切蛇皮问题！



## help(WeChatPYApi)

```python
class WeChatPYApi(builtins.object)
 |  基于PC微信的Python-API
 |  
 |  Methods defined here:
 |  
 |  __init__(self, msg_callback, **kwargs)
 |      初始化方法
 |      :param msg_callback: 消息回调函数
 |      :param exit_callback: 退出微信后的回调函数
 |      :param logger: 日志器句柄
 |      :param kwargs: 略
 |  
 |  add_friend(self, self_wx, to_wx, msg)
 |      添加好友
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 要添加的微信ID
 |      :param msg: 添加时的打招呼消息
 |      :return: 无
 |  
 |  agree_friend(self, self_wx, msg_data)
 |      同意添加好友请求
 |      :param self_wx: 当前微信ID
 |      :param msg_data: 好友请求时的消息数据
 |      :return: 无
 |  
 |  agree_friend_invite_join_chat_room(self, self_wx, msg_data)
 |      同意好友邀请进群
 |      :param self_wx: 当前微信ID
 |      :param msg_data: 消息数据
 |      :return: 无
 |  
 |  alter_chat_room_name(self, self_wx, to_chat_room, name)
 |      修改群名称
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param name: 群名称
 |      :return: 无
 |  
 |  alter_friend_remark(self, self_wx, to_wx, remark)
 |      修改好友备注
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 好友微信ID
 |      :param remark: 备注内容
 |      :return: 无
 |  
 |  alter_my_name_in_chat_room(self, self_wx, to_chat_room, name)
 |      修改我在群里的昵称
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param name: 昵称
 |      :return: 无
 |  
 |  chat_room_member_remark_switch(self, self_wx, to_chat_room, switch)
 |      显示/隐藏群成员昵称
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param switch: True:显示 False:隐藏
 |      :return: 无
 |  
 |  collection(self, self_wx, msg_data)
 |      收款
 |      :param self_wx: 当前微信ID
 |      :param msg_data: 消息数据
 |      :return: 无
 |  
 |  create_chat_room(self, self_wx, wx_id_list)
 |      创建群聊
 |      :param self_wx: 当前微信ID
 |      :param wx_id_list: 邀请进群的微信ID列表
 |      :return: 无
 |  
 |  delete_chat_room_member(self, self_wx, to_chat_room, to_wx)
 |      踢出群成员
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param to_wx: 群成员微信ID
 |      :return: 无
 |  
 |  delete_friend(self, self_wx, to_wx)
 |      删除好友
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 要删除的微信ID
 |      :return: 无
 |  
 |  exit_chat_room(self, self_wx, to_chat_room)
 |      退出群聊
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :return: 无
 |  
 |  follow_mp(self, self_wx, mp_id)
 |      关注公众号
 |      :param self_wx: 当前微信ID
 |      :param mp_id: 公众号ID
 |      :return: 无
 |  
 |  get_chat_room_members(self, self_wx, to_chat_room)
 |      获取群成员列表
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :return: list数据
 |  
 |  get_chat_room_members_of_work(self, self_wx, to_chat_room)
 |      获取企业群成员列表
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 企业群ID
 |      :return: list数据
 |  
 |  get_self_info(self)
 |      获取个人信息
 |      :return: 未登录时返回None，登录成功返回字典数据
 |  
 |  invite_friend_enter_chat_room(self, self_wx, to_chat_room, to_wx)
 |      邀请好友进群
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param to_wx: 好友微信ID
 |      :return: 无
 |  
 |  keep_msg_switch(self, self_wx, switch)
 |      开启/关闭消息防撤回
 |      :param self_wx: 当前微信ID
 |      :param switch: True:开启 False:关闭
 |      :return: 无
 |  
 |  logout(self, self_wx)
 |      退出登录
 |      :param self_wx: 当前微信ID
 |      :return: 无
 |  
 |  mask_msg_switch(self, self_wx, to_id, switch)
 |      开启/关闭消息免打扰
 |      :param self_wx: 当前微信ID
 |      :param to_id: 好友ID/群ID
 |      :param switch: True:开启免打扰 False:关闭免打扰
 |      :return: 无
 |  
 |  pull_list(self, self_wx, pull_type)
 |      拉取列表（好友/群/公众号/其他）
 |      :param self_wx: 当前微信ID
 |      :param pull_type: 好友:1 群:2 公众号:3 其他:4
 |      :return: list数据
 |  
 |  pull_list_of_work(self, self_wx)
 |      拉取企业微信列表（好友/群）
 |      :param self_wx: 当前微信ID
 |      :return: dict数据
 |  
 |  refund(self, self_wx, msg_data)
 |      退款
 |      :param self_wx: 当前微信ID
 |      :param msg_data: 消息数据
 |      :return: 无
 |  
 |  save_img(self, self_wx, save_path, msg_data)
 |      保存图片
 |      :param self_wx: 当前微信ID
 |      :param save_path: 保存图片的绝对路径
 |      :param msg_data: 消息数据
 |      :return: 无
 |  
 |  send_card_link(self, self_wx, to_wx, title, desc, target_url, img_url)
 |      发送卡片链接
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 接收者微信ID
 |      :param title: 卡片标题
 |      :param desc: 卡片描述
 |      :param target_url: 目标地址
 |      :param img_url: 卡片封面地址
 |      :return: 无
 |  
 |  send_file(self, self_wx, to_wx, path)
 |      发送文件/视频消息
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 接收者微信ID
 |      :param path: 文件/视频的绝对路径
 |      :return: 无
 |  
 |  send_friend_card(self, self_wx, to_wx, friend_wx, friend_name)
 |      发送好友名片
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 接收者微信ID
 |      :param friend_wx: 好友微信ID
 |      :param friend_name: 好友昵称
 |      :return: 无
 |  
 |  send_img(self, self_wx, to_wx, path)
 |      发送图片消息
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 接收者微信ID
 |      :param path: 图片的绝对路径
 |      :return: 无
 |  
 |  send_notice(self, self_wx, to_chat_room, msg)
 |      发送群公告
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param msg: 公告内容
 |      :return: 无
 |  
 |  send_text(self, self_wx, to_wx, msg)
 |      发送文本消息
 |      :param self_wx: 当前微信ID
 |      :param to_wx: 接收者微信ID
 |      :param msg: 消息内容
 |      :return: 无
 |  
 |  send_text_and_at_member(self, self_wx, to_chat_room, to_wx, name, msg)
 |      群聊发送文本信息并且@指定群成员
 |      :param self_wx: 当前微信ID
 |      :param to_chat_room: 群ID
 |      :param to_wx: @人的微信ID
 |      :param name: @人的微信昵称
 |      :param msg: 文本消息
 |      :return: 无
 |  
 |  send_xml(self, self_wx, to_wx, xml_str)
 |      发送xml信息
 |      :param self_wx:
 |      :param to_wx:
 |      :param xml_str:
 |      :return: 无
 |  
 |  start_wx(self, path=None)
 |      启动微信，目前支持微信版本：V-3.3.0.115
 |      :param path: 保存登录二维码的绝对路径
 |      :return: 无
 |  
 |  top_chat_switch(self, self_wx, to_id, switch)
 |      置顶/取消置顶聊天
 |      :param self_wx: 当前微信ID
 |      :param to_id: 好友ID/群ID
 |      :param switch: True:置顶 False:取消置顶
 |      :return: 无
 |  
 |  ----------------------------------------------------------------------
```



## 声明

**本项目仅供技术研究，请勿用于非法用途，如有任何人凭此做何非法事情，均于作者无关，特此声明。**



<script type="text/javascript">
    localStorage.gitbook_dir = location.href
</script>
