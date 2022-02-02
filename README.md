# assignment2-manchala
# sai chandh Manchala
 ###### kfc
 my favourite  place to buy food is : hyderbad
 we can find indian style dosa in **Dosaart** to near kfc
 we acmn also find ***muttonbiryani** in  drunken monkey restaurent



 --------------------------------------------------------------

# Gannavaram Airport
## Gannavaram Airport is the closest Airport to my Food location

   - After getting out from the restarunt go straight towards gorantlaa

   - than take left so that you can enter into highway

   - go straight for 2km so that u can get a bypass

   - after entering into the bypass take a immidate left and than immidate right


   ## Food items

1. Chicken Mandi
2. Mutton Mandi
3. Prawns Mandi

---------------------------------------------------------------------

[link to my "about.md " file](https://github.com/chandu-manchala/assignment2-manchala/blob/main/AboutMe.md)


--------------------------------------------------------------------

# Sports

| Name   | Location   | Amount   |
|--------|------------|----------|
| Volley Ball   |Guntur   | $40   |
| Basket Ball   | Vijayawada   | $20   |
| Throw Ball   | Hyderabad   |$15   |

-------------------------------------------------------------------

# pithy Quotes

>The way to get started is to quit talking and begin doing-*Walt Disney*
>
>Life is what happens when you're busy making other plans-*John Lennon*

---------------------------------------------------------------------
# code fencing

>The algorithm exists in many variants. Dijkstra's original algorithm found the shortest path between two given nodes,[6] but a more common variant fixes a single node as the "source" node and finds shortest paths from the source to all other nodes in the graph, producing a shortest-path tree.

<https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm>

```
const int INF = 1000000000;
vector<vector<pair<int, int>>> adj;

void dijkstra(int s, vector<int> & d, vector<int> & p) {
    int n = adj.size();
    d.assign(n, INF);
    p.assign(n, -1);
    vector<bool> u(n, false);

    d[s] = 0;
    for (int i = 0; i < n; i++) {
        int v = -1;
        for (int j = 0; j < n; j++) {
            if (!u[j] && (v == -1 || d[j] < d[v]))
                v = j;
        }

        if (d[v] == INF)
            break;

        u[v] = true;
        for (auto edge : adj[v]) {
            int to = edge.first;
            int len = edge.second;

            if (d[v] + len < d[to]) {
                d[to] = d[v] + len;
                p[to] = v;
            }
        }
    }
}
```
<https://cp-algorithms.com/graph/dijkstra.html>