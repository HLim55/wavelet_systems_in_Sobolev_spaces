## Wavelet_systems_in_Sobolev_spaces
Scrutinize every wavelet system in Sobolev spaces!

[9 Sep, 2025]

### [Meyer]Wavelets_and_Operators

- See Theorem 6 in Chp 2.7.
- 태초에 Meyer가 있었다.
- L2에서 r-regular MRA ($V_0$ space의 generator이자 scaling function $\varphi$의 r계 미분까지 모두 임의의 polynomial보다 빠른 decay를 가짐; see Definition 2 in p.21)를 생각하면 Sobolev space의 임의의 함수에 대해 그 함수를 $V_j$로의 projection시킨 것이 f로 수렴한다는 결과가 존재..
- 대충 cptly supported면서 적당히 smooth한 scaling function에 대한 얘기를 예시로 생각해줄 수 있을듯. 하지만 나는 여전히 approximation error가 궁금하다!!!!!!!

### [1997BastinLaubin]Compactly_supported_wavelets_in_Sobolev_Spaces

- 여기서는 기본적으로 Sobolev space에서 orthonormal basis가 되는 wavelet system을 Multiresolution Analysis (MRA)를 써서 construct하는 것으로 보임. 
- 은연중에 머릿속에서 Sobolev space에서 뭐든 다루려면 dual space를 무조건 고려해야하지 않나라고 생각해왔던 것 같은데, 이게 어쩌면 내가 $L^2$가 아닌 다른 함수공간에 대해서는 거의 frame정도의 더 넉넉한 조건으로 내려가서 보고 있었기 때문에 생긴 편견이었을지도. 되짚어 생각해보면 orthonormal basis가 가능하다면, 즉 analyzer와 synthesizer가 완전히 동일한 함수라면, convergence만 잘 다뤄줄 수 있으면 굳이 dual공간을 들고와야 될 이유는 없을듯..
- 하지만 그래도 여전히 이 paper를 보면서 의아한 점은 approximation space $V_j$마다 scaling function $\varphi^{(j)}$를 bring한다는 점. 그게 얼마나 redundant한지, 아니면 그거라도 써서 이걸 해낸게 얼마나 대단한건지를 파악하려면 아직은 더 읽어봐야 할 듯. 이 논문의 처음이자 제일 큰 진입장벽은 이 부분. 그럼에도 불구하고 아마 Sobolev space에서의 MRA 첫 시도인 듯. 그 이후에도 잘 없는 것 같기도 하고. 

### [2009HanShen]Dual_wavelet_frames_and_Riesz_bases_in_Sobolev_Spaces

- 돌고돌아 다시 HanShen..
- Tight wavelet frame이 아니라 그냥 wavelet frame! 그리고 Riesz bases 결과! 진짜 개쩌는거긴한데. 근데 그렇기 때문에 dual을 찾기가 넘모 어려운 것... 존재성은 알지만 constructive하진 않았던걸로 기억..
아니 더 정확히는 어떤 system 두 개가 있고 그 각각 filter들이 있을 때 dual wavelet frame이 되는지 체크할 수 있는 충분조건이었던 걸로 기억...
- 그래서 UEP가 아니라 mixed extension principle(MEP) 활용
- 근데 이 결과 너무 notation heavy하고 좀 더 practical side로 쓰여있었던 것 같아서 좀 더 MRA의 approximation space와 detail space구조로 좀 더 읽어내봐야 될 필요가 있어보임.
그 때, [2010Ehler]The_multiresolution_structure_of_pairs_of_dual_wavelet_frames_for_a_pair_of_Sobolev_spaces가 도움이 될 것 같음. 나란히 놓고 읽어보기.

[11 Sep, 2025]

### [Hernandez,Weiss]A_first_course_on_wavelets

