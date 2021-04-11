---
title: Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows
description: Dieser Inhalt richtet sich an Entwickler, die Desktop Anwendungen aktualisieren möchten, um den dynamischen Bildschirm Skalierungsfaktor (auch
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102486"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Hohe dpi-Entwicklung für Desktop Anwendungen unter Windows

Dieser Inhalt richtet sich an Entwickler, die Desktop Anwendungen aktualisieren möchten, um die Änderung der Anzeige Skalierungsfaktor (dpi, dpi, dpi, dpi) dynamisch durchzuführen, sodass Ihre Anwendungen auf jeder Anzeige, auf der Sie gerendert werden, auf einen Spitzenwert ausgerichtet werden.

Wenn Sie eine neue Windows-APP von Grund auf neu erstellen, empfiehlt es sich, eine universelle Windows-Plattform-Anwendung [(UWP)](/windows/uwp/get-started/whats-a-uwp) zu erstellen. UWP-Anwendungen &mdash; &mdash; werden für jede Anzeige, auf der Sie ausgeführt werden, automatisch und dynamisch skaliert.

Desktop Anwendungen, die ältere Windows-Programmiertechnologien verwenden (unformatierte Win32-Programmierung, Windows Forms, Windows Presentation Framework (WPF) usw.) können die DPI-Skalierung nicht automatisch verarbeiten, ohne dass zusätzliche Entwickler arbeiten müssen. Ohne diese Arbeit werden Anwendungen in vielen gängigen Verwendungs Szenarien verschwommen oder falsch formatiert. Dieses Dokument enthält Kontext und Informationen dazu, was beim Aktualisieren einer Desktop Anwendung zum ordnungsgemäßen Rendering beteiligt ist.

## <a name="display-scale-factor--dpi"></a>Skalierungsfaktor & dpi anzeigen

Wenn die Anzeige Technologie fortgeschritten ist, haben die Hersteller der Anzeige Bereiche eine wachsende Anzahl von Pixeln in jede Einheit von physischem Raum in ihren Bereichen gepackt. Dies hat zur Folge, dass die Punkte pro Zoll (dpi) moderner Anzeige Bereiche viel höher sind als in der Vergangenheit. In der Vergangenheit hatten die meisten Anzeige 96 Pixel pro linearer Zoll von physischem Speicher (96 dpi). in 2017 sind anzeigen mit fast 300 dpi oder höher sofort verfügbar.

Die meisten Legacy-Desktop Benutzeroberflächen-Frameworks verfügen über integrierte Annahmen, dass die Anzeige dpi während der Lebensdauer des Prozesses nicht geändert wird.  Diese Annahme ist nicht mehr true, und die Anzeige von DPIs ändert sich häufig mehrmals während der Lebensdauer eines Anwendungsprozesses. Einige häufige Szenarien, in denen die Anzeige Skalierungsfaktor/dpi-Änderungen:

-   Konfigurationen mit mehreren Monitoren, bei denen jede Anzeige einen anderen Skalierungsfaktor hat und die Anwendung von einer Anzeige in eine andere verschoben wird (z. b. ein 4K und eine 1080p-Anzeige)
-   Andocken und Andocken eines großen dpi-Laptops mit einer externen Anzeige mit niedriger dpi (oder umgekehrt)
-   Herstellen einer Verbindung über Remotedesktop von einem Laptop/Tablet mit hoher dpi-Verbindung mit einem Gerät mit geringer dpi (oder umgekehrt)
-   Ändern der Einstellungen für die Anzeige des Skalierungsfaktors während der Ausführung von Anwendungen

In diesen Szenarien zeichnen sich UWP-Anwendungen automatisch selbst für den neuen dpi-Abschnitt neu auf. Standardmäßig und ohne zusätzliche Entwickler Arbeit ist dies bei Desktop Anwendungen nicht der Fall. Desktop Anwendungen, die diese zusätzlichen Aufgaben nicht ausführen, um auf dpi-Änderungen zu reagieren, werden möglicherweise unscharf oder falsch für den Benutzer angezeigt.

## <a name="dpi-awareness-mode"></a>DPI-Awareness-Modus

Desktop Anwendungen müssen Windows informieren, wenn Sie die DPI-Skalierung unterstützen. Standardmäßig betrachtet das System Desktop Anwendungen mit dpi-Wert und Bitmap. Wenn Sie einen der folgenden verfügbaren dpi-Awareness-Modi festlegen, können die Anwendungen explizit angeben, wie die DPI-Skalierung verarbeitet werden soll:

### <a name="dpi-unaware"></a>DPI nicht bekannt

Dpi-abhängige Anwendungen werden mit einem Fixed-dpi-Wert von 96 (100%). Wenn diese Anwendungen auf einem Bildschirm mit einer Anzeige Skala größer als 96 dpi ausgeführt werden, wird die Anwendungs Bitmap von Windows auf die erwartete physische Größe gestreckt. Dies führt dazu, dass die Anwendung verschwommen erscheint.

### <a name="system-dpi-awareness"></a>System-dpi-Informationen

Desktop Anwendungen, die System-dpi-fähig sind, erhalten in der Regel den dpi-Wert des primären verbundenen Monitors zum Zeitpunkt der Benutzeranmeldung. Während der Initialisierung legen Sie die Benutzeroberfläche entsprechend fest (Größenänderung, auswählen von Schriftgrößen, Laden von Assets usw.), indem Sie diesen System-dpi-Wert verwenden. Auf diese Weise werden System-dpi-fähige Anwendungen nicht auf dpi skaliert (Bitmap gestreckt) von Windows on zeigt das Rendering bei diesem einzelnen dpi an. Wenn die Anwendung in eine Anzeige mit einem anderen Skalierungsfaktor verschoben wird, oder wenn sich der Anzeige Skalierungsfaktor auf andere Weise ändert, wird Windows das Fenster der Anwendung skalieren, sodass Sie unscharf angezeigt werden. Effektiv werden System-dpi-fähige Desktop Anwendungen nur mit einem einzigen Display scale-Faktor nur mit einem einzigen Display Skalierungsfaktor versehen, wenn sich der dpi-Faktor ändert.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor und Per-Monitor (v2) dpi-Informationen

Es wird empfohlen, Desktop Anwendungen so zu aktualisieren, dass Sie den dpi-Modus pro Monitor verwenden, sodass Sie sofort ordnungsgemäß renderfähig werden, wenn sich der dpi-Wert ändert. Wenn in einer Anwendung Windows angezeigt wird, dass Sie in diesem Modus ausgeführt werden soll, wird die Anwendung von Windows nicht mit Bitmap gestreckt, wenn der dpi-Wert geändert wird. stattdessen wird [WM \_ dpichanged](wm-dpichanged.md) an das Anwendungsfenster gesendet. Dann ist die gesamte Aufgabe der Anwendung, die Größe der neuen dpi-Größe selbst zu verarbeiten. Die meisten Benutzeroberflächen-Frameworks, die von Desktop Anwendungen verwendet werden (allgemeine Windows-Steuerelemente (Comctl32), Windows Forms, Windows Presentation Framework usw.) unterstützen keine automatische DPI-Skalierung, sodass Entwickler die Größe der Inhalte ihrer Fenster selbst ändern und neu positionieren müssen.

Es gibt zwei Versionen von Per-Monitor Awareness, dass sich eine Anwendung selbst registrieren kann: Version 1 und Version 2 (PMv2). Das Registrieren eines Prozesses als Ausführung im PMv2-Awareness-Modus führt zu folgenden Ergebnissen:

1.  Die Anwendung, die benachrichtigt wird, wenn sich der dpi-Wert ändert (sowohl die der obersten als auch die untergeordneten HWNDs)
2.  Die Anwendung, die die unformatierten Pixel der einzelnen anzeigen anzeigen
3.  Die Anwendung wird von Windows nie als Bitmap skaliert.
4.  Automatischer nicht-Client Bereich (Fenster Beschriftung, Scrollleisten usw.) DPI-Skalierung nach Windows
5.  Win32-Dialoge (aus " [deatedialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)") werden von Windows automatisch mit dpi skaliert
6.  Design-gezeichnete Bitmap-Objekte in allgemeinen Steuerelementen (Kontrollkästchen, Schaltflächen Hintergründe usw.) werden automatisch am richtigen dpi-Skalierungsfaktor gerendert.

Bei der Ausführung im Per-Monitor v2-Awareness-Modus werden Anwendungen benachrichtigt, wenn sich Ihr dpi-Zeitpunkt geändert hat. Wenn die Größe einer Anwendung für den neuen dpi-Wert nicht geändert wird, wird die Benutzeroberfläche der Anwendung zu klein oder zu groß angezeigt (abhängig von der Differenz der vorherigen und neuen dpi-Werte).

> [!Note]  
> Das PMv1-Bewusstsein (Per-Monitor v1) ist sehr begrenzt. Es wird empfohlen, dass Anwendungen PMv2 verwenden.

In der folgenden Tabelle wird gezeigt, wie Anwendungen in verschiedenen Szenarien dargestellt werden:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>DPI-Awareness-Modus</th>
<th>Eingeführte Windows-Version</th>
<th>Anwendungs Ansicht von dpi</th>
<th>Verhalten bei dpi-Änderungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bewusste</td>
<td>–</td>
<td>Alle anzeigen sind 96 dpi.</td>
<td>Bitmap-Streckung (Blurry)</td>
</tr>
<tr class="even">
<td>System</td>
<td>Vista</td>
<td>Alle anzeigen weisen denselben dpi-Vorgang auf (der dpi-Zeitpunkt der primären Anzeige zum Zeitpunkt des Starts der aktuellen Benutzersitzung).</td>
<td>Bitmap-Streckung (Blurry)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>Der dpi-Wert der Anzeige, in der sich das Anwendungsfenster hauptsächlich befindet</td>
<td><ul>
<li>HWND der obersten Ebene wird bei dpi-Änderungen benachrichtigt</li>
<li>Keine DPI-Skalierung von Benutzeroberflächen Elementen.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor v2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>Der dpi-Wert der Anzeige, in der sich das Anwendungsfenster hauptsächlich befindet</td>
<td><ul>
<li>Auf oberster Ebene <span class="underline">und</span> untergeordnete HWNDs werden bei dpi-Änderungen benachrichtigt</li>
</ul>
<br/> <span class="underline">Automatische DPI-Skalierung von:</span>
<ul>
<li>Nicht-Client Bereich</li>
<li>Design-gezeichnete Bitmaps in allgemeinen Steuerelementen (Comctl32 V6)</li>
<li>Dialogfelder ("<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">kreatedialog</a>")</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>DPI-Informationen pro Monitor (v1)

Per-Monitor v1-dpi-Awareness-Modus (PMv1) wurde mit Windows 8.1 eingeführt. Dieser dpi-Awareness-Modus ist sehr begrenzt und bietet nur die unten aufgeführten Funktionen. Es wird empfohlen, dass Desktop Anwendungen den Per-Monitor v2-Sensibilisierungs Modus verwenden, der unter Windows 10 1703 oder höher unterstützt wird.

Die anfängliche Unterstützung für die Überwachung pro Monitor bot nur Anwendungen wie folgt:

1.  HWNDs der obersten Ebene werden über eine dpi-Änderung benachrichtigt und eine neue vorgeschlagene Größe bereitgestellt.
2.  Windows wird keine bitmapstreckung der Anwendungs Benutzeroberfläche durchführt
3.  Die Anwendung sieht alle anzeigen in physischen Pixeln (siehe Virtualisierung).

Unter Windows 10 1607 oder höher können PMv1-Anwendungen bei WM nccreate auch [enablenonclientdpiscalingaufgerufen](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) werden, \_ um anzufordern, dass Windows den nicht-Client Bereich des Fensters ordnungsgemäß skaliert.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>DPI-Skalierungs Unterstützung pro Monitor durch Benutzeroberflächen Framework/-Technologie

Die folgende Tabelle zeigt die Ebene der Unterstützung für dpi-Informationen pro Monitor, die von verschiedenen Windows-Benutzeroberflächen-Frameworks ab Windows 10 1703 angeboten wird:

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
<th>DPI-Skalierung verarbeitet von</th>
<th>Weitere Informationen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Universelle Windows-Plattform (UWP)</td>
<td>Vollständig</td>
<td>1607</td>
<td>UI-Framework</td>
<td><a href="/windows/uwp/get-started/whats-a-uwp">Universelle Windows-Plattform (UWP)</a></td>
</tr>
<tr class="even">
<td>Unformatierte Win32-/Common-Steuerelemente V6 (comctl32.dll)</td>
<td><ul>
<li>An alle HWNDs gesendete dpi-Änderungs Benachrichtigungs Meldungen</li>
<li>Design-gezeichnete Objekte werden korrekt in allgemeinen Steuerelementen dargestellt.</li>
<li>Automatische DPI-Skalierung für Dialoge</li>
</ul></td>
<td>1703</td>
<td>Application</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub-Beispiel</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Eingeschränkte automatische pro-Monitor-DPI-Skalierung für einige Steuerelemente</td>
<td>1703</td>
<td>UI-Framework</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Hohe dpi-Unterstützung in Windows Forms</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Systemeigene WPF-Anwendungen, die in anderen Frameworks gehostete WPF-Anwendungen und andere in WPF gehostete Frameworks nicht automatisch skalieren</td>
<td>1607</td>
<td>UI-Framework</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub-Beispiel</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>Keine</td>
<td>–</td>
<td>Application</td>
<td>Siehe <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI-Skalierung</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>Keine</td>
<td>–</td>
<td>Application</td>
<td>Siehe <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI-Skalierung</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>Keine</td>
<td>–</td>
<td>Application</td>
<td>–</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Aktualisieren bestehender Anwendungen

Um eine vorhandene Desktop Anwendung zum ordnungsgemäßen verarbeiten der DPI-Skalierung zu aktualisieren, muss Sie so aktualisiert werden, dass zumindest die wichtigen Teile der Benutzeroberfläche aktualisiert werden, um auf dpi-Änderungen zu reagieren.

Die meisten Desktop Anwendungen werden im System-dpi-Modus ausgeführt. Anwendungen mit System-dpi-Unterstützung Skalieren in der Regel auf den dpi-Wert der primären Anzeige (die Anzeige, in der sich die Taskleiste zum Zeitpunkt der Windows-Sitzung befand). Wenn sich der dpi-Wert ändert, wird die Benutzeroberfläche dieser Anwendungen von Windows durch Bitmap gestreckt, was häufig zu einer Unschärfe führt. Beim Aktualisieren einer System-DPI-fähigen Anwendung, die pro Monitor-dpi-Wert unterstützt wird, muss der Code, der das Benutzeroberflächen Layout verarbeitet, so aktualisiert werden, dass es nicht nur während der Anwendungs Initialisierung ausgeführt wird, sondern auch, wenn eine dpi-Änderungs Benachrichtigung ([WM \_ dpichanged](wm-dpichanged.md) im Fall von Win32) empfangen wird. Dies umfasst in der Regel das erneute Aufrufen von Annahmen im Code, dass die Benutzeroberfläche nur einmal skaliert werden muss.

Im Fall von Win32-Programmierung haben viele Win32-APIs auch keinen dpi-oder Anzeige Kontext, sodass Sie nur Werte relativ zum System-dpi-Wert zurückgeben. Es kann nützlich sein, den Code zu durchlaufen, um nach einigen dieser APIs zu suchen und diese durch dpi-abhängige Varianten zu ersetzen. Einige der gängigen APIs mit dpi-abhängigen Varianten sind:



| Single dpi-Version   | Per-Monitor Version        |
|----------------------|----------------------------|
| GetSystemMetrics     | Getsystemmetricsfordpi     |
| "Setting windowrectex"   | "Setting windowrectexfordpi"   |
| SystemParametersInfo | Systemparametersinfofordpi |
| Getdpiformonitor     | Getdpiforwindow            |



 

Es ist auch eine gute Idee, in Ihrer Codebasis nach hart codierten Größen zu suchen, die einen konstanten dpi-Wert annehmen. Diese werden durch Code ersetzt, der die DPI-Skalierung ordnungsgemäß berücksichtigt. Im folgenden finden Sie ein Beispiel, das alle diese Vorschläge umfasst:

### <a name="example"></a>Beispiel:

Das folgende Beispiel zeigt einen vereinfachten Win32-Fall, bei dem ein untergeordnetes HWND erstellt wird. Beim Aufrufen von "upatewindow" wird davon ausgegangen, dass die Anwendung mit 96 dpi ausgeführt wird und weder die Größe der Schaltfläche noch die Position bei höheren DPIs korrekt ist:


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

1.  Der Code Erstellungs Code dpi, der die Position und die Größe des untergeordneten HWND für den dpi-Wert des übergeordneten Fensters skaliert.
2.  Reagieren auf dpi-Änderungen durch Neupositionieren und Ändern der Größe des untergeordneten HWND
3.  Die hart codierten Größen wurden entfernt und durch Code ersetzt, der auf dpi-Änderungen antwortet.


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



Beim Aktualisieren einer System-DPI-fähigen Anwendung sind einige häufige Schritte zu befolgen:

1.  Markieren Sie den Prozess mit dpi-Werten pro Monitor (v2), indem Sie ein Anwendungs Manifest (oder eine andere Methode, abhängig von den verwendeten Benutzeroberflächen-Frameworks) verwenden.
2.  Machen Sie die Benutzeroberflächen-Layoutlogik wiederverwendbar, und verschieben Sie Sie aus dem Anwendungs Initialisierungs Code so, dass Sie wieder verwendet werden kann, wenn eine dpi-Änderung auftritt (WM \_ dpichanged im Fall von Windows-Programmierung (Win32)).
3.  Für ungültig erklärten Code, der annimmt, dass dpi-sensible Daten (dpi/Fonts/sizes usw.) niemals aktualisiert werden müssen. Es ist eine gängige Vorgehensweise, bei der Prozess Initialisierung Schriftgrößen und dpi-Werte zwischenzuspeichern. Wenn Sie eine Anwendung so aktualisieren, dass Sie mit dpi-Werten pro Monitor erreicht wird, müssen dpi-sensible Daten neu ausgewertet werden, wenn ein neuer dpi-Wert erreicht wird.
4.  Wenn eine dpi-Änderung durchgeführt wird, laden Sie alle bitmapassets für den neuen dpi-Vorgang neu bzw. ändern Sie Sie neu, oder verwenden Sie optional Bitmap die aktuell geladenen Assets auf die richtige Größe.
5.  Grep für APIs, die nicht Per-Monitor dpi-fähig sind und Sie durch Per-Monitor dpi-fähigen APIs ersetzen (falls zutreffend). Beispiel: Ersetzen Sie GetSystemMetrics durch getsystemmetricsfordpi.
6.  Testen Sie die Anwendung auf einem Multidisplay-/Multi-dpi-System.
7.  Verwenden Sie für alle Fenster der obersten Ebene in Ihrer Anwendung, die Sie nicht auf die richtige dpi-Skala aktualisieren können, die DPI-Skalierung im gemischten Modus (unten beschrieben), um die Bitmap-Streckung dieser Fenster der obersten Ebene durch das System zuzulassen.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode DPI-Skalierung (DPI-Skalierung unter Prozess)

Beim Aktualisieren einer Anwendung zur Unterstützung der dpi-Konformität pro Monitor kann es manchmal unpraktisch sein, jedes Fenster in der Anwendung in einem einzigen Schritt zu aktualisieren. Dies kann einfach auf die Zeit und den Aufwand zurückzuführen sein, die zum Aktualisieren und Testen der gesamten Benutzeroberfläche erforderlich sind, oder weil Sie nicht den gesamten UI-Code besitzen, den Sie ausführen müssen (wenn die Anwendung möglicherweise die Benutzeroberfläche von Drittanbietern lädt). In diesen Situationen bietet Windows eine Möglichkeit zur Erleichterung der Überwachung pro Monitor, indem es Ihnen ermöglicht, einige ihrer Anwendungsfenster (nur auf oberster Ebene) in Ihrem ursprünglichen dpi-Kompatibilitätsmodus auszuführen, während Sie sich auf Ihre Zeit und ihre Energie konzentrieren, um die wichtigsten Teile Ihrer Benutzeroberfläche zu aktualisieren.

Im folgenden wird veranschaulicht, wie das aussehen könnte: Sie aktualisieren die Benutzeroberfläche der Hauptanwendung ("Hauptfenster" in der Abbildung), sodass Sie mit dem dpi-Bewusstsein pro Monitor ausgeführt werden können, während Sie andere Fenster im vorhandenen Modus ausführen ("sekundäres Fenster").

![Unterschiede bei der DPI-Skalierung zwischen den Informations Modi](images/hub-page-illustrations.png)

Vor dem Windows 10 Anniversary Update (1607) war der dpi-Awareness-Modus eines Prozesses eine Prozess weite Eigenschaft. Ab dem Windows 10 Anniversary Update kann diese Eigenschaft jetzt pro Fenster der **obersten Ebene** festgelegt werden. (**Unter** geordnete Fenster müssen weiterhin der Skalierungs Größe ihres übergeordneten Elements entsprechen.) Ein Fenster der obersten Ebene ist als Fenster ohne übergeordnetes Element definiert. Dies ist in der Regel ein "reguläres" Fenster mit den Schaltflächen Minimieren, maximieren und schließen. Das Szenario, für das das unter Prozess-dpi-Bewusstsein vorgesehen ist, besteht darin, dass die sekundäre Benutzeroberfläche von Windows (Bitmap gestreckt) skaliert wird, während Sie sich auf die Aktualisierung Ihrer primären Benutzeroberfläche konzentrieren.

Um unter Prozess-dpi-Informationen zu aktivieren, rufen Sie [**setthreaddpiawareness Context**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) vor und nach jedem Fenster Erstellungs Aufruf auf. Das Fenster, das erstellt wird, wird mit dem dpi-Bewusstsein verknüpft, das Sie über setthreaddpiawareness Context festgelegt haben. Verwenden Sie den zweiten-Befehl, um die dpi-Informationen des aktuellen Threads wiederherzustellen.

Wenn Sie die unter Prozess-DPI-Skalierung verwenden, können Sie sich auf Windows verlassen, um einige der DPI-Skalierung für Ihre Anwendung durchzuführen. Dadurch können Sie die Komplexität Ihrer Anwendung erhöhen. Es ist wichtig, dass Sie die Nachteile dieses Ansatzes und die Art der komplexen Komplexität verstehen. Weitere Informationen zu unter Prozess-dpi-Informationen finden Sie unter die [DPI-Skalierung im gemischten Modus und die dpi-fähigen APIs.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Testen der Änderungen

Nachdem Sie die Anwendung so aktualisiert haben, dass Sie pro Monitor-dpi-Wert ist, ist es wichtig sicherzustellen, dass Ihre Anwendung ordnungsgemäß auf dpi-Änderungen in einer gemischten dpi-Umgebung antwortet. Zu Test enden Besonderheiten zählen:

1.  Verschieben von Anwendungs Fenstern zwischen Anzeigen verschiedener dpi-Werte
2.  Starten der Anwendung für die Anzeige verschiedener dpi-Werte
3.  Ändern des Skalierungsfaktors für den Monitor, während die Anwendung ausgeführt wird
4.  Ändern Sie die Anzeige, die Sie als primäre Anzeige verwenden, und melden Sie sich _von Windows_ ab, und testen Sie die Anwendung nach dem erneuten Anmelden erneut. Dies ist besonders nützlich für die Suche nach Code, der hart codierte Größen/Dimensionen verwendet.

## <a name="common-pitfalls-win32"></a>Häufige Fehler (Win32)

**Das vorgeschlagene Rechteck, das in WM dpichanged bereitgestellt wird, wird nicht verwendet. \_**

Wenn Windows das Anwendungsfenster an eine [**WM- \_ dpichanged**](wm-dpichanged.md) -Meldung sendet, enthält diese Meldung ein empfohlenes Rechteck, das Sie zum Ändern der Größe des Fensters verwenden sollten. Es ist wichtig, dass Ihre Anwendung dieses Rechteck verwendet, um die Größe selbst zu ändern. Dies geschieht wie folgt:

1.  Stellen Sie sicher, dass sich der Mauszeiger beim Ziehen zwischen den Anzeigen an derselben relativen Position im Fenster verbleibt.
2.  Verhindern, dass das Anwendungsfenster in einen rekursiven dpi-Änderungs-Cycle gelangt, bei dem eine dpi-Änderung eine nachfolgende dpi-Änderung auslöst, die eine andere dpi-Änderung auslöst.

Wenn Sie über anwendungsspezifische Anforderungen verfügen, die die Verwendung des vorgeschlagenen Rechtecks verhindern, das Windows in der WM \_ dpichanged-Meldung bereitstellt, finden Sie weitere Informationen unter [**WM \_ getdpiscaledsize**](wm-getdpiscaledsize.md). Diese Meldung kann verwendet werden, um Windows eine gewünschte Größe zu geben, die Sie verwenden möchten, sobald die dpi-Änderung aufgetreten ist, während die oben beschriebenen Probleme weiterhin vermieden werden.

**Fehlende Dokumentation zur Virtualisierung**

Wenn ein HWND oder ein Prozess entweder als dpi-oder System-dpi-fähig ausgeführt wird, kann es sich um eine von Fenstern gestreckte Bitmap handeln. In diesem Fall skaliert und konvertiert Windows dpi-sensible Informationen von einigen APIs in den Koordinatenraum des aufrufenden Threads. Wenn z. b. ein dpi-abhängiger Thread die Bildschirmgröße beim Ausführen auf einer High-dpi-Anzeige abfragt, wird die Antwort der Anwendung von Windows virtualisiert, als ob der Bildschirm in 96 dpi-Einheiten enthalten wäre. Wenn ein System-dpi-fähiger Thread mit einer Anzeige auf einem anderen dpi-Wert interagiert, als beim Starten der Sitzung des aktuellen Benutzers verwendet wurde, werden von Windows möglicherweise einige API-Aufrufe in den Koordinaten Bereich, den das HWND verwenden würde, beim ursprünglichen dpi-Skalierungsfaktor von Windows in dpi skaliert.

Wenn Sie Ihre Desktop Anwendung auf die DPI-Skalierung aktualisieren, kann es schwierig zu wissen, welche API-Aufrufe virtualisierte Werte basierend auf dem Thread Kontext zurückgeben können. Diese Informationen sind zurzeit von Microsoft nicht ausreichend dokumentiert. Beachten Sie, dass der Rückgabewert möglicherweise virtualisiert wird, wenn Sie eine System-API von einem dpi-abhängigen oder System-DPI-fähigen Thread Kontext abrufen. Stellen Sie daher sicher, dass der Thread im dpi-Kontext ausgeführt wird, den Sie bei der Interaktion mit dem Bildschirm oder den einzelnen Fenstern erwarten. Wenn Sie den dpi-Kontext eines Threads mithilfe von [setthreaddpiawarenesscontext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)vorübergehend ändern, stellen Sie sicher, dass Sie den alten Kontext wiederherstellen, wenn Sie fertig sind, um an anderer Stelle in der Anwendung ein falsches Verhalten zu vermeiden.

**Viele Windows-APIs haben keinen dpi-Kontext.**

Viele ältere Windows-APIs enthalten keinen dpi-oder HWND-Kontext als Teil ihrer Schnittstelle. Infolgedessen müssen Entwickler häufig zusätzliche Aufgaben ausführen, um die Skalierung von dpi-sensiblen Informationen, wie z. b. Größen, Punkten oder Symbolen, zu verarbeiten. Beispielsweise müssen Entwickler, die [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) verwenden, entweder ein Stretch geladenes Symbol oder alternative APIs verwenden, um korrekte Symbole für den entsprechenden dpi-Wert (z. b. [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew)) zu laden.

**Erzwungene zurück setzung der Prozess weiten dpi-Informationen**

Im Allgemeinen kann der dpi-Awareness-Modus des Prozesses nach der Prozess Initialisierung nicht geändert werden. Windows kann jedoch zwangsweise den dpi-Informationsmodus Ihres Prozesses ändern, wenn Sie versuchen, die Anforderung zu unterbrechen, dass alle hwnds in einer Fenster Struktur denselben dpi-Awareness-Modus aufweisen. In allen Versionen von Windows, ab Windows 10 1703, ist es nicht möglich, verschiedene hwnds in einer HWND-Struktur in verschiedenen dpi-Bekanntheits Modi auszuführen. Wenn Sie versuchen, eine Beziehung zwischen untergeordneten und übergeordneten Elementen zu erstellen, die diese Regel unterbricht, kann die dpi-Bekanntheit des gesamten Prozesses zurückgesetzt werden. Dies kann durch folgende Aktionen ausgelöst werden:

1.  Ein CreateWindow-Aufruf, bei dem das übergeordnete Fenster über einen anderen dpi-Awareness-Modus als der aufrufende Thread verfügt.
2.  Ein SetParent-Befehl, bei dem die beiden Fenster mit unterschiedlichen dpi-Informations Modi verknüpft sind.

Die folgende Tabelle zeigt, was geschieht, wenn Sie versuchen, diese Regel zu verletzen:



| Vorgang                 | Windows 8.1                                  | Windows 10 (1607 und früher)                | Windows 10 (1703 und höher)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| Up Window (in-proc)    | –                                          | **Child erbt** (gemischter Modus)              | **Child erbt** (gemischter Modus)              |
| "Kreatewindow" (Kreuz proc) | **Erzwungene zurück** Setzung (der Prozess des Aufrufers)       | **Child erbt** (gemischter Modus)              | **Erzwungene zurück** Setzung (der Prozess des Aufrufers)       |
| SetParent (in-proc)       | –                                          | **Erzwungene zurück** Setzung (aktueller Prozess)        |  Fehler ( \_ ungültiger \_ Zustand)             |
| SetParent (Cross-proc)    | **Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters) | **Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters) | **Erzwungene zurück** Setzung (der Prozess des untergeordneten Fensters) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hohe dpi-API-Referenz](high-dpi-reference.md)
</dt> <dt>

[Dpi-Skalierungs-und dpi-kompatible APIs im gemischten Modus.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

