*COSTUME METHODE

v 1.2.0
2016-2019
--
Mini library give a bestiary shape or stuff to draw , in 2D or 3D

When use pass a float angle, that must be in radians -PI to PI

Ypu can pas the position and size with the class vec,
vec2 or vec3, if you'r are in Processing 2D and use vec3, no matter Processing understand and only use the component 'x' and 'y' of your vec

--
To choice the shape use method costume_rope()
to change the aspect like fill, stroke or strokeWeight use aspect_rope();
--






*LINE 2D


*void line2()

void line2D(vec2 p1, vec2 p2, boolean aa_is, boolean update_pix_is, PGraphics pg);

void line2D(vec2 p1, vec2 p2, boolean aa_is , boolean update_pix_is);

void line2D(float x1, float y1, float x2, float y2, boolean aa_is, boolean update_pix_is);

void line2D(float x1, float y1, float x2, float y2, boolean aa_is, boolean update_pix_is, PGraphics pg);

>arg position, define the first and the last point of your line
vec2 p1, p2

float x1,y1 and x2,y2 
>arg boolean as_is
define if your line use antialiasing or not

>arg boolean update_pis_is
define if the methode must use the internal method PGraphics.loadPixels() and PGraphics.updatePixels()

>arg PGraphics pg
use to pass a specific render context.

*void alpha_line2D()


alpha_line2D(float entry, float exit);
>define the alpha evolution between the first and the point, the argument must be normal from 0 to 1



Note: with those methods you can use method
void colour(int... color argument);
>useful to create a line with different colour.

void tempo(float... argument);
>useful to define the size of the different colour use on the line, you can create adash colour for example



*echoes with R_Line2D



R_Line2D line2D_echo_loop(R_Line2D line, R_Line2D [] walls, ArrayList<R_Line2D> list, float offset, float angle_echo, boolean go_return_is);
>return the rest of line after this one meet any wall

R_Line2D line is the main line live in the wall envirronment

R_Line2D [] walls define the list of walls of the environment

ArrayList<R_Line2D> list when the line is cut after a wall meeting the line before the meeting is add to this list, becareful is not the rest line.

float offset is use to make an offset withe rest of line

float angle_echo by default the the rest go in the revese way. It's possible the modify with this arg

boolean go_return_is useful to decide than all the restes start from the opposite wall.























*method COSTUME


*main

when the targeting costume is a pixel few possibility is no more available to use, like move in 3D, change thickness...because for pixel the methode set(x,y,c) from Processing is used, see Processing method.

void costume(float x, float y, float sx, float sy, Costume costume);

void costume(float x, float y, float z, float sx, float sy, Costume costume);

void costume(float x, float y, float z, float sx, float sy, float sz, Costume costume);

void costume(vec pos, vec size, float angle, vec3 dir, Costume costume);

void costume(vec pos, vec size, vec3 dir, Costume costume);

void costume(vec pos, int size, int Costume costume);

void costume(vec pos, vec size, int Costume costume);

// with other PGraphics
void costume(float x, float y, float sx, float sy, Costume costume, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, Costume costume, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, float sz, Costume costume, PGraphics pg);

void costume(vec pos, vec size, float angle, vec3 dir, Costume costume, PGraphics pg);

void costume(vec pos, vec size, vec3 dir, Costume costume, PGraphics pg);

void costume(vec pos, int size, int Costume costume, PGraphics pg);

void costume(vec pos, vec size, int Costume costume, PGraphics pg);

*method by id costume

void costume(float x, float y, float sx, float sy, int which);

void costume(float x, float y, float z, float sx, float sy, int which);

void costume(float x, float y, float z, float sx, float sy, float sz, int which);

void costume(vec pos, vec size, float angle, vec3 dir, int which);

void costume(vec pos, vec size, vec3 dir, int which);

void costume(vec pos, int size, int which);

void costume(vec pos, vec size, int which);

// with other PGraphics
void costume(float x, float y, float sx, float sy, int which, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, int which, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, float sz, int which, PGraphics pg);

void costume(vec pos, vec size, float angle, vec3 dir, int which, PGraphics pg);

void costume(vec pos, vec size, vec3 dir, int which, PGraphics pg);