- See Chp 6 (Mainly, Chp 6.6, with Chp 5.1,2, and 6.1.2)
- 아니 애초에 wavelet characterization을 되짚어 다시 잘 생각해보면 그 inequality자체가 애초에 frame assumption이잖아? 라는 생각으로 
그러면 내가 이제까지 맨날 공부하던 함수공간을 wavelet coefficient로 characterize하는 것 자체가 wavelet frame을 주는 거 아니야? 하는 서늘한 생각으로 다시 back to the basic.
- 약간 처리를 해줘야 될 부분은 있지만 적어도 orthonormal basis에서 시작하면 frame (사실은 더 나아가서 다른 함수공간에서도 orthonormal basis까지도)으로 어느정도 고려해줄 수 있을듯 (적어도 Sobolev에서는 -- Hilbert space니까)
- 오늘 앞에 작업은 다 봐뒀으니까 Chp 6.6 툴들 의미생각하면서 자세히 읽어내면 될듯. 또 harmonic 딥하게 쓰이면 계산가능하단 것 이상의 의미를 읽어낼 수 있을지는 모르겠는데 그래도 다시 시도해봐야지 어떡해.
- Chp 6.6 이 사실은 [Meyer]Wavelets and Operators의 Chp 2.7. Theorem 6의 친절한 버전인거 같긴함
- 모쪼록 이거 보고나면, 이거 조건 활용해서 그대로 approximation error로 접근해보는 것도 방법일듯

[15 Sep, 2025]

### [1989Mallat]MRA_and_WOB_of_L2

- See Theorem 3
- 그토록 찾아 헤매던 approximation error에 관한 결과
- 근데 정확히 원하는 형태인지는 좀 더 체크해봐야됨. 생각보다 조금은 거리가 있는 것 같긴해서 원하는 것에서 얼마나 먼지 체크해봐야댐<br>
=> 일단은 원하는 error estimate은 맞음.. [18 Sep, 2025]<br>
For $f \in H^s$, there exists \(C>0\) such that $\lVert f - P_j f \rVert_{L^2}^2 \leq C 2^{-2js}$ for every $j \in \mathbb{Z}$. 
- 그리고 wavelet system의 orthonormality에 엄청나게 depend하는 증명인 것 같아서 그거 들어내려면 쉽지 않을듯. <br>
[18 Sep, 2025]
- 결국엔 Thm3 이전에 나오는 Sobolev characterization으로부터 MRA로 연결해서 $V_j$ space의 error estimation 측정할 수 있게 해주는 결과였음 
- 그래서 다시 [HW]A first course on wavelets에 있는 Sobolev characterization 주는 충분 조건 살펴봤는데 그게 또 묘하데.... 전반적으로 decay 조건은 약하게 걸어도 되는데 미분 하나가 더 필요하고 원함수의 decay를 좀 세게 걸어주면 된다는데 그냥 어떻게 조립하냐의 문제 같기는 해서 체크해보면 될 듯. 그건 그냥 취향이든 필요한 함수에 따라 뚝딱뚝딱 만들어주면 되는 것 같고, 문제는... orthonormality를 어떻게 약화시킬 것인지일듯.. 그러면서도 여전히 $V_j$와 $W_j$가 충분히 나이스한 관계를 가지도록 설계 어떻게 하지...? 

[23 Sep, 2025]

### [2010Ehler]The_multiresolution_structure_of_pairs_of_dual_wavelet_frames_for_a_pair_of_Sobolev_spaces

- 앞선 Mallat의 Thm3에 따르면 결국 MRA hierarchy, 즉, $V_j \subset V_{j+1}$ 과 $V_j \oplus W_j = V_{j+1}$, 이 많은 것들을 자연스럽게 주는데 그 시작이 **scaling relation**과 **scaling function의** $V_0$ **에서의 orthonormality**인데, 우리가 orthonormality를 약화시켜서, tight wavelet frame이든 dual frames든 그 관련된 MRA space들 ($V_j, W_j$) 중 어떤 공간이 남고 각 공간의 관계가 어떻게 되는지도 모르고 있는 것 같아서 그 것에 대한 파악이 우선이라는 생각이 듬.<br>
그 공간들이 있어야 projection도 하고 error estimate도 할테니까... <br>
=> 그래서 일단 [2010Ehler]로 시작. [2008KimKimLim] paper에서 UEP로 부터 만들어지는 모든 TWF에서는 $W_0 = V_1$가 된다는 것을 보였다고 하고 그 결과의 확장이라고 함. 넘나 충격적..... 둘 다 자세히 읽어봐야될 것 같음. 일단 이 페이퍼 언어가 굉장히 친숙해서 그게 정말 좋음.

