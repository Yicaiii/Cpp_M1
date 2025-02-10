# TP4

## randomwalk部分
### 分析：
首先这个代码分为两部分，创建class，还有main函数运行。
1. 创建 class。
   ```cpp
   class RandomWalk {
   protected: 
      unsigned n; //temps courant n
      int s;// valeur de S_n
      int s_init;//valeur de S_0
      std::bernoulli_distribution U;
   public:
      RandomWalk(int s0,double p): n(0), s(s0), s_init(s0), U(p) {}
      int val() const { return s; } //accesseur à s
      unsigned time() const { return n;} //accesseur à n;
      virtual void reset() {s=s_init; n=0;} // redémarrage à l'état initial
      virtual void update(std::mt19937 & G);
            // passage de n à n+1 avec générateur G
   };

注意怎么加代码：mac左上角三个反引号```cpp或者```python.
知识点：
1. unsigned n，代表n是自然数，不可以为负数。
2. acceseur的介绍：
   


  
4. int main（）运行。
