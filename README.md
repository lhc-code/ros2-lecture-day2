# my_first_ros_rclpy_pkg — ROS2 rclpy Hello World (완성본)

동아대학교 KIM Lab / ROS 2 프로그래밍 기초(Python) 2일차 3~4차시 실습용 완성 패키지입니다.

## 📁 구조
```
my_first_ros_rclpy_pkg/
├── my_first_ros_rclpy_pkg/
│   ├── __init__.py
│   ├── helloworld_publisher.py
│   └── helloworld_subscriber.py
├── resource/
│   └── my_first_ros_rclpy_pkg
├── test/
│   ├── test_copyright.py
│   ├── test_flake8.py
│   └── test_pep257.py
├── package.xml
├── setup.cfg
└── setup.py   (entry_points 완성됨)
```

## 🚀 A6000 서버 배포 방법

### 방법 A — git clone (추천)
```bash
cd ~/robot_ws/src/
git clone <레포_URL> my_first_ros_rclpy_pkg
cd ~/robot_ws
colcon build --symlink-install --packages-select my_first_ros_rclpy_pkg
. ~/robot_ws/install/local_setup.bash
```

### 방법 B — 파일만 복사 (git 안 쓸 경우)
1. 이 폴더 전체를 `~/robot_ws/src/my_first_ros_rclpy_pkg`로 복사
2. 위와 동일하게 `colcon build` → `local_setup.bash`

## 🧑‍🏫 강의 운영 팁
- **학생용 배포본**: `setup.py`의 `entry_points` 안 리스트를 비워서(`[]`) 학생이 직접 채우게 하는 "실습용 버전"과, 지금 이 "정답 버전"을 **두 개 브랜치**(`start` / `solution`)로 관리하면 편합니다.
- **클립보드 씹힘 방지**: 학생들에게 이 레포를 미리 `git clone` 시켜두면, 코드 타이핑/붙여넣기 문제 없이 바로 `colcon build`부터 시작 가능합니다.
- 실행 확인:
```bash
ros2 run my_first_ros_rclpy_pkg helloworld_publisher
ros2 run my_first_ros_rclpy_pkg helloworld_subscriber
```
