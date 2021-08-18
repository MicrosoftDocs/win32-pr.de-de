---
title: Entwicklung von Desktopanwendungen mit hohem DPI-Windows
description: Dieser Inhalt richtet sich an Entwickler, die Desktopanwendungen aktualisieren möchten, um den dynamischen Anzeigeskalierfaktor (auch als
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6389553ce2265752e3552fdaaf848e3ac70eede8df3b4fd9e560861bf15f33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036252"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Entwicklung von Desktopanwendungen mit hohem DPI-Windows

Dieser Inhalt richtet sich an Entwickler, die Desktopanwendungen aktualisieren möchten, um Änderungen des Anzeigeskalierfaktors (Punkte pro Zoll oder DPI) dynamisch zu verarbeiten, sodass ihre Anwendungen auf jeder Anzeige, auf der sie gerendert werden, klar sein können.

Wenn Sie eine neue Windows-App von Grund auf neu erstellen, wird dringend empfohlen, eine [UWP-Anwendung (Universelle](/windows/uwp/get-started/whats-a-uwp) Windows-Plattform) zu erstellen. UWP-Anwendungen werden automatisch und dynamisch für jede Anzeige skaliert, &mdash; auf der sie ausgeführt &mdash; werden.

Desktopanwendungen, die ältere Windows-Programmiertechnologien (unformatiert win32-Programmierung, Windows Forms, Windows Presentation Framework (WPF) usw.) verwenden, können die DPI-Skalierung ohne zusätzliche Entwicklerarbeit nicht automatisch verarbeiten. Ohne diese Arbeit erscheinen Anwendungen in vielen gängigen Verwendungsszenarien unscharf oder falsch dimensioniert. Dieses Dokument enthält Kontext und Informationen dazu, was an der Aktualisierung einer Desktopanwendung beteiligt ist, damit sie ordnungsgemäß gerendert wird.

## <a name="display-scale-factor--dpi"></a>Anzeigen des Skalierungsfaktors & DPI

Im Verlauf der Entwicklung der Anzeigetechnologie haben Hersteller von Anzeigepanels eine zunehmende Anzahl von Pixeln in jede Einheit des physischen Raums auf ihren Panels gepackt. Dies hat dazu führen, dass die DPI-Punkte (Dots per Inch) moderner Anzeigepanels viel höher sind als in der Vergangenheit. In der Vergangenheit hatten die meisten Anzeigen 96 Pixel pro linearem Zoll physischen Raum (96 DPI). im Jahr 2017 sind Displays mit fast 300 DPI oder höher sofort verfügbar.

Die meisten Legacy-Desktopbenutzeroberflächenframeworks verfügen über integrierte Annahmen, dass sich der Anzeige-DPI während der Lebensdauer des Prozesses nicht ändert.  Diese Annahme gilt nicht mehr, da sich Anzeige-DPIs während der Lebensdauer eines Anwendungsprozesses häufig mehrmals ändern. Einige häufige Szenarien, in denen sich der Skalierungsfaktor/DPI-Anzeigefaktor ändert, sind:

-   Setups mit mehreren Monitoren, bei denen jede Anzeige über einen anderen Skalierungsfaktor verfügt und die Anwendung von einer Anzeige auf eine andere verschoben wird (z. B. eine 4K- und eine 1080p-Anzeige).
-   Andocken und Abdocken eines Laptops mit hohem DPI-Wert mit einem externen Display mit geringem DPI-Wert (oder umgekehrt)
-   Herstellen einer Verbindung Remotedesktop von einem Laptop/Tablet mit hohem DPI-Wert mit einem Gerät mit geringem DPI-Wert (oder umgekehrt)
-   Ändern der Einstellungen für den Anzeigeskalierenfaktor, während Anwendungen ausgeführt werden

In diesen Szenarien werden UWP-Anwendungen automatisch für den neuen DPI neu gezeichnet. Standardmäßig und ohne zusätzliche Entwicklerarbeit werden Desktopanwendungen nicht verwendet. Desktopanwendungen, die diese zusätzliche Arbeit nicht zum Reagieren auf DPI-Änderungen vornehmen, können für den Benutzer unscharf oder falsch dimensioniert erscheinen.

## <a name="dpi-awareness-mode"></a>DPI-Bewusstseinsmodus

Desktopanwendungen müssen Windows, ob sie die DPI-Skalierung unterstützen. Standardmäßig berücksichtigt das System Desktopanwendungen als DPI nicht und streckt ihre Fenster durch Bitmaps. Durch Festlegen eines der folgenden verfügbaren DPI-Bewusstseinsmodi können Anwendungen explizit Windows, wie sie die DPI-Skalierung behandeln möchten:

### <a name="dpi-unaware"></a>DPI nicht bekannt

Nicht DPI-anwendungen werden mit einem festen DPI-Wert von 96 (100 %) gerendert. Wenn diese Anwendungen auf einem Bildschirm mit einer Anzeigeskala von mehr als 96 DPI ausgeführt werden, streckt Windows die Anwendungsbitmap auf die erwartete physische Größe. Dies führt dazu, dass die Anwendung unscharf erscheint.

### <a name="system-dpi-awareness"></a>System-DPI-Bewusstsein

Desktopanwendungen mit System-DPI-Unterstützung erhalten in der Regel die DPI des primären verbundenen Monitors zum Zeitpunkt der Benutzeranmeldezeit. Während der Initialisierung wird die Benutzeroberfläche mithilfe dieses System-DPI-Werts entsprechend angepasst (Größensteuerelemente, Auswahl von Schriftgraden, Laden von Ressourcen usw.). Daher werden DPI-orientierte Systemanwendungen nicht durch DPI skaliert (Bitmap gestreckt) Windows auf Anzeigen, die mit diesem einzelnen DPI gerendert werden. Wenn die Anwendung auf eine Anzeige mit einem anderen Skalierungsfaktor verschoben wird oder sich der Anzeigeskalierenfaktor andernfalls ändert, skaliert Windows die Fenster der Anwendung in bitmaps, wodurch sie unscharf erscheinen. System-DPI-orientierte Desktopanwendungen rendern effektiv nur mit einem einzigen Anzeigeskalierenfaktor und werden unscharf, wenn sich der DPI ändert.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor und Per-Monitor (V2) DPI Awareness

Es wird empfohlen, Desktopanwendungen so zu aktualisieren, dass sie den DPI-Bewusstseinsmodus pro Monitor verwenden, sodass sie sofort ordnungsgemäß gerendert werden können, wenn sich der DPI ändert. Wenn eine Anwendung meldet Windows dass sie in diesem Modus ausgeführt werden soll, streckt Windows die Anwendung nicht per Bitmap, wenn sich der DPI ändert, sondern sendet [stattdessen WM \_ DPICHANGED](wm-dpichanged.md) an das Anwendungsfenster. Es liegt dann in der vollständigen Verantwortung der Anwendung, die Größenverstellung für den neuen DPI selbst zu verarbeiten. Die meisten benutzeroberflächenframeworks, die von Desktopanwendungen (Windows gängigen Steuerelementen (comctl32), Windows Forms, Windows Presentation Framework usw.) verwendet werden, unterstützen keine automatische DPI-Skalierung. Entwickler müssen die Größe ihrer Fenster selbst ändern und deren Inhalt neu positionieren.

Es gibt zwei Versionen von Per-Monitor, dass sich eine Anwendung als registrieren kann: Version 1 und Version 2 (PMv2). Das Registrieren eines Prozesses als Ausführung im PMv2-Bewusstseinsmodus führt zu:

1.  Die Anwendung, die benachrichtigt wird, wenn sich der DPI ändert (sowohl die HWNDs der obersten Ebene als auch die untergeordneten HWNDs).
2.  Die Anwendung zeigt die unformatten Pixel jeder Anzeige an.
3.  Die Anwendung wird nie per Bitmap skaliert Windows
4.  Automatischer Nicht-Clientbereich (Fensterbeschriftung, Scrollleisten usw.) DPI-Skalierung nach Windows
5.  Win32-Dialoge [(von CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) automatisch DPI skaliert durch Windows
6.  Bitmapressourcen mit Designdesign in allgemeinen Steuerelementen (Kontrollkästchen, Schaltflächenhintergrund usw.), die automatisch mit dem entsprechenden DPI-Skalierungsfaktor gerendert werden

Bei der Ausführung im Per-Monitor v2-Benachrichtigungsmodus werden Anwendungen benachrichtigt, wenn sich ihr DPI geändert hat. Wenn sich die Größe einer Anwendung für den neuen DPI nicht ändert, wird die Benutzeroberfläche der Anwendung zu klein oder zu groß angezeigt (je nach Unterschied in den vorherigen und neuen DPI-Werten).

> [!Note]  
> Per-Monitor V1 (PMv1) ist sehr eingeschränkt. Es wird empfohlen, dass Anwendungen PMv2 verwenden.

Die folgende Tabelle zeigt, wie Anwendungen unter verschiedenen Szenarien gerendert werden:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>DPI-Bewusstseinsmodus</th>
<th>Windows Eingeführte Version</th>
<th>DPI-Ansicht der Anwendung</th>
<th>Verhalten bei DPI-Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nicht bekannt</td>
<td>Nicht zutreffend</td>
<td>Alle Anzeigen sind 96 DPI</td>
<td>Bitmapstreckung (unscharf)</td>
</tr>
<tr class="even">
<td>System</td>
<td>Vista</td>
<td>Alle Anzeigen verfügen über den gleichen DPI-Status (DPI der primären Anzeige zum Zeitpunkt des Startes der aktuellen Benutzersitzung).</td>
<td>Bitmapstreckung (unscharf)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>DPI der Anzeige, auf der sich das Anwendungsfenster hauptsächlich befindet</td>
<td><ul>
<li>HWND der obersten Ebene wird über DPI-Änderungen benachrichtigt</li>
<li>Keine DPI-Skalierung von Benutzeroberflächenelementen.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>DPI der Anzeige, auf der sich das Anwendungsfenster hauptsächlich befindet</td>
<td><ul>
<li>HWNDs der <span class="underline">obersten</span> Ebene und untergeordneten HWNDs werden über DPI-Änderungen benachrichtigt.</li>
</ul>
<br/> <span class="underline">Automatische DPI-Skalierung von:</span>
<ul>
<li>Nicht-Clientbereich</li>
<li>Design gezeichnete Bitmaps in gängigen Steuerelementen (comctl32 V6)</li>
<li>Dialoge (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>DPI-Bewusstsein pro Monitor (V1)

Per-Monitor V1 DPI Awareness Mode (PMv1) wurde mit Windows 8.1. Dieser DPI-Bewusstseinsmodus ist sehr begrenzt und bietet nur die unten aufgeführten Funktionen. Es wird empfohlen, dass Desktopanwendungen Per-Monitor v2-Awareness-Modus verwenden, der für Windows 10 1703 oder höher unterstützt wird.

Die anfängliche Unterstützung für monitorspezifisches Bewusstsein bot nur Anwendungen Folgendes:

1.  HWNDs der obersten Ebene werden über eine DPI-Änderung benachrichtigt und stellen eine neue vorgeschlagene Größe zur Verfügung.
2.  Windows die Benutzeroberfläche der Anwendung wird nicht gestreckt.
3.  Die Anwendung sieht alle Anzeigen in physischen Pixeln (siehe Virtualisierung).

In Windows 10 1607 oder höher können PMv1-Anwendungen während WM NCCREATE auch [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) aufrufen, um an fordern, dass Windows den Nicht-Clientbereich des Fensters ordnungsgemäß \_ skaliert.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Unterstützung der DPI-Skalierung pro Monitor nach UI-Framework/-Technologie

Die folgende Tabelle zeigt den Grad der DPI-Unterstützung pro Monitor, der von verschiedenen Frameworks für Windows-Benutzeroberfläche ab Windows 10 1703 angeboten wird:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Framework/Technologie</th>
<th>Support</th>
<th>Betriebssystemversion</th>
<th>DPI-Skalierung, die von</th>
<th>Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Universelle Windows-Plattform (UWP)</td>
<td>Vollständig</td>
<td>1607</td>
<td>Benutzeroberflächenframework</td>
<td><a href="/windows/uwp/get-started/whats-a-uwp">Universelle Windows-Plattform (UWP)</a></td>
</tr>
<tr class="even">
<td>Unformatierte Win32/Common Controls V6 (comctl32.dll)</td>
<td><ul>
<li>DPI-Änderungsbenachrichtigungsmeldungen, die an alle HWNDs gesendet werden</li>
<li>Designgezeichnete Objekte werden in gängigen Steuerelementen ordnungsgemäß gerendert.</li>
<li>Automatische DPI-Skalierung für Dialoge</li>
</ul></td>
<td>1703</td>
<td>Anwendung</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Beispiel</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Eingeschränkte automatische DPI-Skalierung pro Monitor für einige Steuerelemente</td>
<td>1703</td>
<td>Benutzeroberflächenframework</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Unterstützung hoher DPI-Daten in Windows Forms</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Native WPF-Anwendungen skalieren WPF, das in anderen Frameworks gehostet wird, und andere in WPF gehostete Frameworks werden nicht automatisch skaliert.</td>
<td>1607</td>
<td>Benutzeroberflächenframework</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Beispiel</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>Keine</td>
<td>–</td>
<td>Anwendung</td>
<td>Weitere Informationen finden Sie unter <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling (GDI-Skalierung mit hohem DPI-Anteil).</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>Keine</td>
<td>–</td>
<td>Anwendung</td>
<td>Weitere Informationen finden Sie unter <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI Scaling (GDI-Skalierung mit hohem DPI-Anteil).</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>Keine</td>
<td>–</td>
<td>Anwendung</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Aktualisieren bestehender Anwendungen

Um eine vorhandene Desktopanwendung so zu aktualisieren, dass sie die DPI-Skalierung ordnungsgemäß verarbeitet, muss sie so aktualisiert werden, dass mindestens die wichtigen Teile der Benutzeroberfläche aktualisiert werden, um auf DPI-Änderungen zu reagieren.

Die meisten Desktopanwendungen werden im DPI-Systemerkennungsmodus ausgeführt. System-DPI-fähige Anwendungen werden in der Regel auf den DPI der primären Anzeige skaliert (die Anzeige, auf der sich die Taskleiste zum Zeitpunkt des Startens der Windows Sitzung befand). Wenn sich der DPI ändert, gestreckt Windows die Benutzeroberfläche dieser Anwendungen durch Bitmaps, was häufig dazu führt, dass sie unscharf sind. Wenn eine System-DPI-fähige Anwendung aktualisiert wird, um monitor-DPI-fähige Anwendungen zu erhalten, muss der Code, der das Benutzeroberflächenlayout behandelt, so aktualisiert werden, dass er nicht nur während der Anwendungsinitialisierung ausgeführt wird, sondern auch, wenn eine DPI-Änderungsbenachrichtigung[(WM \_ DPICHANGED](wm-dpichanged.md) im Fall von Win32) empfangen wird. Dies umfasst in der Regel die erneute Überprüfung aller Annahmen im Code, dass die Benutzeroberfläche nur einmal skaliert werden muss.

Im Fall der Win32-Programmierung verfügen viele Win32-APIs über keinen DPI- oder Anzeigekontext, sodass sie nur Werte relativ zum System-DPI zurückgeben. Es kann hilfreich sein, ihren Code zu durchsuchen, um nach einigen dieser APIs zu suchen und sie durch DPI-fähige Varianten zu ersetzen. Einige der gängigen APIs mit DPI-fähigen Varianten sind:



| Einzelne DPI-Version   | Per-Monitor Version        |
|----------------------|----------------------------|
| Getsystemmetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| Systemparametersinfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

Es empfiehlt sich auch, in Ihrer Codebasis nach hart codierten Größen zu suchen, die von einem konstanten DPI ausgehen, und sie durch Code zu ersetzen, der die DPI-Skalierung ordnungsgemäß einberechnen. Im Folgenden finden Sie ein Beispiel, das alle diese Vorschläge enthält:

### <a name="example"></a>Beispiel:

Das folgende Beispiel zeigt einen vereinfachten Win32-Fall zum Erstellen eines untergeordneten HWND. Beim Aufruf von CreateWindow wird davon ausgegangen, dass die Anwendung mit 96 DPI ausgeführt wird und weder die Größe noch die Position der Schaltfläche bei höheren DPIs korrekt ist:


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



Der aktualisierte Code unten zeigt Folgendes:

1.  Der DPI für die Fenstererstellungscodeskalierung der Position und Größe des untergeordneten HWND für den DPI des übergeordneten Fensters
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



Beim Aktualisieren einer System-DPI-fähigen Anwendung sind einige gängige Schritte zu befolgen:

1.  Markieren Sie den Prozess mithilfe eines Anwendungsmanifests (oder einer anderen Methode, abhängig von den verwendeten Benutzeroberflächenframeworks) als monitorabhängige DPI-fähige (V2)-Methode.
2.  Machen Sie die Benutzeroberflächenlayoutlogik wiederverwendbar, und verschieben Sie sie aus dem Anwendungsinitialisierungscode, sodass sie wiederverwendet werden kann, wenn eine DPI-Änderung auftritt (WM \_ DPICHANGED im Fall von Windows (Win32)-Programmierung).
3.  Macht Code ungültig, der annimmt, dass DPI-sensible Daten (DPI/fonts/sizes/etc.) nie aktualisiert werden müssen. Es ist sehr üblich, Schriftgrade und DPI-Werte bei der Prozessinitialisierung zwischenzuspeichern. Wenn eine Anwendung aktualisiert wird, um monitorspezifische DPI-fähige Daten zu erhalten, müssen DPI-sensible Daten immer dann neu ausgewertet werden, wenn ein neuer DPI gefunden wird.
4.  Wenn eine DPI-Änderung auftritt, laden Sie alle Bitmapressourcen für den neuen DPI neu (oder rastern Sie sie erneut), oder strecken Sie optional die aktuell geladenen Objekte auf die richtige Größe.
5.  Grep für APIs, die nicht Per-Monitor DPI-fähigen sind, und ersetzen sie durch Per-Monitor DPI-fähige APIs (falls zutreffend). Beispiel: Ersetzen Sie GetSystemMetrics durch GetSystemMetricsForDpi.
6.  Testen Sie Ihre Anwendung auf einem Mehrfachanzeige-/Multi-DPI-System.
7.  Verwenden Sie für alle Fenster der obersten Ebene in Ihrer Anwendung, die Sie nicht auf die richtige DPI-Skalierung aktualisieren können, die DPI-Skalierung im gemischten Modus (siehe unten), um bitmap-Stretching dieser Fenster der obersten Ebene durch das System zu ermöglichen.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode DPI-Skalierung (Subprozess-DPI-Skalierung)

Beim Aktualisieren einer Anwendung zur Unterstützung der DPI-Überwachung pro Monitor kann es manchmal unpraktisch oder unmöglich werden, jedes Fenster in der Anwendung auf einmal zu aktualisieren. Dies kann einfach auf die Zeit und den Aufwand zurückzuführen sein, die erforderlich sind, um die gesamte Benutzeroberfläche zu aktualisieren und zu testen, oder weil Sie nicht den gesamten Ui-Code besitzen, den Sie ausführen müssen (wenn Ihre Anwendung möglicherweise die Benutzeroberfläche von Drittanbietern lädt). In diesen Situationen bietet Windows eine Möglichkeit, sich in die Welt der Pro-Monitor-Wahrnehmung zu versetzen, indem Sie einige Ihrer Anwendungsfenster (nur auf oberster Ebene) im ursprünglichen DPI-Awareness-Modus ausführen können, während Sie Ihre Zeit und Energie auf die wichtigeren Teile der Benutzeroberfläche konzentrieren.

Im Folgenden wird veranschaulicht, wie dies aussehen könnte: Sie aktualisieren die Benutzeroberfläche der Hauptanwendung ("Hauptfenster" in der Abbildung), damit sie mit DPI-Informationen pro Monitor ausgeführt wird, während Sie andere Fenster im vorhandenen Modus ausführen ("Sekundäres Fenster").

![Unterschiede bei der DPI-Skalierung zwischen Denkmodi](images/hub-page-illustrations.png)

Vor dem Windows 10 Anniversary Update (1607) war der DPI-Awareness-Modus eines Prozesses eine prozessweite Eigenschaft. Ab Windows 10 Anniversary Update kann diese Eigenschaft jetzt pro Fenster der **obersten Ebene** festgelegt werden. (**Untergeordnete** Fenster müssen weiterhin der Skalierungsgröße ihres übergeordneten Elements entsprechen.) Ein Fenster der obersten Ebene wird als Fenster ohne übergeordnetes Element definiert. Dies ist in der Regel ein "reguläres" Fenster mit Schaltflächen zum Minimieren, Maximieren und Schließen. Das Szenario, für das die DPI-Unterprozesserkennung vorgesehen ist, besteht darin, die sekundäre Benutzeroberfläche durch Windows (Bitmap gestreckt) zu skalieren, während Sie Ihre Zeit und Ressourcen auf die Aktualisierung Ihrer primären Benutzeroberfläche konzentrieren.

Um die DPI-Unterprozesserkennung zu aktivieren, rufen [**Sie SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) vor und nach allen Aufrufen der Fenstererstellung auf. Das fenster, das erstellt wird, wird der DPI-Kenntnis zugeordnet, die Sie über SetThreadDpiAwarenessContext festlegen. Verwenden Sie den zweiten Aufruf, um die DPI-Kenntnis des aktuellen Threads wiederherzustellen.

Wenn Sie die DPI-Skalierung des Untergeordneten Prozesses verwenden, können Sie sich auf Windows verlassen, um einen Teil der DPI-Skalierung für Ihre Anwendung zu erledigen. Dies kann die Komplexität Ihrer Anwendung erhöhen. Es ist wichtig, dass Sie die Nachteile dieses Ansatzes und die Komplexität verstehen, die er einführt. Weitere Informationen zur DPI-Unterprozesserkennung finden Sie unter [DPI-Skalierung im gemischten Modus und DPI-fähige APIs.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Testen Ihrer Änderungen

Nachdem Sie Ihre Anwendung so aktualisiert haben, dass sie monitorspezifische DPI-bezogene Daten erkennt, ist es wichtig zu überprüfen, ob Ihre Anwendung ordnungsgemäß auf DPI-Änderungen in einer Gemischt-DPI-Umgebung reagiert. Zu testspezifischen Merkmalen gehören:

1.  Verschieben von Anwendungsfenstern zwischen Anzeigen unterschiedlicher DPI-Werte
2.  Starten der Anwendung auf Anzeigen unterschiedlicher DPI-Werte
3.  Ändern des Skalierungsfaktors für Ihren Monitor während der Ausführung der Anwendung
4.  Ändern der Anzeige, die Sie als primäre Anzeige verwenden, _Abmelden von Windows_ und erneutes Testen Ihrer Anwendung nach der anmeldung. Dies ist besonders nützlich bei der Suche nach Code, der hart codierte Größen/Dimensionen verwendet.

## <a name="common-pitfalls-win32"></a>Häufige Fehler (Win32)

**Das vorgeschlagene Rechteck, das in WM DPICHANGED bereitgestellt wird, wird nicht verwendet. \_**

Wenn Windows dem Anwendungsfenster eine [**\_ WM-DPICHANGED-Nachricht**](wm-dpichanged.md) sendet, enthält diese Nachricht ein vorgeschlagenes Rechteck, das Sie zum Ändern der Fenstergröße verwenden sollten. Es ist wichtig, dass Ihre Anwendung dieses Rechteck verwendet, um die Größe selbst zu ändern, wie dies geschieht:

1.  Stellen Sie sicher, dass sich der Mauszeiger beim Ziehen zwischen den Anzeigen in der gleichen relativen Position im Fenster befindet.
2.  Verhindern Sie, dass das Anwendungsfenster in einen rekursiven DPI-Änderungszyklus wechselt, bei dem eine DPI-Änderung eine nachfolgende DPI-Änderung auslöst, wodurch eine weitere DPI-Änderung ausgelöst wird.

Wenn Sie anwendungsspezifische Anforderungen haben, die sie daran hindern, das vorgeschlagene Rechteck zu verwenden, das Windows in der \_ WM-DPICHANGED-Nachricht bereitstellt, finden Sie weitere Informationen unter [**WM \_ GETDPISCALEDSIZE.**](wm-getdpiscaledsize.md) Diese Meldung kann verwendet werden, um Windows nach der DPI-Änderung eine gewünschte Größe zuzuweisen und gleichzeitig die oben beschriebenen Probleme zu vermeiden.

**Fehlende Dokumentation zur Virtualisierung**

Wenn ein HWND- oder Prozess entweder als DPI-unwissend oder systemdepi-fähigen Prozess ausgeführt wird, kann die Bitmap durch Windows gestreckt werden. In diesem Fall skaliert Windows DPI-sensible Informationen von einigen APIs in den Koordinatenraum des aufrufenden Threads und konvertiert sie. Wenn z. B. ein DPI-nicht bekannter Thread die Bildschirmgröße abfragt, während er auf einer Anzeige mit hohem DPI-Anteil ausgeführt wird, virtualisiert Windows die Antwort an die Anwendung so, als ob der Bildschirm 96 DPI-Einheiten aufwies. Wenn ein System-DPI-fähigen Thread mit einer Anzeige mit einem anderen DPI interagiert, als beim Starten der Sitzung des aktuellen Benutzers verwendet wurde, skaliert Windows alternativ einige API-Aufrufe in den Koordinatenbereich, den der HWND verwendet, wenn er mit seinem ursprünglichen DPI-Skalierungsfaktor ausgeführt wird.

Wenn Sie Ihre Desktopanwendung ordnungsgemäß auf die DPI-Skalierung aktualisieren, kann es schwierig zu wissen, welche API-Aufrufe virtualisierte Werte basierend auf dem Threadkontext zurückgeben können. Diese Informationen werden von Microsoft derzeit nicht ausreichend dokumentiert. Beachten Sie, dass der Rückgabewert virtualisiert werden kann, wenn Sie eine System-API aus einem DPI-fähigen oder system-DPI-fähigen Threadkontext aufrufen. Stellen Sie daher sicher, dass Ihr Thread im DPI-Kontext ausgeführt wird, den Sie bei der Interaktion mit dem Bildschirm oder einzelnen Fenstern erwarten. Wenn Sie den DPI-Kontext eines Threads vorübergehend mit [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)ändern, stellen Sie sicher, dass Sie den alten Kontext wiederherstellen, wenn Sie fertig sind, um zu vermeiden, dass an anderer Stelle in Ihrer Anwendung falsches Verhalten verursacht wird.

**Viele Windows-APIs haben keinen DPI-Kontext.**

Viele Legacy-Windows-APIs enthalten keinen DPI- oder HWND-Kontext als Teil ihrer Schnittstelle. Daher müssen Entwickler häufig zusätzliche Arbeit leisten, um die Skalierung von DPI-vertraulichen Informationen wie Größen, Punkten oder Symbolen zu verarbeiten. Beispielsweise müssen Entwickler, die [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) verwenden, entweder bitmapgeladene Symbole stretchen oder alternative APIs verwenden, um symbole der richtigen Größe für den entsprechenden DPI zu laden, z. B. [LoadImage.](/windows/desktop/api/winuser/nf-winuser-loadimagew)

**Erzwungenes Zurücksetzen prozessweiter DPI-Informationen**

Im Allgemeinen kann der DPI-Erkennungsmodus Ihres Prozesses nach der Prozessinitialisierung nicht mehr geändert werden. Windows können jedoch den DPI-Erkennungsmodus Ihres Prozesses ändern, wenn Sie versuchen, die Anforderung zu unterbrechen, dass alle HWNDs in einer Fensterstruktur denselben DPI-Wahrnehmungsmodus aufweisen. Ab Windows 10 1703 ist es in allen Versionen von Windows nicht möglich, unterschiedliche HWNDs in einer HWND-Struktur in verschiedenen DPI-Wahrnehmungsmodi auszuführen. Wenn Sie versuchen, eine untergeordnete und übergeordnete Beziehung zu erstellen, die diese Regel unterbricht, kann die DPI-Kenntnis des gesamten Prozesses zurückgesetzt werden. Dies kann durch Dies ausgelöst werden:

1.  Ein CreateWindow-Aufruf, bei dem das übergebene übergeordnete Fenster einen anderen DPI-Wahrnehmungsmodus als der aufrufende Thread hat.
2.  Ein SetParent-Aufruf, bei dem die beiden Fenster verschiedenen DPI-Wahrnehmungsmodi zugeordnet sind.

Die folgende Tabelle zeigt, was geschieht, wenn Sie versuchen, gegen diese Regel zu verstoßen:



| Vorgang                 | Windows 8.1                                  | Windows 10 (1607 und früher)                | Windows 10 (1703 und höher)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (In-Proc)    | Nicht zutreffend                                          | **Untergeordnete Erben** (gemischter Modus)              | **Untergeordnete Erben** (gemischter Modus)              |
| CreateWindow (Prozessübergreifend) | **Erzwungenes Zurücksetzen** (des Prozesses des Aufrufers)       | **Untergeordnete Erben** (gemischter Modus)              | **Erzwungenes Zurücksetzen** (des Prozesses des Aufrufers)       |
| SetParent (In-Proc)       | Nicht zutreffend                                          | **Erzwungenes Zurücksetzen** (des aktuellen Prozesses)        | **Fehler** (FEHLER \_ UNGÜLTIGER \_ ZUSTAND)             |
| SetParent (Prozessübergreifend)    | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) | **Erzwungenes Zurücksetzen** (des Prozesses des untergeordneten Fensters) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Api-Referenz zu hohen DPI-Daten](high-dpi-reference.md)
</dt> <dt>

[DPI-Skalierung im gemischten Modus und DPI-fähige APIs.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

