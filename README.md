# 2
def bfs(graph, start):
    visited, queue = [], [start]
    while queue:
        node = queue.pop(0)
        if node not in visited:
            visited.append(node)
            print(node, end=" ")
            queue.extend(neighbour for neighbour in graph[node] if neighbour not in visited)

# Driver Code
graph = {
    '5': ['3', '7'],
    '3': ['2', '4'],
    '7': ['8'],
    '2': [],
    '4': ['8'],
    '