[25 Sep, 2025]

### [2008KimKimLim]Internal_structure_of_the_MRA_defined_by_the_UEP

- See Theorem 1.2.
- 핵심은 **UEP로 부터 만들어진 *거의 모든* TWF은 $W_0 = V_1$가 된다** <br>
제외되는 경우는 *if there exists an highpass filter* $m_j$ *such that other highpass filters* $m_i$ *can be written by* $m_i = \lambda_i m_j$, <br>
즉, 하나의 하이패스 필터의 constant multiple로 다른 highpass filter를 모두 적어낼 수 있는 그런 필터가 존재하지 않는, UEP를 만족하는, TWF은 $W_0 = V_1$을 만족할 수 밖에 없다는 결과.
- $W_0=V_1$이 될 때 임의의 $j$에 대해서 어떤 관계를 만족하는지까지 체크해보고 싶긴 함. $V_0=\{0\}$이 될 수 밖에 없다는걸까?<br>
=> **$V_j$와 $W_j$와의 관계를 좀 더 파봐야지 projection하는 것에서 잘 나눠질 수 있을거라 이걸 잘 알아야될 듯.** 근데 사실 꼭 이 paper로 볼 필요는 없음. Ehler로 봐도 됨.
- 그럼에도 불구하고 Shift-invariant space $S:=\mathcal{S}(\Phi)$와 그 것의 fiber $S_{\Vert x} := \{(\widehat{f}(x +k))_{k \in \mathbb{Z}^d}: f \in S\}$와 spectrum $\sigma(S) := \{x \in \mathbb{T}^d : S_{||x} \not= \{0\} \}$를 처음으로 마음으로 받아들일 수 있었다. <br>
=> 구체적으로 말하자면 shift invariant space에서 fiber와 spectrum의 쓸모?<br>
=> shift-invariant space에서는 $f \in S \Rightarrow T_k f \in S$이기 때문에 $\widehat{f} \in \widehat{S} \Rightarrow \widehat{f} e^{-2\pi i k \cdot \xi} \in \widehat{S}$가 됨. 즉, $\widehat{S}$가 modulation $e^{-2\pi i k \cdot \xi}$에 대해 닫혀있음.<br>
그래서 fiber를 정의할 때 $(\widehat{f}(\xi + k))_{k \in \mathbb{Z}^d}$, $\xi \in \mathbb{T}^d$,만을 조사하면 modulation을 통해 shift-invariant space의 함수를 모두 복구할 수 있게 됨. <br>
뭐 그 의미만 있는 건 아니지만 나는 이러한 이유로 이걸 보는 의미가 있겠다는 의미를 스스로 챙길 수 있었음. <br>
원래 $\mathbb{R}^d$의 것들을 그냥 와장창 기억했다면 그걸 분할해서 fiber로 의미를 부여하게하는? 그정도의 느낌.<br>
그래서 그러한 fiber의 정의대로라면 spectrum은 말하자면 nontrivial한(0이 아닌) $x \in \mathbb{T}^d$점들을 모아놓은 의미있는 점들의 집합 같은 느낌. 재밌다재미따

[14 Oct, 2025]

### [Cohen]Numerical Analysis of Wavelet Methods

- See Corollary 3.4.1 with $p = q_1 = q_2 = 2$.
- 찐찐찐 원하는 결과 찾음! 이전 Mallat의 결과는 error estimate을 L2로 하는 반면 이건 찐 Sobolev norm으로 잼:

$\lVert f - P_j f \rVert_{W^{s,2}} \leq 2^{-j(t-s)} \lVert f \rVert_{W^{t,2}}.$
- 보통 **Jackson-type**의 projection error estimation이라고 부르는 듯..