---
title: Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung
description: Hinweis Auf dieser Seite wird die Legacy-WPF-Entwicklung für Windows 8.1 behandelt. Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, lesen Sie die neueste Dokumentation zu GitHub. .
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows Benutzeroberfläche,DPI-fähige Anwendungen
- Windows Benutzeroberfläche, hoher DPI
- DPI-fähige Anwendungen
- hoher DPI-Anteil
- Schreiben von DPI-fähigen Win32-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1527412e3259efca7d81285c6ba7ed42dbaebf43d37307342de02f1d2ce9d339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249688"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Entwickeln einer DPI pro Monitor-fähigen WPF-Anwendung

**Wichtige APIs**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Auf dieser Seite wird die WPF-Legacyentwicklung für Windows 8.1 behandelt.** Wenn Sie WPF-Anwendungen für Windows 10 entwickeln, lesen Sie die <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">neueste Dokumentation zu GitHub.</a>

 

Windows 8.1 bietet Entwicklern neue Funktionen zum Erstellen von DPI-fähigen Desktopanwendungen pro Monitor. Um diese Funktionalität nutzen zu können, muss eine DPI-fähige Anwendung pro Monitor folgende Schritte ausführen:

-   Ändern der Fensterdimensionen, um eine physische Größe beizubehalten, die auf jeder Anzeige konsistent angezeigt wird
-   Erneutes Layout und erneutes Rendern von Grafiken für die neue Fenstergröße
-   Auswählen von Schriftarten, die entsprechend der DPI-Ebene skaliert werden
-   Auswählen und Laden von Bitmapressourcen, die auf die DPI-Ebene zugeschnitten sind

Um die Erstellung einer DPI-fähigen Anwendung pro Monitor zu vereinfachen, stellt Windows 8.1 die folgenden Microsoft Win32APIs bereit:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (oder DPI-Manifesteintrag) legt den Prozess auf eine angegebene DPI-Bekanntheitsstufe fest, die dann bestimmt, wie Windows die Benutzeroberfläche skaliert. Dadurch wird [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)abgelöst.
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) gibt die DPI-Awareness-Ebene zurück. Dadurch wird [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware)abgelöst.
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) gibt den DPI für einen Monitor zurück.
-   Die [**\_ WM-DPICHANGED-Fensterbenachrichtigung**](wm-dpichanged.md) wird an Monitor-DPI-fähige Anwendungen gesendet, wenn sich die Position eines Fensters so ändert, dass ein Großteil des Bereichs einen Monitor mit einem DPI überschneidet, der sich vom DPI unterscheidet, bevor sich die Position ändert oder der Benutzer den Anzeigeschieberegler verschiebt. Verwenden Sie diese Benachrichtigung, um eine Anwendung zu erstellen, deren Größe geändert und erneut gerendert wird, wenn ein Benutzer sie auf eine andere Anzeige verschiebt.

Weitere Informationen zu den verschiedenen DPI-Bekanntheitsgraden, die für Desktopanwendungen in Windows 8.1 unterstützt werden, finden Sie im Thema [Schreiben von DPI-Aware Desktop- und Win32-Anwendungen.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

## <a name="dpi-scaling-and-wpf"></a>DPI-Skalierung und WPF

WPF-Anwendungen (Windows Presentation Foundation) sind standardmäßig DPI-fähigen Systemanwendungen. Definitionen der verschiedenen DPI-Bewusstseinsebenen finden Sie im Thema [Schreiben von DPI-Aware Desktop- und Win32-Anwendungen.](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)) Das WPF-Grafiksystem verwendet geräteunabhängige Einheiten, um Auflösung und Geräteunabhängigkeit zu ermöglichen. WPF skaliert jedes geräteunabhängige Pixel automatisch basierend auf dem aktuellen System-DPI. Dadurch können WPF-Anwendungen automatisch skaliert werden, wenn der DPI des Monitors, auf dem sich das Fenster befindet, demselben System-DPI entspricht. Da WPF-Anwendungen jedoch systemdpi-fähige Anwendungen sind, wird die Anwendung vom Betriebssystem skaliert, wenn die Anwendung auf einen Monitor mit einem anderen DPI verschoben wird oder wenn der Schieberegler in der Systemsteuerung verwendet wird, um den DPI zu ändern. Die Skalierung im Betriebssystem kann dazu führen, dass WPF-Anwendungen unscharf erscheinen, insbesondere wenn die Skalierung nicht integral ist. Um die Skalierung von WPF-Anwendungen zu vermeiden, müssen sie aktualisiert werden, um DPI-bewusst pro Monitor zu sein.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Exemplarische Vorgehensweise zum WPF-Beispiel pro Monitor

