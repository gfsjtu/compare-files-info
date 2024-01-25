# compare-files-info
Compare files info: They have the same elements, but the sequence is diff.
两个文件里面的元素是相同的，但是每个元素顺序是不同的，使用什么方法可以判断这两个文件里的元素是否一样的，使用python，比较的代码

from collections import Counter

def compare_files(file1, file2):
    with open(file1, 'r') as f:
        counter1 = Counter(f.read().split())
    with open(file2, 'r') as f:
        counter2 = Counter(f.read().split())
    return counter1 == counter2

# 使用函数
file1 = 'file1.txt'
file2 = 'file2.txt'
print(compare_files(file1, file2))
