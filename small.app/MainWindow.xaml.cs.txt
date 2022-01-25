using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;
using System.Threading;

namespace kma_video
{
    /// <summary>
    /// Interaktionslogik für MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }

        private void Grid_MouseDown(object sender, MouseButtonEventArgs e)
        {
            if (e.LeftButton == MouseButtonState.Pressed)
            {
                DragMove();
            }
        }

        private void Button_Click(object sender, RoutedEventArgs e)
        {
            App.Current.Shutdown();
        }

        private void Button_Click_Video(object sender, RoutedEventArgs e)
        {
            MessageBoxResult mbresult = MessageBox.Show("Sie sind gerade dabei 32.228 Schulen anzugreifen!\r\nDDoS Antacken werden in 10. Sekunden gestartet.", "Netzwerk", MessageBoxButton.OK, MessageBoxImage.Warning);
            if (MessageBoxResult.OK == mbresult)
            {
                Thread.Sleep(10000);
                MessageBox.Show("Sie haben 30.000 Schulen Aktiv angegriffen!\r\nTraffic: 1.5 Gbit's", "Netzwerk", MessageBoxButton.OK, MessageBoxImage.Information);
                Thread.Sleep(5000);
                System.Diagnostics.Process.Start("https://www.youtube.com/watch?v=PXqcHi2fkXI");
            }
        }

        private void Button_Click_App(object sender, RoutedEventArgs e)
        {
            MessageBox.Show("Um natürlich zu zeigen wie die App aufgebaut ist habe ich den Source Code zu Verfügung gestellt.", "Source Code", MessageBoxButton.YesNo, MessageBoxImage.Error);
            System.Diagnostics.Process.Start("");
        }
    }
}