Das [WPF-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) pro Monitor ist eine WPF-Beispielanwendung, die aktualisiert wurde, um DPI-fähige Daten pro Monitor zu erhalten. Das Beispiel umfasst zwei Projekte:

-   NativeHelpers.vcxproj: Dies ist ein natives Hilfsprojekt, das die Kernfunktionen implementiert, um eine WPF-Anwendung mithilfe der oben genannten Win32APIs monitor-fähigen DPI-fähigen Anwendungen zu machen. Das Projekt enthält zwei Klassen:
    -   PerMonDPIHelpers: Eine Klasse, die Hilfsfunktionen für DPI-bezogene Vorgänge bereitstellt, z. B. das Abrufen des aktuellen DPI des aktiven Monitors, das Festlegen eines Prozesses auf DPI-bezogene Vorgänge pro Monitor usw.
    -   PerMonitorDPIWindow: Eine von **System.Windows abgeleitete Basisklasse. Fenster,** das Funktionen implementiert, um ein WPF-Anwendungsfenster so zu gestalten, dass es dpi-bewusst pro Monitor ist. Passt fenstergröße, Grafikrenderinggröße und Schriftgrad basierend auf dem DPI des Monitors anstelle des System-DPI an.
-   WPFApplication.csproj: Beispiel-WPF-Anwendung, die PerMonitorDPIWindow (PerMonitorDPIWindow) nutzt und zeigt, wie sich das Anwendungsfenster und das Rendering ändern, wenn das Fenster auf einen Monitor mit einem anderen DPI verschoben wird oder wenn der Schieberegler in der Anzeigesteuerung verwendet wird, um den DPI zu ändern.

Führen Sie die folgenden Schritte aus, um das Beispiel auszuführen:

1.  Herunterladen und Entzippen des [WPF-Beispiels](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) per Monitor Aware
2.  Starten Sie Microsoft Visual Studio, und wählen Sie **Datei > > Project/Projektmappe öffnen** aus.
3.  Navigieren Sie zu dem Verzeichnis, das das entpackte Beispiel enthält. Wechseln Sie zum Verzeichnis mit dem Namen für das Beispiel, und doppelklicken Sie auf die Datei Visual Studio Projektmappe (.sln).
4.  Drücken Sie F7, oder verwenden **Sie Build > Build Solution** , um das Beispiel zu erstellen.
5.  Drücken Sie STRG+F5, oder verwenden Sie **Debuggen > Starten ohne Debuggen,** um das Beispiel auszuführen.

Um die Auswirkungen der Änderung des DPI für eine WPF-Anwendung anzuzeigen, die aktualisiert wird, sodass sie mithilfe der Basisklasse im Beispiel monitorspezifische DPI-fähige Daten enthält, verschieben Sie das Anwendungsfenster in und aus Anzeigen mit unterschiedlichen DPIs. Wenn das Fenster zwischen Monitoren verschoben wird, werden die Fenstergröße und die Ui-Skalierung basierend auf dem DPI der Anzeige mithilfe des skalierbaren Grafiksystems von WPF aktualisiert, anstatt vom Betriebssystem skaliert zu werden. Die Benutzeroberfläche der Anwendung wird nativ gerendert und erscheint nicht unscharf. Wenn Sie nicht über zwei Anzeigen mit unterschiedlichen DPI verfügen, ändern Sie den DPI, indem Sie den Schieberegler in der Systemsteuerung Anzeigen ändern. Wenn Sie den Schieberegler ändern und auf **Übernehmen** klicken, wird die Größe des Fensters der Anwendung geändert und die Skalierung der Benutzeroberfläche automatisch aktualisiert.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Aktualisieren einer vorhandenen WPF-Anwendung zur Überwachung von DPI-fähigen Daten mithilfe des Hilfsprojekts im WPF-Beispiel

Wenn Sie über eine vorhandene WPF-Anwendung verfügen und das DPI-Hilfsprojekt aus dem Beispiel nutzen möchten, um die DPI-Fähige zu machen, führen Sie die folgenden Schritte aus.

