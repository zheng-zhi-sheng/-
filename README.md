
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    ListNode* removeElements(ListNode* head, int val) {
        ListNode *p=new ListNode(0),*pre,*cur=head;
        p->next=head;
        pre=p;
        while(cur){
            if(cur->val==val){
                pre->next=cur->next;
                cur=pre->next;
            }
            else {
                pre=cur;
                cur=pre->next;
            }
        }
        return p->next;
    }
};
