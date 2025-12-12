math, physics, and design choices (short)
Math

Cubic Bézier formula:

𝐵
(
𝑡
)
=
(
1
−
𝑡
)
3
𝑃
0
+
3
(
1
−
𝑡
)
2
𝑡
𝑃
1
+
3
(
1
−
𝑡
)
𝑡
2
𝑃
2
+
𝑡
3
𝑃
3
B(t)=(1−t)
3
P
0
	​

+3(1−t)
2
tP
1
	​

+3(1−t)t
2
P
2
	​

+t
3
P
3
	​


Implemented directly in bezierPoint(t, p0, p1, p2, p3) (web) and bezierPoint (Swift).

Derivative:

𝐵
′
(
𝑡
)
=
3
(
1
−
𝑡
)
2
(
𝑃
1
−
𝑃
0
)
+
6
(
1
−
𝑡
)
𝑡
(
𝑃
2
−
𝑃
1
)
+
3
𝑡
2
(
𝑃
3
−
𝑃
2
)
B
′
(t)=3(1−t)
2
(P
1
	​

−P
0
	​

)+6(1−t)t(P
2
	​

−P
1
	​

)+3t
2
(P
3
	​

−P
2
	​

)

Used to compute tangent vectors; normalized and drawn as short lines to visualize direction.

Physics model

Spring-damper:

𝑎
=
−
𝑘
(
𝑥
−
𝑥
target
)
−
𝑐
𝑣
a=−k(x−x
target
	​

)−cv

Integrated using semi-implicit Euler:

𝑣
←
𝑣
+
𝑎
⋅
𝑑
𝑡
v←v+a⋅dt

𝑥
←
𝑥
+
𝑣
⋅
𝑑
𝑡
x←x+v⋅dt

Semi-implicit Euler chosen for simple stability compared to explicit Euler.

Parameters chosen to feel rope-like: k (stiffness) fairly large, damping moderate. Tweak to taste.

Design choices

Sample t with STEP = 0.01 for smoothness without heavy CPU cost.

Tangents drawn at intervals (not at every sample) for clarity.

Interaction:

Web: drag P1/P2; mouse influences when not dragging.

iOS: CoreMotion controls P1/P2 targets; optionally add touch drag for testing in simulator.

No external libraries; all math done explicitly.

How to run 
Web (quick)

Save bezier-spring.html to disk.

Open in Chrome/Firefox/Edge by double-click or File → Open.

Interact: drag inner control points or move mouse.
