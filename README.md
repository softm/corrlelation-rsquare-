<style>
.MJXp-math.MJXp-display {
  display:inline !important;
}
</style>
<div id="contents">
## 상관관계 분석(Correlation Analysis)?
  - 상관관계는 연속적 속성을 갖는 두 변인들 간 상호연관성에 대한 기술 통계를 제공할 뿐 아니라,
  - 두 변인 간의 상호 연관성에 대한 통계적 유의성을 검증해 주는 통계분석 기법
  - r=.30 약한 관계
  - r=.50 중간 관계
  - r=.70 강한 관계.
  - 두 변인간의 강도와 방향을 산포도(scatterplot)로 표현.

    2차원 공간에서 변인 X(가로축)와 Y(세로축)에 대한 각 케이스 값들 나타냄.

    r이 커질수록 두 변인간의 관계를 나타내는 데이터들이 점점 조밀.

    반대의 경우 변인간 데이터들은 점점 흩어짐.

  - r의 절대값이 클수록 (1에 가까울수록) 두 변수의 값들은 직선 가까이에 위치하며

    따라서 두 변수 사이의 선형적인 상관성은 커진다.

  - r이 절대값이 1일 때 두 변수의 값은 모두 직선 위에 위치 (perfect correlation)

    -> 한 변인의 값을 알면 다른 변인의 값을 정확하게 예측할 수 있음.

  - r이 0일 때 두 변수 사이에 선형적인 상관성은 없다

    -> 한 변인의 값을 알아도 다른 변인의 값을 전혀 예측할 수 없음.

## 상관관계 계수(correlation coefficient)와 공변량(covariance)의 비교
  - Pearson 상관계수는 두 연속형 변수 사이의 선형적인 상관성(linear correlation)을 분석.

  - 커뮤니케이션 분야에서는 흔히 피어슨(곱적률) 상관계수 r 을 자주 사용: -1 +1 사이

  - Karl Pearson -> Pearson’s product-moment coefficients of correlation
    = Pearson correlation coefficient = Zero order correlation coefficient -> r

  - 피어슨 상관계수, 스피어만 상관계수, 켄달의 순위 상관계수

## 평균과 공변량과 상관계수
   - **평균** : https://ko.wikipedia.org/wiki/평균
     * 몇 개의 수치의 대표로서 채용되는 값의 하나.
     * 산술 평균·상승 평균·조화 평균 등이 있음. 보통 산술 평균을 가리킴.
        * $${\displaystyle {\bar {x}}={\frac {1}{n}}\cdot \sum _{i=1}^{n}{x_{i}}}$$
<br/>
   - **편차(deviation)** : https://ko.wikipedia.org/wiki/편차
     * 관측값(x)에서 평균($$\bar{x}$$) 또는 중앙값을 뺀 값.
        * $$d = x - \bar{x}$$
<br/>
     * 편차 d의 표준편차($$s_{d}$$)는 변인 Y의 표준편차($$s_{y}$$)와 같다.
        * $${\displaystyle s_{d}=s_{y}}$$
        * $${\displaystyle \because s_{d}={\sqrt {\frac {\Sigma (d-{\overline {d}})^{2}}{n-1}}}={\sqrt {\frac {\Sigma (y-{\overline {y}})^{2}}{n-1}}}=s_{y}}$$        
<br/>        
   - **분산(分散, 영어: variance)** : https://ko.wikipedia.org/wiki/분산
      - 확률변수가 기댓값으로부터 얼마나 떨어진 곳에 분포하는지를 가늠하는 숫자.

      - 기댓값은 확률변수의 위치를 나타내고
      - 분산은 그것이 얼마나 넓게 퍼져 있는지를 나타낸다.
      - 분산보다는 분산의 제곱근인 표준편차가 더 자주 사용된다.

      - 값을 제곱하고, 그것을 모두 더한 후 전체 갯수로 나눠서 구한다.