1.  Herunterladen und Entzippen des WPF-Beispiels per Monitor Aware
2.  Starten Sie Visual Studio, und wählen Sie **Datei > > Project/Projektmappe öffnen** aus.
3.  Navigieren Sie zu dem Verzeichnis, das eine vorhandene WPF-Anwendung enthält, und doppelklicken Sie auf die Datei Visual Studio Projektmappe (.sln).
4.  Klicken Sie mit der rechten Maustaste auf **Projektmappe > Hinzufügen > Vorhandene Project** ![ screenshot, der die Menüauswahl "Hinzufügen: Vorhandenes Projekt" veranschaulicht.](images/scrvs-image1.png)
5.  Navigieren Sie im Dialogfeld für die Dateiauswahl zu dem Verzeichnis, das das entpackte Beispiel enthält. Öffnen Sie das Verzeichnis namens für das Beispiel, navigieren Sie zum Ordner "NativeHelpers", wählen Sie die Visual C++ Projektdatei "NativeHelpers.vcxproj" aus, und klicken Sie auf **OK.**
6.  Klicken Sie mit der rechten Maustaste auf das Projekt NativeHelpers, und wählen **Sie Erstellen** aus. Dadurch wird NativeHelpers.dll generiert, die im nächsten Schritt als Verweis auf die WPF-Anwendung hinzugefügt werden. In einem Screenshot wird ![ die Auswahl des Buildmenüs veranschaulicht.](images/scrvs-image2.png)
7.  Fügen Sie einen Verweis auf NativeHelpers.dll aus Ihrer WPF-Anwendung hinzu. Erweitern Sie Ihr WPF-Anwendungsprojekt, klicken Sie mit der rechten Maustaste auf **Verweise,** und klicken Sie auf **Verweis hinzufügen...**
8.  Erweitern Sie im resultierenden Dialogfeld den Abschnitt **Projektmappe.** Wählen Sie unter **Projekte** die Option NativeHelpers aus, und klicken Sie in einem Screenshot auf **OK,** ![ der das Dialogfeld "Ressourcen-Manager" veranschaulicht.](images/scrvs-image3.png)
9.  Erweitern Sie Ihr WPF-Anwendungsprojekt, erweitern **Sie Eigenschaften**, und öffnen Sie **AssemblyInfo.cs.** Nehmen Sie die folgenden Ergänzungen zu AssemblyInfo.cs vor:
    -   Fügen Sie einen Verweis auf System hinzu. Windows. Medien im Verweisabschnitt (mit system.Windows. Medien;)
    -   Hinzufügen des DisableDpiAwareness-Attributs ( `[assembly: DisableDpiAwareness]` )

    ![Screenshot zur Veranschaulichung der zusätzlichen Eigenschaften](images/scrvs-image4.png)
