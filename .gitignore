package com.adnisa.tubesAI;

import javax.swing.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class kalkulatorBMI extends JFrame{
    private JTextField beratTextField;
    private JTextField tinggiTextField;
    private JTextField BMITextField;
    private JButton hitungButton;
    private JPanel tubesBMI;
    private JLabel BodyMassIndexLabel;
    private JLabel beratBadanLabel;
    private JLabel tinggiBadanLabel;
    private JLabel BMILabel;
    private JLabel kategoriLabel;
    private JLabel jeniskelaminLabel;
    private JRadioButton lakiLakiRadioButton;
    private JRadioButton perempuanRadioButton;
    private JTextField idealtextField;
    private JLabel idealLabel;


    public kalkulatorBMI() {
        hitungButton.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                //buat variabel
                double berat, tinggi, bmi, meter, usia, amblk, ambp, ideallk, idealp;

                //ambil inputan text field
                berat = Double.parseDouble(beratTextField.getText());
                tinggi = Double.parseDouble(tinggiTextField.getText());
                //usia = Double.parseDouble((usiatextField.getText()));
                
                //hitung BMI
                meter = tinggi / 100;
                bmi = berat / (meter * meter);
                //hitung ideal
                ideallk = (tinggi - 100) - ((tinggi - 100) * 10/100);
                idealp = (tinggi - 100) - ((tinggi - 100) * 15/100);
                

                //taruh hasil BMI
                BMITextField.setText(String.valueOf(bmi));

                //taruh hasil ideal
                String ideal = new String();
                if (lakiLakiRadioButton.isSelected()) {
                    ideal = lakiLakiRadioButton.getText();
                    idealtextField.setText(String.valueOf(ideallk));
                }  else if (perempuanRadioButton.isSelected()) {
                    ideal = perempuanRadioButton.getText();
                    idealtextField.setText(String.valueOf(idealp));
                }

                //keterangan
                if (bmi < 18.5) {
                    JOptionPane.showMessageDialog(null, "Hasil perhitungan BMI menunjukkan bahwa anda Underweight");
                } else if (bmi <= 24.9) {
                    JOptionPane.showMessageDialog(null, "Hasil perhitungan BMI menunjukkan bahwa anda Normal Weight");
                } else if (bmi < 29.9) {
                    JOptionPane.showMessageDialog(null, "Hasil perhitungan BMI menunjukkan bahwa anda Overweight");
                    dispose();
                } else {
                    JOptionPane.showMessageDialog(null, "Hasil perhitungan BMI menunjukkan bahwa anda Obesitas");
                }
            }
        });
    }

    public static void main(String[] args) {
        JFrame frame = new JFrame("kalkulator BMI");
        frame.setContentPane(new kalkulatorBMI().tubesBMI);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.pack();
        frame.setVisible(true);
    }
}
