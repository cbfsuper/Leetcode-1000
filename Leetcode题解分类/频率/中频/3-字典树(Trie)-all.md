### <a id="_link_click_group">LeetCode-字典树(Trie)-all-题单</a>
##### [LeetCode-208.实现](#_id208)
##### [LeetCode-211.添加与搜索单词](#_id211)
##### [LeetCode-212.单词搜索](#_id212)
##### [LeetCode-336.回文对](#_id336)
##### [LeetCode-421.数组中两个数的最大异或值](#_id421)
##### [LeetCode-425.单词方块](#_id425)
##### [LeetCode-472.连接词](#_id472)
##### [LeetCode-642.设计搜索自动补全系统](#_id642)
##### [LeetCode-648.单词替换](#_id648)
##### [LeetCode-676.实现一个魔法字典](#_id676)
##### [LeetCode-677.键值映射](#_id677)
##### [LeetCode-692.前K个高频单词](#_id692)
##### [LeetCode-720.词典中最长的单词](#_id720)
##### [LeetCode-745.前缀和后缀搜索](#_id745)
##### [LeetCode-1023.驼峰式匹配](#_id1023)
##### [LeetCode-1032.字符流](#_id1032)
##### [LeetCode-1065.字符串的索引对](#_id1065)
##### [LeetCode-1638.统计只差一个字符的子串数目](#_id1638)
##### [LeetCode-1698.字符串的不同子字符串个数](#_id1698)
##### [LeetCode-1707.与数组中元素的最大异或值](#_id1707)

###
字典树基础参考:https://leetcode-cn.com/problems/implement-trie-prefix-tree/   
字典树的两种构造方式  
### LeetCode-字典树(Trie)-all-题解
参考:https://blog.csdn.net/qq_43152052/article/details/101109415  
字典树模板代码:  
```
class Trie {
    TrieNode root;
    class TrieNode{
        private TrieNode[] kids;
        private boolean isEnd;
        final int R = 26;
        TrieNode(){
            kids = new TrieNode[R];
        }
        public boolean isEnd(){
            return isEnd;
        }
        public void setEnd(){
            this.isEnd = true;
        }
        public TrieNode getNode(char ch){
            return kids[ch-'a'];
        } 
        public void setNode(char ch, TrieNode node){
            this.kids[ch-'a'] = node;
        }
    }
    /** Initialize your data structure here. */
    public Trie() {
        this.root = new TrieNode();
    }
    
    /** Inserts a word into the trie. */
    public void insert(String word) {
        TrieNode node = root;
        for(char w:word.toCharArray()){
            if(node.getNode(w)==null){
                node.setNode(w, new TrieNode());
            }
            node = node.getNode(w);
        }
        node.setEnd();
    }
    public TrieNode searchNode(String word){
        TrieNode node = root;
        for(char ch:word.toCharArray()){
            if(node.getNode(ch)==null){
                return null;
            }
            node = node.getNode(ch);
        }
        return node;
    }
    /** Returns if the word is in the trie. */
    public boolean search(String word) {
        TrieNode node = searchNode(word);
        return node!=null && node.isEnd();
    }

    
    /** Returns if there is any word in the trie that starts with the given prefix. */
    public boolean startsWith(String prefix) {
        TrieNode node = searchNode(prefix);
        return node!=null;
    }
}
```
##### <a id="_id208">[LeetCode-208.实现](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id211">[LeetCode-211.添加与搜索单词](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id212">[LeetCode-212.单词搜索](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id336">[LeetCode-336.回文对](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id421">[LeetCode-421.数组中两个数的最大异或值](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id425">[LeetCode-425.单词方块](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id472">[LeetCode-472.连接词](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id642">[LeetCode-642.设计搜索自动补全系统](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id648">[LeetCode-648.单词替换](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id676">[LeetCode-676.实现一个魔法字典](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id677">[LeetCode-677.键值映射](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id692">[LeetCode-692.前K个高频单词](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id720">[LeetCode-720.词典中最长的单词](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id745">[LeetCode-745.前缀和后缀搜索](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1023">[LeetCode-1023.驼峰式匹配](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1032">[LeetCode-1032.字符流](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1065">[LeetCode-1065.字符串的索引对](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1638">[LeetCode-1638.统计只差一个字符的子串数目](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1698">[LeetCode-1698.字符串的不同子字符串个数](#_link_click_group)</a>
题目描述:
思路:
```

```
##### <a id="_id1707">[LeetCode-1707.与数组中元素的最大异或值](#_link_click_group)</a>
题目描述:
思路:
```

```