<br/>
      - $$σ^2$$ = $$\frac{\sum(X - \mu_{X})^2}{(m)}$$ = **모분산**
           - $$\mu_{X}$$ : 모집단 X의 평균값
<br/>       
      - $$s^2$$ = $$\frac{\sum(x - \bar x)^2}{(n-1)}$$ = **표본분산**
           - $$\bar{x}$$ : 표본집단 X의 평균값      
<br/>

       **즉, 차이값의 제곱의 평균이다.**
<br/>       
      - **관측값에서 평균을 뺀 값인 편차를 모두 더하면 0이 나오므로 제곱해서 더한다.**
<br/>
      - **모 분산(population variance) $$σ^2$$** 은 모 집단의 분산이다.

        **관측값에서 모 평균을 빼고** 그것을 **제곱한 값** 을 **모두 더하여**
        **전체 데이터 수 m** 으로 **나눈 것** 이다.
<br/>
      - **표본 분산(sample variance)** $$s^2$$은 표본의 분산이다.

        :> **관측값에서 표본평균을 빼고** **제곱한 값** 을 **모두 더한 것을**
          **n-1** 로 **나눈 것** 이다.
<br/>
          > $$s^{2}={\frac  {\Sigma (y-\overline {y})^{2}}{n-1}}={\frac  {SS}{df}}$$

<br/>

  - **기댓값 (期待값, expected value)** : https://ko.wikipedia.org/wiki/기댓값
    - 확률론에서, 확률 변수의 기댓값(期待값, 영어: expected value)은

      **각 사건이 벌어졌을 때의 이득**과 **그 사건이 벌어질 확률**을 **곱한** 것을

      **전체 사건에 대해 합한 값** 이다.
<br/>

    - $$\operatorname {E}(X)=\sum _{i}p_{i}x_{i}$$
           - $${x_i}$$ : 가능한 모든 사건.
           - $${p(x_{i})}$$ : $$x_i$$ 사건이 일어날 확률.
<br/>
           - 예를 들어, 주사위를 한 번 던졌을 때, 각 눈의 값이 나올 확률은 1/6이고,
      주사위값의 기댓값은 각 눈의 값에 그 확률을 곱한 값의 합.
<br/>
           - **각 사건이 벌어졌을 때의 이득** : 1 ~ 6 까지의 눈의 값.
           - **그 사건이 벌어질 확률** : $$\frac{1}{6}$$
           - **곱한** & **전체 사건에 대해 합한 값** :

        = $${\displaystyle 1\cdot {\frac {1}{6}}+2\cdot {\frac {1}{6}}+3\cdot {\frac {1}{6}}+4\cdot {\frac {1}{6}}+5\cdot {\frac {1}{6}}+6\cdot {\frac {1}{6}}=3.5}$$
<br/>

   - **표준편차(標準 偏差, 영어: standard deviation)** : https://ko.wikipedia.org/wiki/표준편차
     - **분산의 제곱근값**
     - 표준편차가 작을수록 평균값에서 변량들의 거리가 가깝다.
<br/>
     - 일반적으로 **모집단의 표준편차는 $$\sigma$$ (시그마)** 로,
       **표본의 표준편차는 $${S}$$(에스)** 로 나타낸다.
<br/>   
       - **모집단 표준편차** ( $$\sigma$$ )

         $$\sqrt\frac{\sum(x - \mu)^2}{(m)}$$ = $$\sqrt{σ^2}$$ = **모분산의 제곱근** = **모표준편차**
<br/>         
       - **표본 표준편차*** ( $$s$$ )

         $$\sqrt\frac{\sum(x - \bar x)^2}{(n-1)}$$ = $$\sqrt{s^2}$$ = **표본분산의 제곱근** = **표본표준편차**       
