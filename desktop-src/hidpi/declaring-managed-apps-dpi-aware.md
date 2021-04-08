---
title: Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung
description: Beachten Sie, dass diese Seite die ältere WPF-Entwicklung für Windows 8.1 behandelt. Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, finden Sie weitere Informationen in der neuesten Dokumentation auf GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows-Benutzeroberfläche, dpi-fähige Anwendungen
- Windows-Benutzeroberfläche, hohe dpi-
- DPI-fähige Anwendungen
- hoher dpi-
- Schreiben von dpi-fähigen Win32-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101639"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung

**Wichtige APIs**

-   [**Setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**Getprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**Getdpiformonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Auf dieser Seite wird die Legacy-WPF-Entwicklung für Windows 8.1 behandelt.** Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, finden Sie weitere Informationen <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">in der neuesten Dokumentation auf GitHub.</a>

 

Windows 8.1 bietet Entwicklern neue Funktionen zum Erstellen von Desktop Anwendungen mit dpi-Werten pro Monitor. Um diese Funktionalität nutzen zu können, muss eine pro-Monitor-dpi-fähige Anwendung folgende Aktionen ausführen:

-   Ändern der Fenster Dimensionen, um eine physische Größe beizubehalten, die auf einer beliebigen Anzeige konsistent angezeigt wird
-   Erneutes Layout und erneutes Renren von Grafiken für die neue Fenstergröße
-   Schriftarten auswählen, die entsprechend der dpi-Ebene skaliert werden
-   Auswählen und Laden von bitmapassets, die auf die dpi-Ebene zugeschnitten sind

Zur Vereinfachung der Erstellung einer dpi-fähigen Anwendung mit dpi-Unterstützung bietet Windows 8.1 folgende Microsoft Win32APIs:

-   [**Setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (oder dpi-Manifest-Eintrag) legt den Prozess auf einen angegebenen dpi-Wert fest, der dann festlegt, wie Windows die Benutzeroberfläche skaliert. Dies ersetzt [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**Getprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) gibt den dpi-Bekanntheitsgrad zurück. Hierdurch wird [**isprocessdpiaware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)abgelöst.
-   [**Getdpiformonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) gibt den dpi-Wert für einen Monitor zurück.
-   Die Benachrichtigung " [**WM- \_ dpichanged**](wm-dpichanged.md) -Fenster" wird an die dpi-fähigen Anwendungen pro Monitor gesendet, wenn sich die Position eines Fensters ändert, sodass der größte Teil des Bereichs einen Monitor mit einem dpi-Wert überschneidet, der sich vom dpi-Wert unterscheidet, bevor die Position geändert wird oder wenn der Benutzer den Schieberegler verschiebt. Um eine Anwendung zu erstellen, deren Größe geändert und wieder gerendert wird, wenn ein Benutzer Sie in eine andere Anzeige verschiebt, verwenden Sie diese Benachrichtigung.

Weitere Informationen zu verschiedenen dpi-Informationen, die für Desktop Anwendungen in unterstützt werden, finden Sie unter Windows 8.1 im Thema [Schreiben von DPI-Aware Desktop-und Win32-Anwendungen](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>DPI-Skalierung und WPF

Windows Presentation Foundation (WPF)-Anwendungen sind standardmäßig System-dpi-fähig. Definitionen der verschiedenen dpi-Informationen finden Sie im Thema [schreiben DPI-Aware Desktop-und Win32-Anwendungen](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). Das WPF-Grafiksystem verwendet geräteunabhängige Einheiten, um Auflösung und Geräteunabhängigkeit zu ermöglichen. WPF skaliert jedes geräteunabhängige Pixel automatisch basierend auf dem aktuellen System-dpi-Wert. Dadurch können WPF-Anwendungen automatisch skaliert werden, wenn der dpi-Wert des Monitors, auf dem sich das Fenster befindet, dasselbe System-dpi ist. Da WPF-Anwendungen jedoch System dpi-fähig sind, wird die Anwendung vom Betriebssystem skaliert, wenn die Anwendung auf einen Monitor mit einem anderen dpi-Wert verschoben wird oder wenn der Schieberegler in der Systemsteuerung verwendet wird, um den dpi-Wert zu ändern. Das Skalieren im Betriebssystem kann dazu führen, dass WPF-Anwendungen unscharf angezeigt werden, insbesondere, wenn die Skalierung nicht ganzzahlig ist. Um das Skalieren von WPF-Anwendungen zu vermeiden, müssen Sie für die dpi-Unterstützung pro Monitor aktualisiert werden.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Exemplarische Vorgehensweise für das WPF-Beispiel pro Monitor

Das [WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) -Beispiel "pro Monitor-fähig" ist eine WPF-Beispielanwendung, die für die dpi-Unterstützung pro Monitor aktualisiert wurde. Das Beispiel umfasst zwei Projekte:

-   Nativehelpers. vcxproj: Hierbei handelt es sich um ein System eigenes Hilfsprogramm, das die Kernfunktionen implementiert, um eine WPF-Anwendung mit dpi-Werten pro Monitor zu erstellen, indem Sie die oben genannten Win32APIs verwenden. Das Projekt enthält zwei Klassen:
    -   Permondpihelper: eine Klasse, die Hilfsfunktionen für dpi-bezogene Vorgänge bereitstellt, z. b. das Abrufen des aktuellen dpi-Wert des aktiven Monitors, das Festlegen eines Prozesses für die dpi-Unterstützung pro Monitor usw.
    -   Permonitordpiwindow: eine Basisklasse, die von **System. Windows. Window** abgeleitet wird und Funktionen implementiert, mit denen ein WPF-Anwendungsfenster pro Monitor dpi-fähig ist. Passt die Fenstergröße, Grafik Renderinggröße und Schriftgröße basierend auf der dpi des Monitors und nicht auf dem System-dpi an.
-   Wpfapplikation. csproj: Beispiel einer WPF-Anwendung, die das permonitordpiwindow (permonitordpiwindow) verwendet, und zeigt, wie das Anwendungsfenster und das Rendering geändert werden, wenn das Fenster auf einen Monitor mit einem anderen dpi-Wert verschoben wird, oder wenn der Schieberegler in der Anzeige Steuerung verwendet wird, um den dpi zu ändern.

Führen Sie die folgenden Schritte aus, um das Beispiel auszuführen:

1.  Herunterladen und Entpacken des WPF-Beispiels " [pro Monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) "
2.  Starten Sie Microsoft Visual Studio, und wählen Sie **Datei > > Projekt/Projekt Mappe öffnen** .
3.  Navigieren Sie zu dem Verzeichnis, das das entzippte Beispiel enthält. Wechseln Sie zum Verzeichnis für das Beispiel, und doppelklicken Sie auf die Visual Studio-Projektmappendatei (. sln).
4.  Drücken Sie F7, oder verwenden Sie **Build > Build Solution** , um das Beispiel zu erstellen.
5.  Drücken Sie STRG + F5 oder **Debuggen > starten ohne Debugging** , um das Beispiel auszuführen.

Um die Auswirkungen der Änderung von dpi für eine WPF-Anwendung, die mit der-Basisklasse im Beispiel aktualisiert wird, auf dpi-fähig zu erkennen, verschieben Sie das Anwendungsfenster in und aus anzeigen, die über unterschiedliche DPIs verfügen. Wenn das Fenster zwischen Monitoren verschoben wird, werden die Fenstergröße und die Benutzeroberflächen Skala basierend auf dem dpi-Wert der Anzeige mithilfe des skalierbaren Grafik Systems von WPF aktualisiert, anstatt durch das Betriebssystem skaliert zu werden. Die Benutzeroberfläche der Anwendung wird nativ gerendert und wird nicht verschwommen angezeigt. Wenn Sie nicht über zwei Anzeigeelemente mit unterschiedlichem dpi verfügen, ändern Sie den dpi-Code, indem Sie den Schieberegler in der Systemsteuerung anzeigen ändern. Wenn Sie den Schieberegler ändern und auf **anwenden** klicken, wird die Größe des Anwendungsfensters geändert und die Benutzeroberflächen Skalierung automatisch aktualisiert.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Aktualisieren einer vorhandenen WPF-Anwendung für die dpi-Unterstützung per Monitor mithilfe des Hilfsprojekts im WPF-Beispiel

Wenn Sie bereits über eine WPF-Anwendung verfügen und das dpi-Hilfsobjekt aus dem Beispiel nutzen möchten, um es zu berücksichtigen, führen Sie die folgenden Schritte aus.

1.  Herunterladen und Entpacken des WPF-Beispiels "pro Monitor"
2.  Starten Sie Visual Studio, und wählen Sie **Datei > > Projekt/Projekt Mappe öffnen** aus.
3.  Navigieren Sie zu dem Verzeichnis, das eine vorhandene WPF-Anwendung enthält, und doppelklicken Sie auf die Visual Studio-Projektmappendatei (. sln).
4.  Klicken Sie mit der rechten Maustaste auf Projekt Mappe, **> > vorhandenes Projekt hinzuzufügen**. ![](images/scrvs-image1.png)
5.  Navigieren Sie im Dialogfeld zur Dateiauswahl zu dem Verzeichnis, das das entzippte Beispiel enthält. Öffnen Sie für das Verzeichnis, das für das Beispiel benannt ist, navigieren Sie zum Ordner "nativehelpers", wählen Sie die Visual C++ Projektdatei "nativehelpers. vcxproj" aus, und klicken Sie auf **OK** .
6.  Klicken Sie mit der rechten Maustaste auf das Projekt nativehelpers, und wählen Sie **Erstellen**. Hierdurch werden NativeHelpers.dll generiert, die im nächsten Schritt als Verweis auf die WPF-Anwendung hinzugefügt werden. ![](images/scrvs-image2.png)
7.  Fügen Sie einen Verweis auf NativeHelpers.dll aus der WPF-Anwendung hinzu. Erweitern Sie das WPF-Anwendungsprojekt, klicken Sie mit der rechten Maustaste auf **Verweise** , und klicken Sie auf **Verweis hinzufügen.**
8.  Erweitern Sie im daraufhin angezeigten Dialogfeld **den Abschnitt Projekt** Mappe. Wählen Sie unter **Projekte** die Option nativehelpers aus, und klicken Sie auf **OK** ![ einen Screenshot, der das Dialogfeld Resource Manager veranschaulicht.](images/scrvs-image3.png)
9.  Erweitern Sie das WPF-Anwendungsprojekt, erweitern Sie **Eigenschaften**, und öffnen Sie **AssemblyInfo. cs**. Nehmen Sie an AssemblyInfo. cs die folgenden Ergänzungen vor.
    -   Fügen Sie im Referenz Abschnitt (mithilfe von System. Windows. Media;) einen Verweis auf System. Windows. Media hinzu.
    -   Fügen Sie das disabledpiawareness-Attribut () hinzu. `[assembly: DisableDpiAwareness]`

    ![ein Screenshot, der die zusätzlichen Eigenschaften veranschaulicht](images/scrvs-image4.png)
10. Die Haupt-WPF-Fenster Klasse wird von der permonitordpiwindow-Basisklasse geerbt.
    -   Aktualisieren Sie die CS-Datei des Hauptfensters von WPF so, dass Sie von der permonitordpiwindow-Basisklasse geerbt wird.
        -   Fügen Sie im Abschnitt "Reference" einen Verweis auf nativehelpers hinzu, indem Sie die Zeile hinzufügen. `using NativeHelpers;`
        -   Die Hauptfenster Klasse wird von der permonitordpiwindow-Klasse geerbt.

        ![ein Screenshot, der die c++-Referenz veranschaulicht](images/scrvs-image5.png)
    -   Aktualisieren Sie die XAML-Datei des Haupt-WPF-Fensters, um von der permonitordpiwindow-Basisklasse zu erben.
        -   Fügen Sie im Abschnitt "Reference" einen Verweis auf nativehelpers hinzu, indem Sie die Zeile hinzufügen. `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Die Hauptfenster Klasse wird von der permonitordpiwindow-Klasse geerbt.

        ![Screenshot, der das Hinzufügen des XAML-Verweises veranschaulicht](images/scrvs-image6.png)
11. Drücken Sie F7, oder verwenden Sie **Build > Build Solution** , um das Beispiel zu erstellen.
12. Drücken Sie STRG + F5 oder **Debuggen > starten ohne Debugging** , um das Beispiel auszuführen.

Die [Beispielanwendung "pro Monitor-fähiger WPF](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) " veranschaulicht, wie eine WPF-Anwendung aktualisiert werden kann, um dpi-fähig zu sein, indem auf die Benachrichtigung "WM- [**\_ dpichanged**](wm-dpichanged.md) -Fenster" reagiert wird. In Reaktion auf die Fenster Benachrichtigung aktualisiert das Beispiel die Skalierungs Transformation, die von WPF verwendet wird, basierend auf dem aktuellen dpi-Wert des Monitors, auf dem sich das Fenster befindet. Der *wParam* -Parameter der Fenster Benachrichtigung enthält den neuen dpi-Code in der *wParam*. Der *LPARAM* enthält ein Rechteck mit der Größe und Position des neuen vorgeschlagenen Fensters, das auf den neuen dpi skaliert wird.

Hinweis:

> [!Note]  
> Da in diesem Beispiel die Fenstergröße und die Skalierungs Transformation des Stamm Knotens des WPF-Fensters überschrieben werden, sind möglicherweise weitere Aufgaben für Anwendungsentwickler erforderlich, wenn Folgendes gilt:
>
> -   Die Größe des Fensters wirkt sich auf andere Teile der Anwendung aus, wie dieses WPF-Fenster, das in einer anderen Anwendung gehostet wird.
> -   Die WPF-Anwendung, die diese Klasse erweitert, legt eine andere Transformation für das visuelle Stamm Element fest. Das Beispiel kann eine andere Transformation überschreiben, die von der WPF-Anwendung selbst angewendet wird.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Übersicht über das Hilfsprojekt im WPF-Beispiel

Um eine vorhandene WPF-Anwendung pro Monitor dpi-fähig zu machen, bietet die nativehelpers-Bibliothek die folgenden Funktionen:

-   **Markiert die WPF-Anwendung als pro-ponitor-dpi-Unterstützung:** Die WPF-Anwendung wird mit dpi-Werten pro Monitor gekennzeichnet, indem [**setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) für den aktuellen Prozess aufgerufen wird. Wenn Sie die Anwendung mit dpi-Werten pro Monitor markieren, wird sichergestellt, dass

    -   Das Betriebssystem skaliert die Anwendung nicht, wenn der System-dpi nicht mit dem aktuellen dpi-Wert des Monitors identisch ist, auf dem sich das Anwendungsfenster befindet.
    -   Die [**WM- \_ dpichanged**](wm-dpichanged.md) -Nachricht wird gesendet, wenn sich der dpi-Wert des Fensters ändert.

-   **Passt die Fenster Dimension an, formatiert das Layout und renre den Grafik Inhalt erneut und wählt Schriftarten basierend auf dem anfänglichen dpi-Wert des Monitors aus, auf dem sich das Fenster befindet:** Nachdem die Anwendung mit dpi-Werten pro Monitor markiert wurde, skaliert WPF weiterhin die Fenstergröße, Grafik und Schriftgröße basierend auf dem System-dpi. Da der dpi-Wert beim APP-Start nicht garantiert identisch mit dem dpi-Wert des Monitors ist, auf dem das Fenster gestartet wird, werden diese Werte von der Bibliothek nach dem Laden des Fensters angepasst. Die Basisklasse **permonitordpiwindow** aktualisiert diese im **OnLoaded ()** -Handler.

    Die Fenstergröße wird aktualisiert, indem die Eigenschaften für **Breite** und **Höhe** des Fensters geändert werden. Layout und Größe werden aktualisiert, indem eine entsprechende Skalierungs Transformation auf den Stamm Knoten des WPF-Fensters angewendet wird.

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   **Antwortet auf WM \_ Benachrichtigung zum dpichanged-Fenster:** aktualisieren Sie die Fenstergröße, Grafik und Schriftgröße basierend auf dem in der Fenster Benachrichtigung übergebenen dpi-Code. Die Basisklasse **permonitordpiwindow** behandelt die Fenster Benachrichtigung in der Methode " **Lenker Nachrichten ()** ".

    Die Fenstergröße wird durch Aufrufen von **SetWindowPos** mithilfe der Informationen aktualisiert, die im *LPARAM* der Fenster Meldung ausgegeben werden. Layout und Grafik Größe werden aktualisiert, indem eine entsprechende Skalierungs Transformation auf den Stamm Knoten des WPF-Fensters angewendet wird. Der Skalierungsfaktor wird mithilfe des dpi-Wert berechnet, der in der *wParam* der Fenster Meldung ausgegeben wird.

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Behandeln von dpi-Änderungen für Assets wie Bilder

Um Grafik Inhalte zu aktualisieren, wendet die Beispiel-WPF-Anwendung eine Skalierungs Transformation auf den Stamm Knoten der WPF-Anwendung an. Dies funktioniert gut für Inhalte, die nativ von WPF (Rechteck, Text usw.) gerendert werden. Dies impliziert, dass Bitmap-Assets wie Bilder von WPF skaliert werden.

Um unscharfe Bitmaps zu vermeiden, die durch die Skalierung verursacht werden, kann der WPF-Anwendungsentwickler ein benutzerdefiniertes dpi-Bild Steuerelement schreiben, das basierend auf dem aktuellen dpi-Wert des Monitors, auf dem sich das Fenster befindet, ein anderes Das Image-Steuerelement kann sich auf das **dpichanged ()** -Ereignis stützen, das für das WPF-Fenster ausgelöst wird, das aus dem **permonitordpiwindow** verwendet wird

> [!Note]  
> Das Image-Steuerelement sollte auch das Rechte Steuerelement beim Starten der APP im **geladenen** WPF-Fenster Ereignishandler auswählen.

 

 

 