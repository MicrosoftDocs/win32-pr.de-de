---
title: Desktopanwendungsentwicklung mit hohem DPI-Windows
description: Dieser Inhalt richtet sich an Entwickler, die Desktopanwendungen aktualisieren möchten, um den dynamischen Skalierungsfaktor (auch als
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01958791dccd7c836babedbe726233797eddb646
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471326"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Desktopanwendungsentwicklung mit hohem DPI-Windows

Dieser Inhalt richtet sich an Entwickler, die Desktopanwendungen aktualisieren möchten, um Änderungen des Anzeigeskalierungsfaktors (Punkte pro Zoll oder DPI) dynamisch zu verarbeiten, sodass ihre Anwendungen auf jeder Anzeige, auf der sie gerendert werden, präzise sein können.

Wenn Sie zunächst eine neue Windows-App von Grund auf neu erstellen, wird dringend empfohlen, eine [UWP-Anwendung (Universal Windows Platform)](/windows/uwp/get-started/whats-a-uwp) zu erstellen. UWP-Anwendungen werden &mdash; automatisch und dynamisch für jede Anzeige &mdash; skaliert, auf der sie ausgeführt werden.

Desktopanwendungen, die ältere Windows Programmiertechnologien (unformatierte Win32-Programmierung, Windows Forms, Windows Presentation Framework usw.) verwenden, können die DPI-Skalierung ohne zusätzliche Entwicklerarbeit nicht automatisch verarbeiten. Ohne diese Arbeit erscheinen Anwendungen in vielen gängigen Verwendungsszenarien unscharf oder falsch dimensionierte Anwendungen. Dieses Dokument enthält Kontext und Informationen dazu, was bei der Aktualisierung einer Desktopanwendung erforderlich ist, um ordnungsgemäß gerendert zu werden.

## <a name="display-scale-factor--dpi"></a>Anzeigen des Skalierungsfaktors & DPI

Im Laufe der Anzeigetechnologie haben Hersteller von Anzeigepanels eine steigende Anzahl von Pixeln in jede Einheit des physischen Raums auf ihren Panels gepackt. Dies hat dazu geführt, dass die DPI -Punkte (Dots per Inch) moderner Anzeigepanels wesentlich höher sind als in der Vergangenheit. In der Vergangenheit hatten die meisten Anzeigen 96 Pixel pro linearen Zoll physischen Raum (96 DPI); Im Jahr 2017 sind Anzeigen mit fast 300 DPI oder höher sofort verfügbar.

Die meisten Legacyframeworks der Desktopbenutzeroberfläche haben integrierte Annahmen, dass sich der Anzeige-DPI während der Lebensdauer des Prozesses nicht ändert.  Diese Annahme gilt nicht mehr, da sich Anzeige-DPIs während der Lebensdauer eines Anwendungsprozesses häufig mehrmals ändern. Einige häufige Szenarien, in denen sich der Anzeigeskalfaktor/DPI ändert, sind:

-   Setups mit mehreren Monitoren, bei denen jede Anzeige über einen anderen Skalierungsfaktor verfügt und die Anwendung von einer Anzeige in eine andere verschoben wird (z. B. eine 4K- und eine 1080p-Anzeige).
-   Andocken und Abdocken eines Laptops mit hohem DPI-Wert mit einer externen Anzeige mit geringem DPI -Wert (oder umgekehrt)
-   Herstellen einer Verbindung über Remotedesktop von einem Laptop/Tablet mit hohem DPI-Wert mit einem Low-DPI-Gerät (oder umgekehrt)
-   Ändern von Anzeigefaktoreinstellungen während der Ausführung von Anwendungen

In diesen Szenarien zeichnen sich UWP-Anwendungen automatisch für den neuen DPI neu. Desktopanwendungen werden standardmäßig und ohne zusätzliche Entwicklerarbeit nicht verwendet. Desktopanwendungen, die diese zusätzliche Arbeit nicht durchführen, um auf DPI-Änderungen zu reagieren, erscheinen dem Benutzer möglicherweise unscharf oder falsch dimensionierte.

## <a name="dpi-awareness-mode"></a>DPI-Awareness-Modus

Desktopanwendungen müssen Windows mitteilen, ob sie die DPI-Skalierung unterstützen. Standardmäßig berücksichtigt das System Desktopanwendungen DPI nicht und streckt ihre Fenster bitmapgestreckt. Durch Festlegen eines der folgenden verfügbaren DPI-Erkennungsmodi können Anwendungen explizit Windows angeben, wie sie die DPI-Skalierung behandeln möchten:

### <a name="dpi-unaware"></a>DPI nicht bekannt

Anwendungen ohne DPI-Werte werden mit einem festen DPI-Wert von 96 (100 %) gerendert. Wenn diese Anwendungen auf einem Bildschirm mit einer Anzeigeskala von mehr als 96 DPI ausgeführt werden, strecken Windows die Anwendungsbitmap auf die erwartete physische Größe. Dies führt dazu, dass die Anwendung unscharf erscheint.

### <a name="system-dpi-awareness"></a>System-DPI-Kenntnis

Desktopanwendungen, die system-DPI-fähige Anwendungen sind, erhalten in der Regel den DPI des primären verbundenen Monitors zum Zeitpunkt der Benutzeranmeldung. Während der Initialisierung wird die Benutzeroberfläche entsprechend (Größenanpassungssteuerelemente, Auswahl von Schriftgraden, Laden von Ressourcen usw.) mit diesem System-DPI-Wert angepasst. Daher werden System-DPI-fähige Anwendungen nicht durch Windows auf Anzeigen skaliert (Bitmap gestreckt), die an diesem einzelnen DPI gerendert werden. Wenn die Anwendung auf eine Anzeige mit einem anderen Skalierungsfaktor verschoben wird oder sich der Skalierungsfaktor der Anzeige andernfalls ändert, skaliert Windows die Fenster der Anwendung durch Bitmaps, sodass sie unscharf erscheinen. System-DPI-fähige Desktopanwendungen werden effektiv nur mit einem einzigen Skalierungsfaktor gerendert, was bei jeder Änderung des DPI unscharf wird.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor und Per-Monitor (V2) – DPI-Kenntnis

Es wird empfohlen, Desktopanwendungen so zu aktualisieren, dass sie den DPI-Modus pro Monitor verwenden, sodass sie sofort ordnungsgemäß gerendert werden können, wenn sich der DPI ändert. Wenn eine Anwendung an Windows meldet, dass sie in diesem Modus ausgeführt werden soll, stretcht Windows die Anwendung nicht, wenn sich der DPI ändert, sondern sendet [WM \_ DPICHANGED](wm-dpichanged.md) an das Anwendungsfenster. Es liegt dann in der vollständigen Verantwortung der Anwendung, die Größenänderung für den neuen DPI selbst zu übernehmen. Die meisten Benutzeroberflächenframeworks, die von Desktopanwendungen (Windows allgemeinen Steuerelementen (comctl32), Windows Forms, Windows Presentation Framework usw.) verwendet werden, unterstützen keine automatische DPI-Skalierung, sodass Entwickler die Größe ihrer Fenster selbst ändern und neu positionieren müssen.

Es gibt zwei Versionen von Per-Monitor Bekanntheit, dass sich eine Anwendung als registrieren kann: Version 1 und Version 2 (PMv2). Das Registrieren eines Prozesses als im PMv2-Awareness-Modus ausgeführt führt zu:

1.  Die Anwendung, die benachrichtigt wird, wenn sich der DPI ändert (sowohl die HWNDs der obersten Ebene als auch die untergeordneten HWNDs)
2.  Die Anwendung sieht die unformatierten Pixel der einzelnen Anzeigen.
3.  Die Anwendung wird nie durch Windows skaliert.
4.  Automatischer Nicht-Clientbereich (Fensterbeschriftung, Scrollleisten usw.) DPI-Skalierung nach Windows
5.  Win32-Dialoge (aus [CreateDialog)](/windows/desktop/api/winuser/nf-winuser-createdialogw)werden automatisch durch Windows skaliert.
6.  Designgezeichnete Bitmap-Objekte in allgemeinen Steuerelementen (Kontrollkästchen, Schaltflächenhintergrund usw.), die automatisch mit dem entsprechenden DPI-Skalierungsfaktor gerendert werden

Bei ausführung im Per-Monitor v2 Awareness-Modus werden Anwendungen benachrichtigt, wenn sich ihr DPI geändert hat. Wenn eine Anwendung die Größe für den neuen DPI nicht selbst ändert, wird die Benutzeroberfläche der Anwendung zu klein oder zu groß angezeigt (abhängig vom Unterschied in den vorherigen und neuen DPI-Werten).

> [!Note]  
> Per-Monitor V1-Awareness (PMv1) ist sehr begrenzt. Es wird empfohlen, dass Anwendungen PMv2 verwenden.

Die folgende Tabelle zeigt, wie Anwendungen in verschiedenen Szenarien gerendert werden:


| DPI-Awareness-Modus | Windows Eingeführte Version | DPI-Ansicht der Anwendung | Verhalten bei DPI-Änderung | 
|--------------------|----------------------------|---------------------------|------------------------|
| Nicht bekannt | – | Alle Anzeigen sind 96 DPI | Bitmap-Stretching (unscharf) | 
| System | Vista | Alle Anzeigen verfügen über den gleichen DPI (DPI der primären Anzeige zum Zeitpunkt des Startens der aktuellen Benutzersitzung). | Bitmap-Stretching (unscharf) | 
| Per-Monitor | 8.1 | Der DPI der Anzeige, auf der sich das Anwendungsfenster in erster Linie befindet. | <ul><li>HWND der obersten Ebene wird über DPI-Änderungen benachrichtigt</li><li>Keine DPI-Skalierung von Benutzeroberflächenelementen.</li></ul><br /> | 
| Per-Monitor V2 | Windows 10 Creators Update (1703) | Der DPI der Anzeige, auf der sich das Anwendungsfenster in erster Linie befindet. | <ul><li>HWNDs der obersten Ebene <span class="underline">und</span> untergeordneter HWNDs werden über DPI-Änderungen benachrichtigt.</li></ul><br /><span class="underline">Automatische DPI-Skalierung von:</span><ul><li>Nicht-Clientbereich</li><li>Designgezeichnete Bitmaps in allgemeinen Steuerelementen (comctl32 V6)</li><li>Dialoge (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li></ul><br /> | 


### <a name="per-monitor-v1-dpi-awareness"></a>Pro Monitor (V1) DPI-Kenntnis

Per-Monitor V1 DPI Awareness Mode (PMv1) wurde mit Windows 8.1 eingeführt. Dieser DPI-Awareness-Modus ist sehr eingeschränkt und bietet nur die unten aufgeführten Funktionen. Es wird empfohlen, dass Desktopanwendungen Per-Monitor v2-Modus verwenden, der ab Windows 10 1703 unterstützt wird.

Die anfängliche Unterstützung für die überwachungsbezogene Erkennung bot anwendungen nur Folgendes:

1.  HWNDs der obersten Ebene werden über eine DPI-Änderung benachrichtigt und erhalten eine neue vorgeschlagene Größe.
2.  Windows wird die Benutzeroberfläche der Anwendung nicht durch Bitmap gestreckt.
3.  Die Anwendung sieht alle Anzeigen in physischen Pixeln (siehe Virtualisierung).

Bei Windows 10 1607 oder höher können PMv1-Anwendungen während WM NCCREATE auch [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) aufrufen, \_ um anzufordern, dass der Nicht-Clientbereich des Fensters ordnungsgemäß skaliert Windows.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Unterstützung der DPI-Skalierung pro Monitor nach BENUTZERoberflächenframework/Technologie

Die folgende Tabelle zeigt den Grad der Unterstützung von DPI-Informationen pro Monitor, der von verschiedenen Windows UI-Frameworks ab Windows 10 1703 angeboten wird:


| Framework/Technologie | Support | Betriebssystemversion | DPI-Skalierung durch | Weitere Informationen | 
|------------------------|---------|------------|------------------------|-----------------|
| Universelle Windows-Plattform (UWP) | Vollständig | 1607 | Benutzeroberflächenframework | <a href="/windows/uwp/get-started/whats-a-uwp">Universelle Windows-Plattform (UWP)</a> | 
| Raw Win32/Common Controls V6 (comctl32.dll) | <ul><li>DPI-Änderungsbenachrichtigungsmeldungen, die an alle HWNDs gesendet werden</li><li>Designgezeichnete Objekte werden ordnungsgemäß in allgemeinen Steuerelementen gerendert.</li><li>Automatische DPI-Skalierung für Dialoge</li></ul> | 1703 | Application | <a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Beispiel</a> | 
| Windows Forms | Eingeschränkte automatische DPI-Skalierung pro Monitor für einige Steuerelemente | 1703 | Benutzeroberflächenframework | <a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Hohe DPI-Unterstützung in Windows Forms</a> | 
| Windows Presentation Framework (WPF) | Native WPF-Anwendungen skalieren WPF, die in anderen Frameworks gehostet werden, DPI-Skalierung, und andere in WPF gehostete Frameworks werden nicht automatisch skaliert. | 1607 | Benutzeroberflächenframework | <a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Beispiel</a> | 
| GDI | Keine | – | Application | Weitere Informationen <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">finden Sie unter GDI High-DPI Scaling (GDI-Skalierung mit hohem DPI-Wert).</a> | 
| GDI+ | Keine | – | Application | Weitere Informationen <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">finden Sie unter GDI High-DPI Scaling (GDI-Skalierung mit hohem DPI-Wert).</a> | 
| MFC | Keine | – | Application | – | 




 

## <a name="updating-existing-applications"></a>Aktualisieren bestehender Anwendungen

Um eine vorhandene Desktopanwendung für die ordnungsgemäße DPI-Skalierung zu aktualisieren, muss sie so aktualisiert werden, dass zumindest die wichtigen Teile der Benutzeroberfläche aktualisiert werden, um auf DPI-Änderungen zu reagieren.

Die meisten Desktopanwendungen werden im DPI-Bewusstseinsmodus des Systems ausgeführt. System-DPI-orientierte Anwendungen werden in der Regel auf die DPI der primären Anzeige skaliert (die Anzeige, auf der sich die Taskleiste zum Zeitpunkt des Windows Sitzung befand). Wenn sich der DPI-Windows, wird die Benutzeroberfläche dieser Anwendungen gestreckt, was häufig dazu führt, dass sie unscharf sind. Wenn Sie eine System-DPI-orientierte Anwendung aktualisieren, um monitorspezifische DPI-benachrichtigungen zu erhalten, muss der Code, der das Benutzeroberflächenlayout behandelt, so aktualisiert werden, dass er nicht nur während der Anwendungsin initialisierung ausgeführt wird, sondern auch, wenn eine DPI-Änderungsbenachrichtigung[(WM \_ DPICHANGED](wm-dpichanged.md) im Fall von Win32) empfangen wird. Dies umfasst in der Regel das Erneute Überprüfen sämtlicher Annahmen im Code, dass die Benutzeroberfläche nur einmal skaliert werden muss.

Außerdem verfügen viele Win32-APIs bei der Win32-Programmierung über keinen DPI- oder Anzeigekontext, sodass sie nur Werte relativ zum System-DPI zurückgeben. Es kann hilfreich sein, ihren Code zu durchgehren, um nach einigen dieser APIs zu suchen und sie durch DPI-orientierte Varianten zu ersetzen. Einige der gängigen APIs, die über DPI-orientierte Varianten verfügen, sind:



| Einzelne DPI-Version   | Per-Monitor Version        |
|----------------------|----------------------------|
| Getsystemmetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| Systemparametersinfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

Es ist auch eine gute Idee, in Ihrer Codebasis nach hart codierten Größen zu suchen, die von einem konstanten DPI ausgehen, und diese durch Code zu ersetzen, der die DPI-Skalierung ordnungsgemäß abspricht. Im Folgenden finden Sie ein Beispiel, das alle diese Vorschläge enthält:

### <a name="example"></a>Beispiel:

Das folgende Beispiel zeigt einen vereinfachten Win32-Fall, bei dem ein untergeordnetes HWND erstellt wird. Beim Aufruf von CreateWindow wird davon ausgegangen, dass die Anwendung mit 96 DPI ausgeführt wird und weder die Größe noch die Position der Schaltfläche bei höheren DPIs korrekt ist:


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



Der folgende aktualisierte Code zeigt Folgendes:

1.  Der DPI-Code für die Fenstererstellung skaliert die Position und Größe des untergeordneten HWND für den DPI des übergeordneten Fensters.
2.  Reagieren auf DPI-Änderungen durch Neupositionieren und Ändern der Größe des untergeordneten HWND
3.  Hart codierte Größen wurden entfernt und durch Code ersetzt, der auf DPI-Änderungen reagiert.


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



Beim Aktualisieren einer System-DPI-orientierte Anwendung sind einige häufige Schritte zu befolgen:

1.  Markieren Sie den Prozess mithilfe eines Anwendungsmanifests (oder einer anderen Methode, je nach verwendeten Benutzeroberflächenframeworks) als monitorspezifische dPI-bewusst (V2).
2.  Machen Sie die Layoutlogik der Benutzeroberfläche wiederverwendbar, und verschieben Sie sie aus dem Anwendungsin initialisierungscode, damit sie wiederverwendet werden kann, wenn eine DPI-Änderung auftritt (WM DPICHANGED im Fall der \_ Windows (Win32)-Programmierung).
3.  Ungültiger Code, bei dem davon ausgegangen wird, dass DPI-sensible Daten (DPI/fonts/sizes/etc.) nie aktualisiert werden müssen. Es ist üblich, Schriftgrößen und DPI-Werte bei der Prozessin initialisierung zwischenspeichern. Wenn Eine Anwendung aktualisiert wird, um DPI-sensitiv zu werden, müssen DPI-sensible Daten neu ausgewertet werden, wenn ein neuer DPI-Wert gefunden wird.
4.  Wenn eine DPI-Änderung auftritt, laden Sie alle Bitmapressourcen für den neuen DPI erneut (oder rastern Sie sie neu), oder strecken Sie optional die aktuell geladenen Objekte auf die richtige Größe.
5.  Grep für APIs, die nicht Per-Monitor DPI-bewusst sind, und ersetzen Sie sie durch Per-Monitor DPI-orientierte APIs (falls zutreffend). Beispiel: Ersetzen Sie GetSystemMetrics durch GetSystemMetricsForDpi.
6.  Testen Sie Ihre Anwendung auf einem System mit mehreren Anzeige-/Mehrfach-DPI-Dateien.
7.  Verwenden Sie für alle Fenster der obersten Ebene in Ihrer Anwendung, die Sie nicht auf die ordnungsgemäße DPI-Skalierung aktualisieren können, die DPI-Skalierung im gemischten Modus (siehe unten), um bitmap stretching dieser Fenster der obersten Ebene durch das System zu ermöglichen.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode DPI-Skalierung (Subprozess-DPI-Skalierung)

Wenn Sie eine Anwendung aktualisieren, um die DPI-Unterstützung pro Monitor zu unterstützen, kann es manchmal unpraktisch oder unmöglich werden, jedes Fenster in der Anwendung auf einmal zu aktualisieren. Dies kann einfach an der Zeit und dem Aufwand zum Aktualisieren und Testen der benutzeroberfläche oder daran liegt, dass Sie nicht den ganzen Code der Benutzeroberfläche besitzen, den Sie ausführen müssen (wenn Ihre Anwendung möglicherweise die Benutzeroberfläche eines Drittanbieters lädt). In diesen Situationen bietet Windows eine Möglichkeit, sich in die Welt der Überwachung zu konzentrieren, indem Sie einige Ihrer Anwendungsfenster (nur auf oberster Ebene) in ihrem ursprünglichen DPI-Bewusstseinsmodus ausführen können, während Sie ihre Zeit und Energie auf die wichtigeren Teile Ihrer Benutzeroberfläche konzentrieren.

Im Folgenden wird veranschaulicht, wie dies aussehen könnte: Sie aktualisieren die Hauptanwendungsbenutzeroberfläche ("Hauptfenster" in der Abbildung), damit sie mit DPI-Kenntnis pro Monitor ausgeführt wird, während Sie andere Fenster im vorhandenen Modus ausführen ("Sekundäres Fenster").

![Unterschiede bei der DPI-Skalierung zwischen Denkmodi](images/hub-page-illustrations.png)

Vor dem Windows 10 Anniversary Update (1607) war der DPI-Bewusstseinsmodus eines Prozesses eine prozessweite Eigenschaft. Ab dem Windows 10 Anniversary Update kann diese Eigenschaft jetzt pro Fenster der **obersten Ebene festgelegt** werden. (**Untergeordnete** Fenster müssen weiterhin mit der Skalierungsgröße ihres übergeordneten Elements übereinstimmen.) Ein Fenster der obersten Ebene wird als Fenster ohne übergeordnetes Element definiert. Dies ist in der Regel ein "normales" Fenster mit Schaltflächen zum Minimieren, Maximieren und Schließen. Das Szenario, für das das Subprozess-DPI-Bewusstsein vorgesehen ist, besteht im Skalieren der sekundären Benutzeroberfläche durch Windows (Bitmap-Stretching), während Sie ihre Zeit und Ressourcen auf die Aktualisierung Ihrer primären Benutzeroberfläche konzentrieren.

Rufen Sie [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) vor und nach jedem Aufruf der Fenstererstellung auf, um das DPI-Bewusstsein für untergeordnete Prozesse zu aktivieren. Das erstellte Fenster wird dem DPI-Bewusstsein zugeordnet, das Sie über SetThreadDpiAwarenessContext festlegen. Verwenden Sie den zweiten Aufruf, um die DPI-Kenntnis des aktuellen Threads wiederherzustellen.

Durch die Verwendung der DPI-Skalierung unter einem Prozess können Sie sich zwar auf Windows verlassen, um einen Teil der DPI-Skalierung für Ihre Anwendung zu nutzen, aber dies kann die Komplexität Ihrer Anwendung erhöhen. Es ist wichtig, dass Sie die Nachteile dieses Ansatzes und die Komplexität verstehen, die er mit sich bringt. Weitere Informationen zum Erkennen von DPI-Unterprozessen finden Sie unter DPI-Skalierung im gemischten Modus [und DPI-orientierte APIs.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Testen Ihrer Änderungen

Nachdem Sie Ihre Anwendung aktualisiert haben, um die DPI-Leistung pro Monitor zu überwachen, ist es wichtig, zu überprüfen, ob Ihre Anwendung ordnungsgemäß auf DPI-Änderungen in einer Mixed DPI-Umgebung reagiert. Zu den zu testden Besonderheiten gehören:

1.  Verschieben von Anwendungsfenstern zwischen Anzeigeanzeigen mit unterschiedlichen DPI-Werten
2.  Starten der Anwendung auf Anzeigen verschiedener DPI-Werte
3.  Ändern des Skalierungsfaktors für Ihren Monitor, während die Anwendung ausgeführt wird
4.  Ändern der Anzeige, die Sie als primäre Anzeige _verwenden,_ Abwahl von Windows und anschließendes erneutes Testen Ihrer Anwendung nach der Anmeldung. Dies ist besonders nützlich bei der Suche nach Code, der hart codierte Größen/Dimensionen verwendet.

## <a name="common-pitfalls-win32"></a>Häufige Fallstricke (Win32)

**Nichtverwendung des vorgeschlagenen Rechtecks, das in WM \_ DPICHANGED bereitgestellt wird**

Wenn Windows dem Anwendungsfenster eine [**\_ WM-DPICHANGED-Nachricht**](wm-dpichanged.md) sendet, enthält diese Nachricht ein vorgeschlagenes Rechteck, das Sie zum Ändern der Fenstergröße verwenden sollten. Es ist wichtig, dass Ihre Anwendung dieses Rechteck verwendet, um die Größe selbst zu ändern, wie dies geschieht:

1.  Stellen Sie sicher, dass sich der Mauszeiger beim Ziehen zwischen den Anzeigen in der gleichen relativen Position im Fenster befindet.
2.  Verhindern Sie, dass das Anwendungsfenster in einen rekursiven DPI-Änderungszyklus wechselt, bei dem eine DPI-Änderung eine nachfolgende DPI-Änderung auslöst, wodurch eine weitere DPI-Änderung ausgelöst wird.

Wenn Sie anwendungsspezifische Anforderungen haben, die sie daran hindern, das vorgeschlagene Rechteck zu verwenden, das Windows in der WM \_ DPICHANGED-Nachricht bereitstellt, finden Sie weitere Informationen unter [**WM \_ GETDPISCALEDSIZE.**](wm-getdpiscaledsize.md) Diese Meldung kann verwendet werden, um Windows eine gewünschte Größe zuzuweisen, sobald die DPI-Änderung erfolgt ist, und gleichzeitig die oben beschriebenen Probleme zu vermeiden.

**Fehlende Dokumentation zur Virtualisierung**

Wenn ein HWND- oder Prozess entweder als DPI-nicht bekannt oder system-DPI-fähigen ausgeführt wird, kann es durch Windows gestreckt werden. In diesem Fall skaliert Windows DPI-sensible Informationen von einigen APIs in den Koordinatenraum des aufrufenden Threads und konvertiert sie. Wenn z. B. ein DPI-nicht bekannter Thread die Bildschirmgröße abfragt, während er auf einer Anzeige mit hohem DPI-Anteil ausgeführt wird, virtualisiert Windows die an die Anwendung übergebene Antwort so, als ob sich der Bildschirm in 96 DPI-Einheiten befing. Wenn ein System-DPI-fähigen Thread mit einer Anzeige an einem anderen DPI interagiert, als beim Starten der Sitzung des aktuellen Benutzers verwendet wurde, skaliert Windows alternativ einige API-Aufrufe in den Koordinatenbereich, den der HWND verwenden würde, wenn er mit seinem ursprünglichen DPI-Skalierungsfaktor ausgeführt würde.

Wenn Sie Ihre Desktopanwendung ordnungsgemäß auf die DPI-Skalierung aktualisieren, kann es schwierig zu wissen, welche API-Aufrufe virtualisierte Werte basierend auf dem Threadkontext zurückgeben können. Diese Informationen werden von Microsoft derzeit nicht ausreichend dokumentiert. Beachten Sie Folgendes: Wenn Sie eine System-API aus einem DPI-fähigen oder system-DPI-fähigen Threadkontext aufrufen, kann der Rückgabewert virtualisiert werden. Stellen Sie daher sicher, dass Ihr Thread im DPI-Kontext ausgeführt wird, den Sie bei der Interaktion mit dem Bildschirm oder einzelnen Fenstern erwarten. Wenn Sie den DPI-Kontext eines Threads vorübergehend mit [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)ändern, stellen Sie sicher, dass Sie den alten Kontext wiederherstellen, wenn Sie fertig sind, um ein falsches Verhalten an anderer Stelle in Ihrer Anwendung zu vermeiden.

**Viele Windows-APIs haben keinen DPI-Kontext**

Viele Legacy-Windows-APIs enthalten keinen DPI- oder HWND-Kontext als Teil ihrer Schnittstelle. Daher müssen Entwickler häufig zusätzliche Arbeit leisten, um die Skalierung von DPI-vertraulichen Informationen wie Größen, Punkten oder Symbolen zu verarbeiten. Beispielsweise müssen Entwickler, die [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) verwenden, entweder geladene Bitmapsymbole gestreckt oder alternative APIs verwenden, um symbole der richtigen Größe für den entsprechenden DPI zu laden, z. B. [LoadImage.](/windows/desktop/api/winuser/nf-winuser-loadimagew)

**Erzwungenes Zurücksetzen prozessweiter DPI-Informationen**

Im Allgemeinen kann der DPI-Erkennungsmodus Ihres Prozesses nach der Prozessinitialisierung nicht mehr geändert werden. Windows können jedoch den DPI-Wahrnehmungsmodus Ihres Prozesses ändern, wenn Sie versuchen, die Anforderung zu unterbrechen, dass alle HWNDs in einer Fensterstruktur denselben DPI-Wahrnehmungsmodus aufweisen. Ab Windows 10 1703 ist es in allen Versionen von Windows nicht möglich, unterschiedliche HWNDs in einer HWND-Struktur in verschiedenen DPI-Wahrnehmungsmodi auszuführen. Wenn Sie versuchen, eine untergeordnete und übergeordnete Beziehung zu erstellen, die diese Regel unterbricht, kann die DPI-Kenntnis des gesamten Prozesses zurückgesetzt werden. Dies kann durch Dies ausgelöst werden:

1.  Ein CreateWindow-Aufruf, bei dem das übergebene übergeordnete Fenster einen anderen DPI-Wahrnehmungsmodus als der aufrufende Thread hat.
2.  Ein SetParent-Aufruf, bei dem die beiden Fenster verschiedenen DPI-Wahrnehmungsmodi zugeordnet sind.

Die folgende Tabelle zeigt, was geschieht, wenn Sie versuchen, gegen diese Regel zu verstoßen:



| Vorgang                 | Windows 8.1                                  | Windows 10 (1607 und früher)                | Windows 10 (1703 und höher)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (In-Proc)    | –                                          | **Untergeordnete Erben** (gemischter Modus)              | **Untergeordnete Erben** (gemischter Modus)              |
| CreateWindow (Prozessübergreifend) | **Erzwungenes Zurücksetzen** (des Prozesses des Aufrufers)       | **Untergeordnete Erben** (gemischter Modus)              | **Erzwungenes Zurücksetzen** (des Prozesses des Aufrufers)       |
| SetParent (In-Proc)       | –                                          | **Erzwungenes Zurücksetzen** (des aktuellen Prozesses)        | **Fehler** (FEHLER \_ UNGÜLTIGER \_ ZUSTAND)             |
| SetParent (Prozessübergreifend)    | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Api-Referenz zu hohen DPI-Daten](high-dpi-reference.md)
</dt> <dt>

[DPI-Skalierung im gemischten Modus und DPI-fähige APIs.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

