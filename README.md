# css-grid-system
CSS Grid System All Properties

display: grid;
grid-template-columns: repeat(2, 1fr);  ( px auto % can be used at same time )
grid-template-columns: 150px 40% auto 1fr .5fr; (fr means fraction)
grid-template-rows: 100px 130px 100px;


******Grid Gap******
grid-row-gap:30px;
grid-column-gap:10px;
grid-gap: 10px 10px;  (row value - column value) 
grid-gap: 10px; (row and column value)


*****Grid Positioning*****
grid-column: 1 / 2; ( Column start / Column end )
grid-row: 1 / 2; ( Row start / Row end )
grid-area: 1 / 1 / 2 / 2; ( row start / column start / row end / column end )

*****Grid Spanning*****
.box1 {
    grid-column: 1 / 3;  (start / end)
    grid-row: 1 / 3;     (start / end)
}    

*****Grid Area Naming*****
grid-template-areas: 
        "header header header"
        "menu menu menu"
        "box1 box2 sidebar"
        "content content sidebar"
        "footer footer footer";

.header {
    grid-area: header;
    background: hotpink;
}

.menu {
    grid-area: menu;
    background: orangered;
}


*****Min Max*****
.container2 {
    display: grid;
    grid-template-columns: max-content 1fr 1fr min-content;
    grid-template-rows: repeat(2, min-content); 
    grid-template-rows: repeat(2, minmax(150px, min-content));
}

*****Implicit and Explicit*****
.container3 {
    grid-auto-rows: 50px;
    grid-auto-flow: column;  (row is default value)
    grid-auto-columns: 80px;
}

*****Grid Item Alignment*****

.container4{
    align-items: center;  (Vertically)
    justify-items: end;   (Horizontally)
    align-self: center;  (Vertically)
    justify-self: end;   (Horizontally)
    place-items: center center;  (align-items  justify-items)
    place-self: center end; (align-self  justify-self)
}


Implicit: Things that decide browser. (Auto rows and columns)
Explicit:Things taht we decide ourself.


Order: Changes the order of items within the grid. Jitna order high grid will go to end.