10. Erben der WPF-Hauptfensterklasse von der PerMonitorDPIWindow-Basisklasse
    -   Aktualisieren Sie die CS-Datei des WPF-Hauptfensters, um von der PerMonitorDPIWindow-Basisklasse zu erben.
        -   Fügen Sie im Verweisabschnitt einen Verweis auf NativeHelpers hinzu, indem Sie die Zeile hinzufügen. `using NativeHelpers;`
        -   Erben der Hauptfensterklasse von der PerMonitorDPIWindow-Klasse

        ![Screenshot zur Veranschaulichung der c++-Referenz](images/scrvs-image5.png)
    -   Aktualisieren Sie die XAML-Datei des WPF-Hauptfensters, um von der PerMonitorDPIWindow-Basisklasse zu erben.
        -   Fügen Sie im Verweisabschnitt einen Verweis auf NativeHelpers hinzu, indem Sie die Zeile hinzufügen. `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Erben der Hauptfensterklasse von der PerMonitorDPIWindow-Klasse

        ![Screenshot zum Hinzufügen des XAML-Verweises](images/scrvs-image6.png)
11. Drücken Sie F7, oder verwenden **Sie Build > Build Solution** , um das Beispiel zu erstellen.
12. Drücken Sie STRG+F5, oder verwenden Sie **Debuggen > Starten ohne Debuggen,** um das Beispiel auszuführen.

Die [WPF-Beispielanwendung](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) pro Monitor veranschaulicht, wie eine WPF-Anwendung aktualisiert werden kann, um eine DPI-fähige Überwachung zu erhalten, indem auf die [**\_ WM-DPICHANGED-Fensterbenachrichtigung**](wm-dpichanged.md) reagiert wird. Als Reaktion auf die Fensterbenachrichtigung aktualisiert das Beispiel die von WPF verwendete Skalierungstransformation basierend auf dem aktuellen DPI des Monitors, auf dem sich das Fenster befindet. Die *wParam* der Fensterbenachrichtigung enthält den neuen DPI im *wParam*. Das *lParam-Objekt* enthält ein Rechteck mit der Größe und Position des neuen vorgeschlagenen Fensters, das für den neuen DPI skaliert wird.

Hinweis:

> [!Note]  
> Da in diesem Beispiel die Fenstergröße und die Skalierungstransformation des Stammknotens des WPF-Fensters überschrieben werden, sind möglicherweise weitere Arbeiten erforderlich, wenn:
>
> -   Die Größe des Fensters wirkt sich auf andere Teile der Anwendung aus, z. B. dieses WPF-Fenster, das in einer anderen Anwendung gehostet wird.
> -   Die WPF-Anwendung, die diese Klasse erweitert, legt eine andere Transformation für das Stammvisual fest. Das Beispiel überschreibt möglicherweise eine andere Transformation, die von der WPF-Anwendung selbst angewendet wird.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Übersicht über das Hilfsprojekt im WPF-Beispiel

Um eine vorhandene WPF-Anwendung monitorspezifische DPI-fähige WPF-Anwendungen zu erstellen, bietet die NativeHelpers-Bibliothek die folgenden Funktionen:

-   **Markiert die WPF-Anwendung als DPI-bewusst:** Die WPF-Anwendung wird durch Aufrufen von [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) für den aktuellen Prozess als monitorspezifische DPI-orientierte Anwendung gekennzeichnet. Durch das Markieren der Anwendung als DPI-bewusst pro Monitor wird sichergestellt, dass

    -   Das Betriebssystem skaliert die Anwendung nicht, wenn der System-DPI nicht mit dem aktuellen DPI des Monitors im Anwendungsfenster übereinstimmen.
    -   Die [**WM \_ DPICHANGED-Nachricht**](wm-dpichanged.md) wird gesendet, wenn sich der DPI-Aufruf des Fensters ändert.

-   **Passt die Fensterdimension an, layoutt** und rendert Grafikinhalte neu und wählt Schriftarten basierend auf dem anfänglichen DPI des Monitors aus, auf dem sich das Fenster befindet: Sobald die Anwendung als monitorspezifische DPI-bezogene Anwendung markiert ist, skaliert WPF die Fenstergröße, Grafiken und Schriftgröße weiterhin basierend auf dem System-DPI. Da beim Starten der App nicht garantiert wird, dass der DPI-Wert des Systems mit dem DPI-Wert des Monitors identisch ist, auf dem das Fenster gestartet wird, passt die Bibliothek diese Werte an, sobald das Fenster geladen wurde. Die Basisklasse **PerMonitorDPIWindow** aktualisiert diese im **OnLoaded()-Handler.**

    Die Fenstergröße wird aktualisiert, indem die **Eigenschaften Breite** und **Höhe** des Fensters geändert werden. Das Layout und die Größe werden aktualisiert, indem eine entsprechende Skalierungstransformation auf den Stammknoten des WPF-Fensters ausgeführt wird.

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

    

-   **Reagiert auf WM \_ DPICHANGED-Fensterbenachrichtigung: Aktualisieren** Sie die Fenstergröße, Die Grafik und den Schriftgrad basierend auf dem in der Fensterbenachrichtigung übergebenen DPI. Die Basisklasse **PerMonitorDPIWindow** verarbeitet die Fensterbenachrichtigung in der **HandleMessages()-Methode.**

    Die Fenstergröße wird aktualisiert, indem **SetWindowPos mithilfe** der im *Lparam* der Fenstermeldung übergebenen Informationen aufruft. Das Layout und die Grafikgröße werden aktualisiert, indem eine entsprechende Skalierungstransformation auf den Stammknoten des WPF-Fensters ausgeführt wird. Der Skalierungsfaktor wird mithilfe des DPI berechnet, der im *Wparam* der Fenstermeldung übergeben wird.

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

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Behandeln von DPI-Änderungen für Ressourcen wie Bilder

Zum Aktualisieren des Grafikinhalts wendet die WPF-Beispielanwendung eine Skalierungstransformation auf den Stammknoten der WPF-Anwendung an. Dies funktioniert zwar gut für Inhalte, die nativ von WPF gerendert werden (Rechteck, Text usw.), aber dies impliziert, dass Bitmapressourcen wie Bilder von WPF skaliert werden.

Um verschwommene Bitmaps zu vermeiden, die durch die Skalierung verursacht werden, kann der WPF-Anwendungsentwickler ein benutzerdefiniertes DPI-Bildsteuer steuerelement schreiben, das basierend auf dem aktuellen DPI-Wert des Monitors, auf dem sich das Fenster befindet, ein anderes Objekt auswählt. Das Image-Steuerelement kann sich auf das **DPIChanged()-Ereignis** verlassen, das für das WPF-Fenster ausgelöst wird, das von **PerMonitorDPIWindow** verwendet, wenn sich der DPI ändert.

> [!Note]  
> Das Image-Steuerelement sollte auch das richtige Steuerelement während des App-Starts im **Loaded()** WPF-Fensterereignishandler auswählen.

 

 

 