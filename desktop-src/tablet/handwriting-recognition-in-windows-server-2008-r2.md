---
description: Windows Server 2008 R2 bietet Unterstützung für die Server seitige Handschrifterkennung für Windows. In diesem Thema wird beschrieben, wie Sie die Handschrift in Windows Server 2008 R2 erkennen.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Handschrifterkennung in Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039805"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Handschrifterkennung in Windows Server 2008 R2

Windows Server 2008 R2 unterstützt die Server seitige Handschrifterkennung. Die serverseitige Erkennung ermöglicht einem Server, Inhalte aus Stift Eingaben auf Webseiten zu erkennen. Dies ist besonders nützlich, wenn Benutzer in einem Netzwerk Begriffe angeben, die mit einem benutzerdefinierten Wörterbuch interpretiert werden. Wenn Sie z. b. eine medizinische Anwendung haben, die eine Server Datenbank für Patientennamen abgefragt hat, könnten diese Namen einer anderen Datenbank hinzugefügt werden, auf die übergreifende Verweise aus einem handschriftlichen Silverlight-Formular verwiesen wird.

## <a name="set-up-your-server-for-server-side-recognition"></a>Einrichten des Servers für die Server-Side Erkennung

Die folgenden Schritte müssen befolgt werden, um die serverseitige Erkennung einzurichten.

- Installieren von Freihand-und Handschriftdienste
- Installieren der Unterstützung für Webserver (IIS) und Anwendungs Server
- Aktivieren der Desktop Darstellung-Rolle
- Starten Sie den Tablet PC-Eingabe Dienst.

### <a name="install-ink-and-handwriting-services"></a>Installieren von Freihand-und Handschriftdienste

Öffnen Sie zum Installieren der Freihand-und Handschrift Dienste den Server-Manager, indem Sie in der Schnellstartleiste auf das Symbol Server-Manager klicken. Klicken Sie im Menü **Features** auf **Features hinzufügen**. Stellen Sie sicher, dass Sie das Kontrollkästchen **Freihand-und Handschriftdienste** aktivieren. In der folgenden Abbildung wird das Dialogfeld **Features auswählen** angezeigt, in dem **Freihand-und Handschriftdienste** ausgewählt ist.

![Dialogfeld "Features auswählen" mit aktivierten Kontrollkästchen für frei Hand Eingabe und Handschrift](images/setup-server-1-ink-and-handwriting.png)<br/>
*Dialogfeld "Features auswählen" mit aktivierten Kontrollkästchen für frei Hand Eingabe und Handschrift*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Installationsunterstützung für Webserver (IIS) und Anwendungs Server

Öffnen Sie den Server-Manager wie im ersten Schritt. Als nächstes müssen Sie die Rollen "Webserver (IIS)" und "Anwendungs Server" hinzufügen. Klicken Sie im Menü **Rollen** auf **Rollen hinzufügen**. Der Assistent zum Hinzufügen von Rollen wird angezeigt. Klicken Sie auf **Weiter**. Stellen Sie sicher, dass **Anwendungs Server** und **Webserver (IIS)** ausgewählt sind. In der folgenden Abbildung wird das Dialogfeld **Server Rollen auswählen** angezeigt, in dem die Rollen **Webserver (IIS)** und **Anwendungs Server** ausgewählt sind.

![Dialogfeld "Server Rollen auswählen", bei dem Webserver (IIS) und Anwendungsserver Rollen ausgewählt sind](images/setup-server-2-select-server-roles.png)<br/>
*Dialogfeld "Server Rollen auswählen", bei dem Webserver (IIS) und Anwendungsserver Rollen ausgewählt sind*

Wenn Sie den **Anwendungs Server** auswählen, werden Sie aufgefordert, das ASP.NET Framework zu installieren. Klicken Sie auf die Schaltfläche **erforderliche Features hinzufügen** . Nachdem Sie auf " **weiter**" klicken, wird ein Übersichts Dialogfeld angezeigt. Klicken Sie auf **weiter**. Das Dialogfeld **Rollen Dienste auswählen** sollte jetzt verfügbar sein. Stellen Sie sicher, dass **Webserver (IIS)** ausgewählt ist. In der folgenden Abbildung wird das Dialogfeld **Rollen Dienste auswählen** mit aktiviertem Webserver (IIS) angezeigt.