<br/>
     - 확률변수 $${\displaystyle X}$$ 의 흩어짐을 재는 데 사용되는 표준 편차 $${\displaystyle \sigma_{X}}$$ 는
        > $${\sigma_{X}={\sqrt {\operatorname {E} (X-\operatorname {E} (X))^{2}}}}$$

   - **공변량(covariance)** : 공분산 : https://ko.wikipedia.org/wiki/공분산
     - 여러 변수들이 공통적으로 함께 공유하고 있는 변량을 뜻한다.
     - 공분산(共分散, 영어: covariance)은 2개의 확률변수의 상관정도를 나타내는 값이다.
       (1개의 변수의 이산정도를 나타내는 분산과는 별개임)
<br/>
       > 만약 2개의 변수중 **하나의 값이 상승** 하는 경향을 보일 때,
       **다른 값도 상승** 하는 경향의 상관관계에 있다면, **공분산의 값은 양수** 가 될 것이다.

       > 반대로 2개의 변수중 **하나의 값이 상승** 하는 경향을 보일 때,
       **다른 값이 하강** 하는 경향을 보인다면 **공분산의 값은 음수** 가 된다.

       > 이렇게 공분산은 상관관계의 상승 혹은 하강하는 경향을 이해할 수 있으나 2개 변수의 측정 단위의 크기에 따라 값이 달라지므로 상관분석을 통해 정도를 파악하기에는 부적절하다. 상관분석에서는 상관관계의 정도를 나타내는 단위로 모상관계수 ρ를 사용한다.

     * $${cov}(X,Y) = \frac{\sum(X - \bar{X})(Y - \bar{Y})}{(N-1)} $$ = $$\operatorname {E}((X-\mu )(Y-\nu )^{\top }).\,$$

        - $$X$$ : 표본 집단 X
       - $$Y$$ : 표본 집단 Y
       - $$\bar{X}$$ : X평균
       - $$\bar{Y}$$ : Y평균     
       - N : 자료수
<br/>
   - **상관관계 계수(Correlation coefficient)**
      * 정의 및 참고
        - https://en.wikipedia.org/wiki/Pearson_correlation_coefficient
        - https://ko.wikipedia.org/wiki/상관_분석

      - 두 변수간에 어떤 선형적 관계를 갖고 있는 지를 분석하는 방법.
      - 단위로 모상관계수 ρ
<br/>

   - **모집단(population)에 대한 피어슨 상관 계수**
   <br/>   
        - $$\rho_{X,Y}={\frac{\operatorname{cov}(X,Y)}{\sigma_{X}\sigma_{Y}}}$$ =  공변량 ÷ ( 모집단 X의 표준편차 × 모집단 Y의 표준편차 )
   <br/>
          - $${cov}(X,Y)$$ = 공변량 = $$\frac{\sum{(X - \mu_{X})(Y - \mu_{Y})}}{(m)}$$
          - $$\sigma_{X}$$ = 모집단 X의 표준편차
          - $$\sigma_{Y}$$ = 모집단 Y의 표준편차
          - m = 모집단의 개체수
   <br/>
         - **모집단 표준편차** ( $$\sigma$$ )
           $$\sqrt\frac{\sum(x - \mu)^2}{(m)}$$ = $$\sqrt{σ^2}$$ = **모분산의 제곱근** = **모표준편차**
<br/>
   - **표본 상관 계수(sample correlation coefficient)에 대한 피어슨 상관 계수**
<br/>   
     - $$\rho ={\frac{\operatorname{cov}(X,Y)}{s{X}s{Y}}}$$ =  공변량 ÷ ( 표본집단 X의 표준편차 × 표본집단 Y의 표준편차 )
<br/>

          - $${cov}(X,Y)$$ = 공변량 = $$\frac{\sum{(x - \bar{x})(y - \bar{y})}}{(n-1)}$$
          - $$s_{X}$$ = 표본집단 X의 표준편차
          - $$s_{Y}$$ = 표본집단 Y의 표준편차
          - n = 표본집단의 개체수
<br/>
      - **표본 표준편차*** ( $$s$$ )
        $$\sqrt\frac{\sum(x - \bar x)^2}{(n-1)}$$ = $$\sqrt{s^2}$$ = **표본분산의 제곱근** = **표본표준편차**