void costume(vec pos, int size, int which, PGraphics pg);

void costume(vec pos, vec size, int which, PGraphics pg);

*Method String

void costume(float x, float y, float sx, float sy, String sentence);

void costume(float x, float y, float z, float sx, float sy, String sentence);

void costume(float x, float y, float z, float sx, float sy, float sz, String sentence);

void costume(vec pos, int size, float angle, String sentence);

void costume(vec2pos, vec size, float angle, String sentence);

void costume(vec pos, int size, String sentence);

void costume(vec pos, vec size, String sentence);

// with other PGraphics
void costume(float x, float y, float sx, float sy, String sentence, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, String sentence, PGraphics pg);

void costume(float x, float y, float z, float sx, float sy, float sz, String sentence, PGraphics pg);

void costume(vec pos, int size, float angle, String sentence, PGraphics pg);

void costume(vec2pos, vec size, float angle, String sentence, PGraphics pg);

void costume(vec pos, int size, String sentence, PGraphics pg);

void costume(vec pos, vec size, String sentence, PGraphics pg);







*List

void print_list_costume() ;
> return all the Integer constant ID, the name and the type of renderer.










*Text

void costume_text(String s) ;
>use to set the text

*Costume available

costumes_size() ;
>return the quantity of costumes available.


*ID costume

int get_costume(int target)
>return ID of the costume at this rank, if this one don't exist, that return 0. 0 is ID of 'point'


*rotate

void costume_rotate_x();
> give authorization to raotate

void costume_rotate_y();
> give authorization to raotate

void costume_rotate_z();
> give authorization to raotate

void costume_rotate(vec rotate);
> pass value for rotation

void costume_rotate(vec rotate, PGraphics other);
> pass value for rotation






















*ASPECT

void aspect_is(boolean fill_is, boolean stroke_is, boolean alpha_is);

void init_bool_aspect();

void aspect(int fill, int stroke, float thickness);

void aspect(int fill, int stroke, float thickness, PGraphics other);

void aspect(vec fill, vec stroke, float thickness);

void aspect(vec fill, vec stroke, float thickness, PGraphics other);


float get_fill_rope();
>return the fill component

float get_stroke_rope();
>return the stroke component

float get_thickness_rope();
>return the strokeWeight / thickness component





*RATIO SIZE

void set_ratio_costume_size(value);
>it's opssible to set the ratio size, to change multiply the size of all elements,
actullly available only for the CROSS_BOX_2_ROPE et CROSS_BOX_3_ROPE










*SHAPE CATALOGUE


STAR
--
void star(vec position, vec size);

void star(vec position, vec size, PGraphics other);

void star_3D_is(boolean is_3D);

void star_summits(int summits);

void star_angle(float angle);

void star_ratio(float... ratio);


star argument
--
>Pos, you can send a 'vec2' or 'vec3'
>Size, you can use 'int' or 'vec2', in the 'int' case the value is the same for the width and height
>Summits is the quantity of the higher summits of your star, the num of star points is summits * 2
>angle, in the rotation angle of the star in radians.
>the ratio is the 'raidus' or 'size' multiplicator to make difference on the higher or lower points, note you can use a sequence to make something weird like a compass : 



CROSS
--
void cross_rect(ivec2 pos, int thickness, int radius);

void cross_box_2(vec2 size,float ratio);

void cross_box_3(vec3 size,float ratio);

void cross_rect(ivec2 pos, int thickness, int radius, PGraphics other);

void cross_box_2(vec2 size,float ratio, PGraphics other);

void cross_box_3(vec3 size,float ratio, PGraphics other);


VIRUS
--
void virus(vec pos, vec size, int node, int num) ;

void virus(vec pos, vec size, int node, int num, float angle)  ;

void virus(vec pos, vec size, int node, int num, int speed) ;

void virus(vec pos, vec size, int node, int num, int speed_mutation, float angle, int close) ;



FLOWER
--
void flower(vec pos, int diam, int petals_num);

void flower(vec pos, int diam, int petals_num, PGraphics other);

void flower_wind(vec2 petal_left, float strength_left, vec2 petal_right, float strength_right);

void flower_static(vec2 petal_left, float strength_left, vec2 petal_right, float strength_right);


