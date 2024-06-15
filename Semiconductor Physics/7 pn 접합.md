
## 7.1 pn 접합의 기본 구조

- 반도체 전체 영역은 단결정 물질
- 금속학적 접합(metallurgical junction): 접합의 계면
- 계단 접합(step junction): 계면에서 도핑 프로파일이 급격히 변화
![[Pasted image 20240616005602.png|400]]

- 공간 전하 영역(space charge region): 도펀트 이온에 의해 형성
- 열평형에서 안으로 작용하는 확산력과 밖으로 작용하는 전계력은 균형을 이룬다.

## 7.2 제로 인가 바이어스

### 7.2.1 내부 전위 장벽 (Built-in Potential Barrier)

*가정*
1. *열평형*
2. *볼츠만 근사*
3. *완전 이온화*

![[Pasted image 20240616011445.png|400]]
$$
V_{bi}=|\phi_{Fn}|+|\phi_{Fp}|
$$
$$
n_{0}=n_{i}\exp\left[ \frac{-e\phi_{Fn}}{kT} \right] \longrightarrow\phi_{Fn}=-\frac{kT}{e}\ln\left( \frac{N_{d}}{n_{i}} \right) \; (n_{0}=N_{d})
$$
$$
p_{0}=p_{i}\exp\left[ \frac{e\phi_{Fp}}{kT} \right] \longrightarrow\phi_{Fp}=+\frac{kT}{e}\ln\left( \frac{N_{a}}{n_{i}} \right) \; (p_{0}=N_{a})
$$
$$
V_{bi}=V_{t}\ln\left( \frac{N_{a}N_{d}}{n^{2}_{i}} \right)
$$

### 7.2.2 전계
![[Pasted image 20240616013235.png|400]]

p형 영역:
$$
E=\int \frac{\rho(x)}{\epsilon_{s}}dx=-\int \frac{eN_{a}}{\epsilon _{s}}dx=-\frac{eN_{a}}{\epsilon_{s}}x+C_{1}
$$

==전체 전기장==:
$$
E = \begin{cases}
-\frac{eN_{a}}{\epsilon_{s}}(x+x_{p}) & -x_{p}\leq x\leq 0 \\ \\
-\frac{eN_{d}}{\epsilon_{s}}(x_{n}-x) & 0\leq x\leq x_{n} \\
\end{cases}
$$
위치에 대한 전위: quadratic
$$
\phi(x)=-\int E(x)dx = \begin{cases}
\frac{eN_{a}}{2\epsilon_{s}}(x+x_{p})^{2} & -x_{p}\leq x\leq 0 \\
\frac{eN_{d}}{\epsilon_{s}}\left( x_{n}x-\frac{x^{2}}{2} \right)+\frac{eN_{a}}{2\epsilon_{s}}x^{2}_{p} & 0\leq x\leq x_{n}
\end{cases}
$$
==다시 정의한 전위 장벽==:
$$
V_{bi}=|\phi(x=x_{n})|=\frac{e}{2\epsilon_{s}}(N_{d}x^{2}_{n}+N_{a}x^{2}_{p})
$$

### 7.2.3 공간전하폭
$N_{a}x_{p}=N_{d}x_{n}$
$$
\longrightarrow x_{n}= 
\biggl\{
\frac{2\epsilon_{s}V_{bi}}{e} \left[ \frac{N_{a}}{N_{d}} \right] \left[ \frac{1}{N_{a}+N_{d}} \right]
\biggr\}^{1/2}
$$
$$
\longrightarrow x_{p}= 
\biggl\{
\frac{2\epsilon_{s}V_{bi}}{e} \left[ \frac{N_{d}}{N_{a}} \right] \left[ \frac{1}{N_{a}+N_{d}} \right]
\biggr\}^{1/2}
$$
==총 공간전하폭==:
$$
W=x_{n}+x_{p}=
\biggl\{
\frac{2\epsilon_{s}V_{bi}}{e}\bigg[\frac{N_{a}+N_{d}}{N_{a}N_{d}}\bigg]
\biggr\}^{1/2}
$$

## 7.3 역방향 인가 바이어스

### 7.3.1 공간전하폭과 전계
![[Pasted image 20240616020529.png|300]]

$$
V_{\text{total}}=V_{\text{bi}}+V_{\text{R}}
$$
$$
W=
\biggl\{
\frac{2\epsilon_{s}(V_{bi}+V_{R})}{e}\bigg[\frac{N_{a}+N_{d}}{N_{a}N_{d}}\bigg]
\biggr\}^{1/2}
$$
$$
E_{\text{max}}=
-\bigg\{
\frac{2e(V_{bi}+V_{R})}{\epsilon_{s}}
\left[\frac{N_{a}N_{d}}{N_{a}+N_{d}}\right]
\bigg\}^{1/2}
=-\frac{2(V_{bi}+V_{R})}{W}
$$

### 7.3.2 접합 커패시턴스
![[Pasted image 20240616021418.png|300]]
$$
C'=\bigg\{\frac{e\epsilon_{s}N_{a}N_{d}}{2(V_{bi}+V_{R})(N_{a}+N_{d})}\bigg\}^{1 / 2}
=\frac{\epsilon_{s}}{W}
\; \text{[F/cm}^2]
$$

- 일방 접합 (One-sided Junction)
	$N_{a}\gg N_{d} \rightarrow \text{p}^{+}\text{n}$접합
	$W \approx x_{n}$
	$C' \approx \bigg\{\frac{e\epsilon_{s}N_{d}}{2(V_{bi}+V_{R})}\bigg\}^{1 / 2}$
$$
\left( \frac{1}{C'} \right)^{2}=\frac{2(V_{bi}+V_{R})}{e\epsilon_{s}N_{d}}
$$
➡ 선형적이다.

## 7.4 접합 항복

역바이어스 전압이 항복 전압에 도달하면 역바이어스 전류가 급격히 증가한다.

### 7.4.1 제너 효과 (Zener effect)

전도대와 가전자대가 가까워져 직접 터널링이 일어난다.

### 7.4.2 애벌런치 효과 (avalanche effect)
![[Pasted image 20240616023437.png|300]]
- 공간 전하 영역 속 캐리어가 전계로부터 에너지를 받고 원자의 전자와 충돌하여 전자-정공 쌍을 생성
-  생성 과정의 연쇄
- 지배적인 항복 메커니즘

p$^{+}$n 접합, $V_{R}\gg V_{bi}$ 가정:
$$
E_{\text{max}}=\frac{eN_{d}x_{n}}{\epsilon_{s}},\;x_{n}\approx\left\{ \frac{2\epsilon_{s}V_{R}}{e} \cdot \frac{1}{N_{d}} \right\}^{1 /2}
$$
$$
V_{B}=\frac{\epsilon_{s}E^{2}_{\text{crit}}}{2eN_{B}}
$$
- $V_{B}$: 항복 전압
- $E_{\text{crit}}$: 항복 지점에서의 $E_{\text{max}}$
- $N_{B}$: 일방 접합의 저 도핑 영역에 대한 도핑 농도


## 7.5 불균일하게(nonuniformly) 도핑된 접합
### 7.5.1 Linearly Graded Junction
![[Pasted image 20240616030315.png|300]]
### 7.5.2 Hyperabrupt Junction
$m<0$
p$^{+}$n$^{-}$n$^{+}$ 접합 
![[Pasted image 20240616030422.png|300]]
