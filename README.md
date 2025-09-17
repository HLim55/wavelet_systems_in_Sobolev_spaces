## Wavelet_systems_in_Sobolev_spaces
Scrutinize every wavelet system in Sobolev spaces!

[9 Sep, 2025]

#[Meyer]Wavelets_and_Operators

- See Theorem 6 in Chp 2.7.
- 태초에 Meyer가 있었다.
- L2에서 r-regular MRA (V_0 space의 generator이자 scaling function \varphi의 r계 미분까지 모두 임의의 polynomial보다 빠른 decay를 가짐; see Definition 2 in p.21)를 생각하면 Sobolev space의 임의의 함수에 대해 그 함수를 V_j로의 projection시킨 것이 f로 수렴한다는 결과가 존재..
- 대충 cptly supported면서 적당히 smooth한 scaling function에 대한 얘기를 예시로 생각해줄 수 있을듯. 하지만 나는 여전히 approximation error가 궁금하다!!!!!!!

#[1997BastinLaubin]Compactly_supported_wavelets_in_Sobolev_Spaces

- 여기서는 기본적으로 Sobolev space에서 orthonormal basis가 되는 wavelet system을 Multiresolution Analysis (MRA)를 써서 construct하는 것으로 보임. 
- 은연중에 머릿속에서 Sobolev space에서 뭐든 다루려면 dual space를 무조건 고려해야하지 않나라고 생각해왔던 것 같은데, 이게 어쩌면 내가 L2가 아닌 다른 함수공간에 대해서는 거의 frame정도의 더 넉넉한 조건으로 내려가서 보고 있었기 때문에 생긴 편견이었을지도. 되짚어 생각해보면 orthonormal basis가 가능하다면, 즉 analyzer와 synthesizer가 완전히 동일한 함수라면, convergence만 잘 다뤄줄 수 있으면 굳이 dual공간을 들고와야 될 이유는 없을듯..
- 하지만 그래도 여전히 이 paper를 보면서 의아한 점은 approximation space V_j마다 scaling function \varphi^{(j)}를 bring한다는 점. 그게 얼마나 redundant한지, 아니면 그거라도 써서 이걸 해낸게 얼마나 대단한건지를 파악하려면 아직은 더 읽어봐야 할 듯. 이 논문의 처음이자 제일 큰 진입장벽은 이 부분. 그럼에도 불구하고 아마 Sobolev space에서의 MRA 첫 시도인 듯. 그 이후에도 잘 없는 것 같기도 하고. 

#[2009HanShen]Dual_wavelet_frames_and_Riesz_bases_in_Sobolev_Spaces

- 돌고돌아 다시 HanShen..
- Tight wavelet frame이 아니라 그냥 wavelet frame! 그리고 Riesz bases 결과! 진짜 개쩌는거긴한데. 근데 그렇기 때문에 dual을 찾기가 넘모 어려운 것... 존재성은 알지만 constructive하진 않았던걸로 기억..
아니 더 정확히는 어떤 system 두 개가 있고 그 각각 filter들이 있을 때 dual wavelet frame이 되는지 체크할 수 있는 충분조건이었던 걸로 기억...
- 그래서 UEP가 아니라 mixed extension principle(MEP) 활용
- 근데 이 결과 너무 notation heavy하고 좀 더 practical side로 쓰여있었던 것 같아서 좀 더 MRA의 approximation space와 detail space구조로 좀 더 읽어내봐야 될 필요가 있어보임.
그 때, [2010Ehler]The_multiresolution_structure_of_pairs_of_dual_wavelet_frames_for_a_pair_of_Sobolev_spaces가 도움이 될 것 같음. 나란히 놓고 읽어보기.

[11 Sep, 2025]

#[Hernandez,Weiss]A_first_course_on_wavelets

- See Chp 6 (Mainly, Chp 6.6, with Chp 5.1,2, and 6.1.2)
- 아니 애초에 wavelet characterization을 되짚어 다시 잘 생각해보면 그 inequality자체가 애초에 frame assumption이잖아? 라는 생각으로 
그러면 내가 이제까지 맨날 공부하던 함수공간을 wavelet coefficient로 characterize하는 것 자체가 wavelet frame을 주는 거 아니야? 하는 서늘한 생각으로 다시 back to the basic.
- 약간 처리를 해줘야 될 부분은 있지만 적어도 orthonormal basis에서 시작하면 frame (사실은 더 나아가서 다른 함수공간에서도 orthonormal basis까지도)으로 어느정도 고려해줄 수 있을듯 (적어도 Sobolev에서는 -- Hilbert space니까)
- 오늘 앞에 작업은 다 봐뒀으니까 Chp 6.6 툴들 의미생각하면서 자세히 읽어내면 될듯. 또 harmonic 딥하게 쓰이면 계산가능하단 것 이상의 의미를 읽어낼 수 있을지는 모르겠는데 그래도 다시 시도해봐야지 어떡해.
- Chp 6.6 이 사실은 [Meyer]Wavelets and Operators의 Chp 2.7. Theorem 6의 친절한 버전인거 같긴함
- 모쪼록 이거 보고나면, 이거 조건 활용해서 그대로 approximation error로 접근해보는 것도 방법일듯

[15 Sep, 2025]

#[1989Mallat]MRA_and_WOB_of_L2

- See Theorem 3
- 그토록 찾아 헤매던 approximation error에 관한 결과
- 근데 정확히 원하는 형태인지는 좀 더 체크해봐야됨. 생각보다 조금은 거리가 있는 것 같긴해서 원하는 것에서 얼마나 먼지 체크해봐야댐
- 그리고 wavelet system의 orthonormality에 엄청나게 depend하는 증명인 것 같아서 그거 들어내려면 쉽지 않을듯.