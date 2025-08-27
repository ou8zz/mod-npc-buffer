### 修改自 azerothcore/mod-npc-buffer 
### NPC Buffer 改为 物品 Buffer

### 之前是NPC在哪儿去领一个buffer，但是我们都是在副本或者boss面前需要用，领buffer这种设定很麻烦，所以改为物品触发。

#### 我这边使用物品是小宝的丝带 entry = 52019 需要修改几个字段
```sql

update item_template set flags = 67141696, scriptName = 'buff_item', discription = '比心，爱你，点击获取多个增益' where entry = 52019;

```

#### 重新编译即可

#### 这样就不需要NPC了，直接绑定物品触发Buffer