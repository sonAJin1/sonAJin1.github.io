## [unity] Slider로 게이지 바 만들기



> ### Slider 생성방법

1. hierarchy View에 우클릭 후 UI -> Slider를 선택한다.

   ![2018_05_28_slider_01](/assets/img/2018_05_28_slider_01.png)

   ​

   ​

2. Slider Fill의 색을 원하는 색상으로 변경한다.

   ![2018_05_28_slider_02](/assets/img/2018_05_28_slider_02.png)

   ​

   ​


> ### C# 스크립트로 Slider 제어방법 (코드로 값변경)

1. Project의 Assets에 C# 스크립트를 생성한다.

   ![2018_05_28_slider_03](/assets/img/2018_05_28_slider_03.png)

   ​

2. 스페이스 바를 누르고 있으면 값이 증가하는 코드 작성 후 저장한다.

   ~~~c#
   using System.Collections;
   using System.Collections.Generic;
   using UnityEngine;
   using UnityEngine.UI;

   public class NewBehaviourScript : MonoBehaviour {

       public Slider healthBarSlider; // slider 호출
       public float maxvalue; // slider 최대값
      // public float BarValue;
         

   	// Use this for initialization
   	void Start () {
   		
   	}
   	
   	// Update is called once per frame
   	void Update () {
           healthBarSlider.maxValue = maxvalue; //호출한 slider의 최대값을 내가 만든 maxvalue 값으로 설정
         
           if(Input.GetKey(KeyCode.Space) == true) // 스페이스 바가 눌렸음을 인지하면
           {
               healthBarSlider.value += 10 * Time.deltaTime; // 프레임당 10씩 증가한다
               if (healthBarSlider.value > maxvalue) // slider값이 최대값을 초과하면
                   healthBarSlider.value = maxvalue; // sldier값을 최대값과 같게한다.
           }
   	}

       
   }

   ~~~
   ​

3. C# 스크립트를 hierarchy view에 있는 slider로 드래그해서 적용한다.

   ![2018_05_28_slider_04](/assets/img/2018_05_28_slider_04.png)

   ​

4. Inspector view의  script 부분의 Health Bar Slider에 hierarchy의 slide를 드래그해서 적용한다.

   ![2018_05_28_slider_05](/assets/img/2018_05_28_slider_05.png)

   ​

5. Maxvalue는 100으로 설정한다.

   ![2018_05_28_slider_06](/assets/img/2018_05_28_slider_06.png) 

   ​

6. Play 버튼을 클릭해서 스페이스 바를 누르면 게이지 바가 증가하는 것을 볼 수 있다.

   ![2018_05_28_slider_07](/assets/img/2018_05_28_slider_07.png)

   ​