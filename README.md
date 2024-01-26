//----------------------------------------------------------------------------------------------------------------------
// Creating a bird Author: Estefani Rivera
//
//----------------------------------------------------------------------------------------------------------------------

import javafx.application.Application;
import javafx.stage.Stage;
import javafx.scene.Group;
import javafx.scene.Scene;
import javafx.scene.paint.Color;
import javafx.scene.shape.*;

public class Bird extends Application
{

    //------------------------------------------------------------------------------------------------------------------
    // Presents a bird scene.
    //--------------------------------------------------------------------------------------------------------------------


    public void start(Stage primaryStage) {


        Ellipse body = new Ellipse(80, 240, 100, 50);
        body.setFill(Color.BLUE);


        Ellipse peak = new Ellipse(30, 170, 60,11);
        peak.setFill(Color.ORANGERED);


        Circle head = new Circle(37, 175, 53);
        head.setFill(Color.BLUE);


        Ellipse tail = new Ellipse(180, 235, 10, 7);
        tail.setFill(Color.BLUE);
        tail.setRotate(10);


        Ellipse wing = new Ellipse(90,220,60,6);
        wing.setFill(Color.DARKBLUE);


        Circle Eye = new Circle(30, 160, 6);
        Eye.setFill(Color.BLACK);


        Line LeftLA = new Line(115, 290, 117,310);
        LeftLA.setStrokeWidth(7);
        Line RightLA = new Line(112, 305, 115, 290);
        RightLA.setStrokeWidth(7);


        Group Bird= new Group(body,peak, head, tail,wing,Eye, LeftLA, RightLA);
        Bird.setTranslateX(90);
        Bird.setTranslateY(60);


        Circle sun = new Circle(50, 50, 40);
        sun.setFill(Color.YELLOW);


        Rectangle ground = new Rectangle(0, 360, 510, 110);
        ground.setFill(Color.FORESTGREEN);

        Rectangle Tree = new Rectangle(379,80,35,500);
        Tree.setFill(Color.BROWN);
        Circle leaves1 = new Circle(400,75,80);
        leaves1.setFill(Color.DARKGREEN);

        Circle leaves2 = new Circle(350,130,85);
        leaves2.setFill(Color.DARKGREEN);

        Circle leaves3 = new Circle(450,132,85);
        leaves3.setFill(Color.DARKGREEN);

        Ellipse pond = new Ellipse (430,430,450,30);
        pond.setFill(Color.CORNFLOWERBLUE);

        Group root = new Group(ground,Bird,sun,Tree,leaves1,leaves2,leaves3,pond);
        Scene scene = new Scene(root, 500, 450, Color.LIGHTBLUE);

        primaryStage.setTitle("Bird");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

}
// Created a scene of a cute bird,enjoying a nice day outside.
// The slides guide me to create this project.
// Java programming for the first time.