![Dialogfeld "Rollen Dienste auswählen" mit aktiviertem Webserver (IIS)](images/setup-server-3-select-role-services.png)<br/>
*Dialogfeld "Rollen Dienste auswählen" mit aktiviertem Webserver (IIS)*

Klicken Sie auf **Weiter**. Ein Übersichts Dialogfeld wird angezeigt. Klicken Sie erneut auf **weiter** . Ihnen wird nun eine Seite angezeigt, auf der Sie Optionen für Rollen für Webserver (IIS) bereitstellen. Klicken Sie auf **Weiter**. Auf der nächsten Seite wird die Schaltfläche " **Installieren** " aktiviert. Klicken Sie auf **Installieren** , und installieren Sie die Unterstützung für Webserver (IIS) und Anwendungs Server.

### <a name="enable-the-desktop-experience-role"></a>Aktivieren der Desktop Darstellung-Rolle

Um die Desktop Darstellung zu aktivieren, klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Server-Manager**. Wählen Sie **Dienste hinzufügen** und dann den **Desktop Darstellung-** Dienst aus. In der folgenden Abbildung wird das Dialogfeld **Features auswählen** angezeigt, in dem das Element Desktop Darstellung installiert ist.

![Dialogfeld "Features auswählen" mit ausgewähltem Desktop Darstellung-Dienst](images/setup-server-4-desktop-experience.png)<br/>
*Dialogfeld "Features auswählen" mit ausgewähltem Desktop Darstellung-Dienst*

Klicken Sie auf **weiter** , um die Desktop Darstellung zu installieren.

### <a name="start-the-tablet-service"></a>Starten des Tablet-Dienstanbieter

Nachdem Sie den Desktop Erfahrungs Dienst installiert haben, wird der Tablet PC-Eingabe Dienst im Menü **Dienste** angezeigt. Um auf das Menü **Dienste** zuzugreifen, klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Dienste**. Klicken Sie mit der rechten Maustaste auf **Tablet PC Input Service** , und klicken Sie dann auf **starten**. Die folgende Abbildung zeigt das Menü **Dienste** , in dem der Tablet PC-Eingabe Dienst gestartet wurde.

