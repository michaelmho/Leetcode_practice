# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def addTwoNumbers(self, l1: Optional[ListNode], l2: Optional[ListNode]) -> Optional[ListNode]:
        l3 = curr = ListNode()
        carryover = 0

        while l1 or l2:
            d = carryover
            if l1 and l2:
                d += (l1.val + l2.val)
                l1 = l1.next 
                l2 = l2.next
            elif l1 and not l2:
                d += l1.val
                l1 = l1.next
            elif l2 and not l1:
                d += l2.val
                l2 = l2.next

            carryover = d // 10
            curr.next = ListNode(d % 10)
            curr = curr.next
        if carryover == 1: curr.next = ListNode(1)
        return l3.next
