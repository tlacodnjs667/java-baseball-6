<h2>숫자 야구 게임 기능 정의</h2>

<ol>
	<li>게임 초기화 : 임의의 3자리 난수 생성
		- 사용자가 유추할 3자리 숫자를 생성하고, 이를 컴퓨터라는 클래스의 인스턴스 멤버의 멤버 변수로 초기화
	<li>입력
		<ol> 
			<li>게임 진행 시 비교할 사용자의 3자리 숫자 입력 받기.
				입력 시 조건은 다음과 같다 : 입력 받는 수는 서로 다른 3자리 수여야 하고, 각 자릿수의 범위는 1에서 9를 포함한 그 사이의 정수이다.
				위의 범위에서 벗어난 수를 입력 시 `IllegalArgumentException`가 발생하고 애플리케이션은 종료된다.
			<li>한 라운드가 끝나게 되었을 때, 사용자에게 게임 재시작 여부를 입력 받기.
				재시작을 나타내는 숫자는 1, 프로그램 종료를 의미하는 숫자는 2이다.
				이외의 수를 입력받거나, 정수가 아닌 수를 입력받았을 경우 `IllegalArgumentException`가 발생하고 애플리케이션은 종료된다.
		</ol>
	<li>게입 실행 순서
		<ol>
			<li>사용자가 유추하는 3자리수 입력 받음
			<li>컴퓨터가 생성한 임의의 3자리 난수와 사용자에게 입력받은 수를 비교
			<li>난수와 입력받은 수를 ArrayList에 담고 있으며, 각 자릿수와 값을 비교한다.
			<li>만약 난수와 입력받은 수의 값과 자릿수가 동일하지 않다면 해당 (1) ~ (3)의 과정 반복
			<li>만약 난수와 입력받은 수가 동일하다면, 해당 라운드를 종료하고 게임 재진행 여부를 입력받음
		</ol>
	<li>사용자가 입력한 재시작 여부에 따라 위 과정을 반복하거나, Application의 main 메서드를 종료한다. 	
</ol>

<h3>TODO : </h3>

<ol>
	<li style="text-decoration:underline dotted"> Computer class
	<ol>
		<li>3자리수의 난수를 생성하는 생성자로, 각 라운드마다 새로운 난수가 생성됨
		<li>유저의 리스트 아규먼트를 넘겨받아 해당 컴퓨터가 가지고 있는 3자리 난수와 비교하는 메서드
		<li>비교한 결과값을 가지로 해당 입력에 대한 상태 출력하는 메서드
	</ol>
	<li style="text-decoration:underline dotted"> User class
	: User의 입력을 관장하고, 입력 받은 수를 저장하는 클래스
	<ol>
		<li>유저가 유추하는 숫자를 입력받는 메서드
		<ul>조건은 다음과 같음.
			<li>3자리 정수일 것.
			<li>각 자리수의 값이 1에서 9 사이일 것.
		</ul>
		<li>게임의 재진행 여부를 입력받는 메서드
		<ul>조건은 다음과 같음.
			<li>입력값은 1이나 2일 것.
		</ul>
	</ol>
</ol>