![Menü "Dienste" mit Start des Tablet PC-Eingabe Diensts](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menü "Dienste" mit Start des Tablet PC-Eingabe Diensts*

## <a name="performing-server-side-recognition-using-silverlight"></a>Durchführen Server-Side Erkennung mithilfe von Silverlight

In diesem Abschnitt wird gezeigt, wie eine Webanwendung erstellt wird, die Silverlight zum Erfassen von Handschrift Eingaben verwendet. Führen Sie die folgenden Schritte aus, um die Erkennung in Visual Studio 2008 zu programmieren.

- Installieren und aktualisieren Sie Visual Studio 2008, um die Unterstützung für Silverlight hinzuzufügen.
- Erstellen Sie ein neues Silverlight-Projekt in Visual Studio 2008.
- Fügen Sie dem Projekt die erforderlichen Dienst Verweise hinzu.
- Erstellen Sie einen Silverlight-WCF-Dienst für die frei Handerkennung.
- Fügen Sie dem Client Projekt den Dienst Verweis hinzu.
- Fügen Sie die InkCollector-Klasse dem InkRecognition-Projekt hinzu.
- Entfernen von sicheren Transport Direktiven aus der Client Konfiguration

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Installieren und Aktualisieren von Visual Studio 2008 zum Hinzufügen von Unterstützung für Silverlight

Bevor Sie beginnen, müssen Sie die folgenden Schritte auf Ihrem Windows Server 2008 R2-Server ausführen.

- Installieren Sie Visual Studio 2008.
- Installieren Sie [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).
- Installieren Sie das [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).

Nachdem Sie diese Anwendungen und Updates installiert haben, können Sie die serverseitige Erkennungs-Webanwendung erstellen.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Erstellen eines neuen Silverlight-Webprojekts in Visual Studio 2008

Klicken Sie im Menü **Datei** auf **Neues Projekt**. Wählen Sie die Vorlage Silverlight-Anwendung aus der Liste Visual C- \# Projekt aus. Nennen Sie Ihr Projekt InkRecognition, und klicken Sie auf **OK**. Die folgende Abbildung zeigt das \# ausgewählte C Silverlight-Projekt mit dem Namen InkRecognition.

![c \# Silverlight-Projekt mit dem Namen "InkRecognition" ausgewählt](images/project-1-new-project.png)<br/>
*c \# Silverlight-Projekt mit dem Namen "InkRecognition" ausgewählt*

Nachdem Sie auf **OK** geklickt haben, werden Sie in einem Dialogfeld aufgefordert, dem Projekt eine Silverlight-Anwendung hinzuzufügen. Wählen Sie **ein neues ASP.NET-Webprojekt zur Projekt Mappe hinzufügen aus, um Silverlight zu hosten,** **und klicken Sie** In der folgenden Abbildung wird gezeigt, wie Sie das Beispiel Projekt einrichten, bevor Sie auf **OK** klicken.

![Dialog Feld mit der Aufforderung zum Hinzufügen einer Silverlight-Anwendung zu einem Projekt](images/project-2-add-a-new-aspnetproject.png)<br/>
*Dialog Feld mit der Aufforderung zum Hinzufügen einer Silverlight-Anwendung zu einem Projekt*

### <a name="add-the-necessary-service-references-to-your-project"></a>Fügen Sie dem Projekt die erforderlichen Dienst Verweise hinzu.

Nun verfügen Sie über das generische Silverlight-Client Projekt (InkRecognition) mit einem Webprojekt (InkRecognition. Web), das in Ihrer Lösung eingerichtet ist. Das Projekt wird mit "page. XAML" und "default. aspx" geöffnet. Schließen Sie diese Fenster, und fügen Sie die Verweise "System. Runtime. Serialization" und "System. Service Model" dem Projekt "inkrekognition" hinzu, **indem Sie mit** der rechten Maustaste auf den Ordner "Verweise" im Projekt "inkrekognition" klicken In der folgenden Abbildung wird das Dialogfeld angezeigt, in dem die erforderlichen Verweise ausgewählt sind.

![Verweise hinzufügen (Dialogfeld) mit System. Runtime. Serialization und System. Service Model ausgewählt](images/project-3a-add-references-to-inkreco.png)<br/>
*Verweise hinzufügen (Dialogfeld) mit System. Runtime. Serialization und System. Service Model ausgewählt*

Als nächstes müssen Sie dem Projekt "InkRecognition. Web" die Verweise "System. Service Model" und "Microsoft. Ink" hinzufügen. Die Microsoft. Ink-Referenz wird nicht standardmäßig in den .net-verweisen angezeigt. Suchen Sie daher im Windows-Ordner nach Microsoft.Ink.dll. Nachdem Sie die dll gefunden haben, fügen Sie die Assembly zu den Projekt verweisen hinzu: Wählen Sie die Registerkarte **Durchsuchen** aus, wechseln Sie in den Ordner mit Microsoft.Ink.dll, wählen Sie Microsoft.Ink.dll aus, und klicken Sie dann auf **OK**. Die folgende Abbildung zeigt die Projekt Mappe im Windows-Explorer mit allen hinzugefügten Verweisassemblys.

![InkRecognition-Projekt in Windows-Explorer mit hinzugefügten Verweisassemblys](images/project-3b-with-reference-assemblies.png)<br/>
*InkRecognition-Projekt in Windows-Explorer mit hinzugefügten Verweisassemblys*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Erstellen eines Silverlight WCF-Dienstanbieter für die frei Handerkennung

Als Nächstes fügen Sie einen WCF-Dienst für die frei Handerkennung zum Projekt hinzu. Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition. Web, klicken Sie auf **Hinzufügen** und dann auf **Neues Element**. Wählen Sie die WCF Silverlight-Dienst Vorlage aus, ändern Sie den Namen in inkrecogitionservice, und klicken Sie dann auf **Hinzufügen**. Die folgende Abbildung zeigt das Dialogfeld **Neues Element hinzufügen** , bei dem der Silverlight-WCF-Dienst ausgewählt und benannt ist.

![Dialogfeld "Neues Element hinzufügen" mit ausgewähltem Silverlight-WCF-Dienst](images/project-4-add-wcf-service.png)<br/>
*Dialogfeld "Neues Element hinzufügen&quot; mit ausgewähltem Silverlight-WCF-Dienst*

Nachdem Sie den WCF Silverlight-Dienst hinzugefügt haben, wird der Dienst Code &quot;inkrecognitionservice. cs&quot; geöffnet. Ersetzen Sie den Dienst Code durch den folgenden Code.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Hinzufügen des Dienst Verweises zu Ihrem Client Projekt

Nachdem Sie den Silverlight-WCF-Dienst für InkRecognition erstellt haben, nutzen Sie den Dienst von Ihrer Client Anwendung. Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition, und wählen Sie **Dienstverweis hinzufügen**. Wählen Sie im angezeigten Dialogfeld **Dienstverweis hinzufügen** die Option **ermitteln** aus, um die Dienste aus der aktuellen Projekt Mappe zu ermitteln. Inkrecognitionservice wird im Bereich Dienste angezeigt. Doppelklicken Sie im Bereich Dienste auf inkrecognitionservice, ändern Sie den Namespace in inkrecognitionservicereferen, und klicken Sie dann auf **OK**. In der folgenden Abbildung wird das Dialogfeld **Dienstverweis hinzufügen** angezeigt, in dem inkrecognitionservice ausgewählt und der Namespace geändert wurde.

![Dialogfeld "Dienst Verweis hinzufügen", bei dem inkrecognitionservice ausgewählt und der Namespace geändert wurde](images/project-5-discover-service-reference.png)<br/>
*Dialogfeld "Dienst Verweis hinzufügen", bei dem inkrecognitionservice ausgewählt und der Namespace geändert wurde*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Hinzufügen der InkCollector-Klasse zum InkRecognition-Projekt

Klicken Sie mit der rechten Maustaste auf das Projekt InkRecognition, klicken Sie auf **Hinzufügen** und dann auf **Neues Element**. Wählen Sie im **Visual \# C** -Menü die Option **C- \# Klasse** aus. Benennen Sie die Klasse "InkCollector". In der folgenden Abbildung wird das Dialogfeld angezeigt, in dem die C \# -Klasse ausgewählt und benannt ist.

![Dialogfeld "Neues Element hinzufügen" mit \# ausgewählter c-Klasse und Namen](images/project-6-add-ink-collector.png)<br/>
*Dialogfeld "Neues Element hinzufügen" mit \# ausgewählter c-Klasse und Namen*

Nachdem Sie die InkCollector-Klasse hinzugefügt haben, wird die Klassendefinition geöffnet. Ersetzen Sie den Code im Ink Collector durch den folgenden Code.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Aktualisieren der XAML-Datei für die Standardseite und Hinzufügen eines Code Behind für die Handschrifterkennung

Nachdem Sie nun über eine Klasse verfügen, die frei Hand Eingaben sammelt, müssen Sie den XAML-Code in Page. XAML mit dem folgenden XAML-Code aktualisieren. Der folgende Code fügt dem Eingabebereich einen gelben Farbverlauf, ein InkCanvas-Steuerelement und eine Schaltfläche hinzu, die die Erkennung auslöst.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Ersetzen Sie die Code Behind-Seite Page. XAML. cs durch den folgenden Code, mit dem ein Ereignishandler für die Schaltfläche " **erkennen** " hinzugefügt wird.

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Entfernen von sicheren Transport Direktiven aus der Client Konfiguration

Bevor Sie den WCF-Dienst nutzen können, müssen Sie alle sicheren Transport Optionen aus der Dienst Konfiguration entfernen, da sichere Transporte in den WCF-Diensten von Silverlight 2,0 derzeit nicht unterstützt werden. Aktualisieren Sie aus dem Projekt inkrekognition die Sicherheitseinstellungen in ServiceReferences. ClientConfig. Ändern der Sicherheits-XML-Datei

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

zu

```XML
       <security mode="None"/>
```

Nun sollte Ihre Anwendung ausgeführt werden. In der folgenden Abbildung wird gezeigt, wie die Anwendung in awebpagemit einem im Erkennungs Feld eingegebenen Handschrift aussieht.

![Anwendung in awebpage, bei der eine Handschrift in das Erkennungs Feld eingegeben wurde](images/demo-1.png)<br/>
*Anwendung in awebpage, bei der eine Handschrift in das Erkennungs Feld eingegeben wurde*

Die folgende Abbildung zeigt den erkannten Text in der Dropdown Liste " **Ergebnis** ".

![Anwendung innerhalb von awebpagewith erkannter Text in der Dropdown Liste "Ergebnis"](images/demo-2.png)<br/>
*Anwendung innerhalb von awebpagewith erkannter Text in der Dropdown Liste "Ergebnis"*

 

 