## 상관계수 계산.

| 응답자 |교육 점수| 차이 점수 | 텔레비전시청시간| 차이 점수 |
|:------|:-------:|:--------:|:-------------:|:--------:|
| 1     | 2 |2 - 3.2 = -1.2 | 3 | 3 - 3.4 = -0.4|
| 2     | 2 |2 - 3.2 = -1.2 | 2 | 2 - 3.4 = -1.4|
| 3     | 3 |3 - 3.2 = -0.2 | 4 | 4 - 3.4 = +0.6|
| 4     | 4 |4 - 3.2 = +0.8 | 3 | 3 - 3.4 = -0.4|
| 5     | 5 |5 - 3.2 = +1.8 | 5 | 5 - 3.4 = +1.6|
| 평균 | | 3.2 | | 3.4|
| 표준편차 | | 1.30 | | 1.14|

> 공변량 
 = $$\frac{(-1.2)(0.4) + (-1.2)(-1.4) + (-0.2)(0.6) + (0.8)(0.4) + (1.8)(1.6) }{4}$$
 = $$\frac{(0.48) + (1.68) + (-0.12) + (0.32) + (2.88) }{4}$$
 = $$1.15$$

## 참고
  - [모집단(population), 표본집단(sample)](https://m.blog.naver.com/PostView.nhn?blogId=istech7&logNo=50151725609&proxyReferer=https%3A%2F%2Fwww.google.co.kr%2F)
- [상관 계수(correlation coefficient) 와 결정 계수(coefficient of determination)](https://m.blog.naver.com/istech7/50153288534)

<br/>
## 수학기호 참고
  - http://freesearch.pe.kr/archives/707
  - https://librewiki.net/wiki/수학_기호
  > σ : 소문자 시그마는 표준편차를 나타내는 기호
    Σ : 대문자 시그마는 아래첨자와 위첨자를 기입하여 합에 관한 기호로 사용
    i : 아이. 허수단위. 제곱해서 -1이 되는 수입니다.
    cosΘ : 코사인쎄타인듯 보입니다. cosθ를 쓴거 맞는지요?
    (하이퍼블릭코사인-쌍곡삼각함수중 하나로 수학에서는 거의 cosh를 사용합니다)
    √ – 제곱근 또는 루트라고 읽습니다.
    ㅠ – 파이 : 정확한 모양을 모르겠는데, 소문자 파이는 원주율을 나타내는 기호로 3.141592… 값을 가지며, 대문자 파이는 확률에서 중복순열을 나타내거나 위첨자 아래첨자와 함께 쓰는 경우 곱에 관한 기호가 됩니다.
    ∫ – 인테그랄 : 적분기호
    ∬ – 중적분 기호로, 적분을 두번 하라는 것입니다.
    V。 – ? 뭡니까 이건? 혹시 V만 쓴 것이라면 분산을 나타내는 것이긴 한데… 이건 잘 모르겠군요
    ± – 플러스마이너스 : 플러스 또는 마이너스 라는 뜻
    × – 곱하기
    ÷ – 나누기
    ∏ – 대문자 파이군요.. 위에서 설명드렸고..
    ≠ – 같지앉다
    ∴ – 따라서 또는 그러므로
    ∵ – 왜냐하면
    ≒ – 약: 근사값을 쓸때 또는 양쪽 값이 거의 비슷할때 사용
    ≤ – (왼쪽이 오른쪽보다) 작거나 같다
    ≥ – (왼쪽이 오른쪽보다) 크거나 같다
    ＜ – (왼쪽이 오른쪽보다) 작다
    ＞ – (왼쪽이 오른쪽보다) 크다
    dθ – 디쎄타 – 미분에서 사용되는 기호입니다.
    ≡ – 합동 또는 모듈로(mod)를 나타내는 기호인데… 아마 질문하신 님이 알파, 베타를 읽을 줄 모르신다면,, 나이가 어리신듯 한데, 만약 십대시라면, 그냥 도형의 합동 기호라고 알아두는게 좋을 듯 합니다.
    ∈ – (왼쪽이 오른쪽의) 원소이다.
    ∋ – (오른쪽이 왼쪽의) 원소이다.
    ⊂ – (왼쪽이 오른쪽의) 부분집합이다. (오른쪽 집합이 왼쪽 집합을) 포함한다.
    ⊃ – (오른쪽이 왼쪽의) 부분집합이다. (오른쪽 집합이 왼쪽 집합을) 포함한다.
    ∪ – 합집합
    ∩ – 교집합
    ∀ – 임의의
    ∃ – 존재한다. exist.

  > Å – 옴스트롱 또는 옴고스트롱. 10의 -10승인가 -8승인가… 뭐 그런건데, 수학에서 쓰이는 건 여태 단 한번도 본 적이 없음.
    μ(마이크로) – 10의 -6승. 즉, 1/1000000 의 크기.
    ℉ – 화씨. 온도 단위
    ℃ – 섭씨. 역시 온도의 단위. 다들 아시죠..
    ㎛(마이크로미터) ㎝(센티미터) – 길이의 단위
    ㎟(제곱밀리미터)㎩ ㎢(제곱키로미터) – 넓이의 단위
    ㎣(세제곱밀리미터) ㎤(세제곱 센티미터) ㎥(세제곱 미터) ㎦(세제곱 키로미터) – 부피의 단위.
    ㏈ – 데시벨. 소리의 단위
    ㎲ -마이크로초. 시간의 단위
    ㏘ -뭐라고 쓴건지 잘 모르겠는데.. pm이라고 쓴건가요? 그렇다면 피코미터라고, 길이의 단위인데..

  > 집합기호 : { }, ⊂,⊃,⊆,⊇,
    명제기호 : ∧,∨,←,→,⇔,⇒,⇒
    도형기호 : ∠(각),∽(닮음),≡(합동),?(평행),⊥(수직)
    대소관계 : <, >, ≤,≥,
    각종괄호 : (,),{,},[,]
    적분기호 : ∫, ∬, ∮
    미분기호 : ∂(편미분)
    삼각함수 : sin, cos, tan, sec, cosec, cot, sinh, cosh, tanh, sech, cosech, coth, 각각의 함수에 역함수 기호(^-1)를 붙이면 arc삼각함수(=역삼각함수)가 된다.
    기타 : ∞(무한대), !(팩토리얼,factorial), 기호가 표시는 안됩니다만.. 세제곱근호, 네제곱근호, 선적분, 면적분, 벡터기호, 등등 여러가지가 있습니다.

</div>
<script type="text/javascript" src="https://rawgit.com/softm/loader/master/loader.js"></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML' async></script>
    <script type="text/javascript">
    window.onload = function () {
        loader.js(
            [
                "https://cdnjs.cloudflare.com/ajax/libs/showdown/1.8.6/showdown.min.js",
                "https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.12.0/highlight.min.js",
                "https://cdnjs.cloudflare.com/ajax/libs/highlight.js/9.12.0/styles/default.min.css"
            ],
            [
              function(e) {
                console.log("1st",e);
              },
              function(e) {
                console.log("2nd",e);
              },
              function(e) {
                console.log("3rd",e);
                var container = document.getElementById("contents");
                var containers = [container];
                var sd = new showdown.Converter();
                for (var i = 0; i < containers.length; i++) {
                    containers[i].innerHTML = sd.makeHtml(containers[i].innerHTML);
                    var codes = containers[i].querySelectorAll("pre code");
/*
                    codes.forEach(function(code) {
                        hljs.highlightBlock(code);
                    });
*/
                    for(var j=0;j<codes.length;j++) {
                        var code = codes[j];
                             hljs.highlightBlock(code);
                    }
                }
              }
            ],
            false // default false
        );
    }
    </script>
