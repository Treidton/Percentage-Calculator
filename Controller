package percentage.app;

import java.net.URL;
import java.text.DecimalFormat;
import java.time.Instant;
import java.time.LocalDate;
import java.time.ZoneId;
import java.time.format.DateTimeFormatter;
import java.time.temporal.ChronoUnit;
import java.util.Date;
import java.util.ResourceBundle;
import javafx.event.ActionEvent;
import javafx.event.EventHandler;
import javafx.fxml.FXML;
import javafx.fxml.Initializable;
import javafx.scene.control.Alert;
import javafx.scene.control.Button;
import javafx.scene.control.DatePicker;
import javafx.scene.control.Label;

/**
 *
 * @author Tyler
 */


public class Controller implements Initializable {
    
@FXML
DatePicker dp_start;

@FXML
DatePicker dp_current;

@FXML
DatePicker dp_end;

@FXML
Button button_calculate;

@FXML
Button button_reset;

@FXML
Label l_start;

@FXML
Label l_current;

@FXML
Label l_end;

@FXML
Label l_total;

@FXML
Label l_complete;

@FXML
Label l_left;

@FXML
Label l_percentage;

@FXML
Label l_per, l_p, l_dl, l_dc, l_td, l_ed, l_cd, l_sd;




    @Override
    public void initialize(URL location, ResourceBundle resources) {
        String startS;
        String currentS, endS;
        
        DateTimeFormatter format = DateTimeFormatter.ofPattern("dd/MM/yyyy");    
        
        
        
        button_calculate.setOnAction(new EventHandler<ActionEvent>(){
       
       @Override
        public void handle(ActionEvent event){
            
       
           
        l_dl.setVisible(true);
        l_dc.setVisible(true);
        l_td.setVisible(true);
        l_ed.setVisible(true);
        l_cd.setVisible(true);
        l_sd.setVisible(true);
        l_total.setVisible(true);
        l_complete.setVisible(true);
        l_left.setVisible(true);
        l_percentage.setVisible(true);
        l_p.setVisible(true);
        l_per.setVisible(true);
        l_start.setVisible(true);
        l_current.setVisible(true);
        l_end.setVisible(true);

        
        
        LocalDate start = dp_start.getValue();
        LocalDate current = dp_current.getValue();
        LocalDate end = dp_end.getValue();
        
     
        
        l_start.setText(start.toString());
        l_current.setText(current.toString());
        l_end.setText(end.toString());
        
        long totalDays = ChronoUnit.DAYS.between(start, end);
        l_total.setText(totalDays + "");
        
        long completedDays = ChronoUnit.DAYS.between(start, current);
        l_complete.setText(completedDays + "");
        
        long daysLeft = ChronoUnit.DAYS.between(current, end);
        l_left.setText(daysLeft + "");
        
        DecimalFormat fmt = new DecimalFormat("#.#");
        double sf = (totalDays - daysLeft);
        double sds = (sf / totalDays) * 100;
        
        l_percentage.setText(fmt.format(sds) + "");
        l_p.setText("YOU HAVE COMPLETED");
        
            
        
        
    }
    
});
        button_reset.setOnAction(new EventHandler<ActionEvent>(){
       
       @Override
        public void handle(ActionEvent event){
        l_dl.setVisible(false);
        l_dc.setVisible(false);
        l_td.setVisible(false);
        l_ed.setVisible(false);
        l_cd.setVisible(false);
        l_sd.setVisible(false);
        l_total.setVisible(false);
        l_complete.setVisible(false);
        l_left.setVisible(false);
        l_percentage.setVisible(false);
        l_p.setVisible(false);
        l_per.setVisible(false);
        l_start.setVisible(false);
        l_current.setVisible(false);
        l_end.setVisible(false); 
        
        dp_start.setValue(null);
        dp_current.setValue(null);
        dp_end.setValue(null);
        l_start.setText("2001/01/01");
        l_current.setText("2001/01/01");
        l_end.setText("2001/01/01");
        l_total.setText("0");
        l_complete.setText("0");
        l_left.setText("0");
        l_percentage.setText("0");
        
        }
    });
        
        
    
}
}
