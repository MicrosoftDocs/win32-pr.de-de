---
title: Mixed-Mode DPI-Skalierung und DPI-orientierte APIs
description: Mixed-Mode DPI-Skalierung und DPI-orientierte APIs
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f5b16e4c438cfe1f0d04e61524899e213b25ea
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119725"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode DPI-Skalierung und DPI-orientierte APIs

## <a name="sub-process-dpi-awareness-support"></a>Sub-Process DPI Awareness Support

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) ermöglicht die Verwendung verschiedener DPI-Skalierungsmodi innerhalb eines einzelnen Prozesses. Vor der Windows 10 Anniversary Update war die DPI-Orientierte eines Fensters an den prozessweiten DPI-Bewusstseinsmodus gebunden (DPI nicht bekannt, System-DPI-bewusst oder Per-Monitor DPI-bewusst). Mit **SetThreadDpiAwarenessContext** können Fenster der obersten Ebene jedoch über einen DPI-Bewusstseinsmodus verfügen, der sich von dem des prozessweiten DPI-Bewusstseinsmodus unterscheiden kann. Dies wirkt sich auch auf untergeordnete Fenster aus, da sie immer den gleichen DPI-Bewusstseinsmodus wie das übergeordnete Fenster haben.

Durch die **Verwendung von SetThreadDpiAwarenessContext** können Entwickler entscheiden, wo sie ihre Entwicklungsbemühungen konzentrieren möchten, wenn sie DPI-spezifisches Verhalten für Desktopanwendungen definieren. Beispielsweise könnte das primäre Fenster der obersten Ebene einer Anwendung auf Monitorbasis skaliert werden, während sekundäre Fenster der obersten Ebene über die Bitmapskalierung durch das Betriebssystem skaliert werden könnten.

## <a name="the-dpi-awareness-context"></a>Der DPI-Bewusstseinskontext

Vor der Verfügbarkeit von **SetThreadDpiAwarenessContext** wurde die DPI-Kenntnis eines Prozesses entweder im Manifest der Anwendungsbinardatei oder über einen Aufruf von [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) während der Prozessin initialisierung definiert. Mit **SetThreadDpiAwarenessContext** kann jeder Thread über einen individuellen DPI-Bewusstseinskontext verfügen, der sich von dem des prozessweiten DPI-Bewusstseinsmodus unterscheiden kann. Der DPI-Bewusstseinskontext eines Threads wird mit dem [Typ "/DPI \_ AWARENESS \_ CONTEXT"](dpi-awareness-context.md) dargestellt und verhält sich wie folgt:

-   Der DPI-Kontext eines Threads kann jederzeit geändert werden.
-   Alle API-Aufrufe, die nach dem Ändern des Kontexts ausgeführt werden, werden im entsprechenden DPI-Kontext ausgeführt (und können virtualisiert werden).
-   Wenn ein Fenster erstellt wird, wird sein DPI-Bewusstsein als DPI-Kenntnis des aufrufenden Threads zu diesem Zeitpunkt definiert.
-   Wenn die Fensterprozedur für ein Fenster aufgerufen wird, wird der Thread automatisch in den DPI-Bewusstseinskontext umgeschaltet, der beim Erstellen des Fensters verwendet wurde.

Ein häufiges Szenario für die Verwendung von **SetThreadDpiAwarenessContext** ist folgendes: Beginnen Sie mit einem Thread, der mit einem Kontext ausgeführt wird (z. B. **DPI \_ AWARENESS CONTEXT PER MONITOR \_ \_ \_ \_ AWARE),** wechseln Sie vorübergehend zu einem anderen Kontext **(DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE),** erstellen Sie ein Fenster, und wechseln Sie dann sofort wieder in den vorherigen Zustand des Threadkontexts. Das erstellte Fenster hat den DPI-Kontext **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE,** während der Kontext des aufrufenden Threads mit einem nachfolgenden Aufruf von **SetThreadDpiAwarenessContext** in **DPI AWARENESS CONTEXT PER \_ \_ MONITOR \_ \_ \_ AWARE** wiederhergestellt wird. In diesem Szenario wird das fenster, das dem aufrufenden Thread zugeordnet ist, mit einem Monitorkontext ausgeführt (und daher nicht vom Betriebssystem gestreckt), während das neu erstellte Fenster nicht DPI-bewusst ist (und daher automatisch auf einer Anzeige gestreckt wird, die auf eine Skalierung von >100 % festgelegt ist).

Abbildung 1 zeigt, wie der Hauptprozessthread mit **DPI \_ AWARENESS CONTEXT \_ PER \_ \_ MONITOR** ausgeführt wird, seinen Kontext in **DPI AWARENESS CONTEXT \_ \_ \_ UNAWARE** umschaltet und ein neues Fenster erstellt. Das neu erstellte Fenster wird dann mit dem DPI-Bewusstseinskontext **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE** ausgeführt, wenn eine Nachricht an das Fenster gesendet oder API-Aufrufe von diesem gesendet werden. Unmittelbar nach dem Erstellen des neuen Fensters wird der Hauptthread im vorherigen Kontext **DPI \_ AWARENESS CONTEXT PER MONITOR \_ \_ \_ wiederhergestellt.**

![Diagramm, das die DPI-Wahrnehmung pro Monitor in Aktion zeigt](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Neue DPI-bezogene APIs

Zusätzlich zur Unterstützung für verschiedene DPI-Bewusstseinsmodi innerhalb eines einzelnen Prozesses, den **SetThreadDpiAwarenessContext** bietet, wurden die folgenden DPI-spezifischen Funktionen für Desktopanwendungen hinzugefügt:<dl> <dd>[EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> Der DPI-Bewusstseinsmodus "Pro **Monitor V2"** aktiviert diese Funktionalität automatisch, und das Aufrufen von **EnableNonClientDpiScaling** ist daher in Anwendungen, die sie verwenden, nicht erforderlich.

 

Das **Aufrufen von EnableNonClientDpiScaling** innerhalb des **WM \_ NCCREATE-Handlers** eines Fensters führt dazu, dass der Nicht-Clientbereich eines Fensters der obersten Ebene automatisch für DPI skaliert wird. Wenn das Fenster der obersten Ebene DPI-bewusst pro Monitor ist (unabhängig davon, ob der Prozess selbst DPI-bewusst ist oder weil das Fenster in einem DPI-orientierten Thread pro Monitor erstellt wurde), werden die Beschriftungsleiste, Scrollleisten, Menüs und Menüleisten dieser Fenster immer dann DPI-skaliert, wenn sich der DPI-Wert des Fensters ändert.
</dt> <dt>

Beachten Sie, dass Nicht-Clientbereiche eines untergeordneten Fensters, z. B. Nicht-Client-Bildlaufleisten eines untergeordneten Bearbeitungssteuerfelds, nicht automatisch skaliert werden, wenn diese API verwendet wird.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** muss vom **WM \_ NCCREATE-Handler aufgerufen** werden.

</dt> </dl> </dd> <dd> <b> Die *ForDpi-APIs </b>

-   Mehrere häufig verwendete APIs wie [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) haben keinen Kontext eines HWND und haben daher keine Möglichkeit, das richtige DPI-Bewusstsein für ihre Rückgabewerte zu deduzieren. Das Aufrufen dieser APIs aus einem Thread, der in einem anderen DPI-Bewusstseinsmodus oder Kontext ausgeführt wird, kann Werte zurückgeben, die nicht für den Kontext des aufrufenden Threads skaliert werden. ["GetSystemMetricForDpi",](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi) ["SystemParametersInfoForDpi",](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)und ["AdjustWindowRectExForDpi"](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) führen die gleiche Funktionalität wie ihre nicht DPI-nicht unterstützten Entsprechungen aus. Verwenden Sie jedoch einen DPI-Parameter als Argument, und ziehen Sie das DPI-Bewusstsein aus dem Kontext des aktuellen Threads ab.
-   **GetSystemMetricForDpi** und **SystemParametersInfoForDpi** geben gemäß dieser Gleichung DPI-skalierte Systemmetrikwerte und Systemparameterwerte zurück:

    
    GetSystemMetrics(...) @ dpi == GetSystemMetricsForDpi(..., dpi)

    

     

    Daher gibt der Aufruf von **GetSystemMetrics** (oder **SystemParametersInfoForDpi)** während der Ausführung auf einem Gerät mit einem bestimmten DPI-Wert des Systems denselben Wert zurück, den die DPI-bewussten Varianten (**GetSystemMetricsForDpi** und **SystemParametersInfoForDpi**) bei demselben DPI-Wert wie die Eingabe erhalten.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) verwendet einen HWND und berechnet die erforderliche Größe eines Fensterrechtecks auf DPI-sensitive Weise.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow gibt</b> den DPI zurück, der dem bereitgestellten HWND zugeordnet ist. Die Antwort hängt vom DPI-Bewusstseinsmodus des HWND ab:

| DPI Awareness-Modus von HWND | Rückgabewert                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nicht bekannt                    | 96                                                                                                                                                                                                            |
| System                     | Der System-DPI                                                                                                                                                                                                |
| Per-Monitor                | Der DPI-Wert der Anzeige, auf der sich das zugeordnete Fenster der obersten Ebene hauptsächlich befindet. <br/> (Wenn ein untergeordnetes Fenster bereitgestellt wird, wird der DPI-Wert des entsprechenden übergeordneten Fensters der obersten Ebene zurückgegeben.)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

Das **Aufrufen von GetDpiForSystem** ist effizienter als das Aufrufen von [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) und [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) zum Abrufen des System-DPI.
</dt> <dt>

Jede Komponente, die in einer Anwendung ausgeführt werden kann, die DPI-Informationen zu Unterprozessen verwendet, sollte nicht davon ausgehen, dass der System-DPI während des Lebenszyklus des Prozesses statisch ist. Wenn beispielsweise ein Thread, der unter **DPI \_ AWARENESS CONTEXT \_ \_ UNAWARE** ausgeführt wird, den System-DPI abfragt, lautet die Antwort 96. Wenn derselbe Thread jedoch zum Kontext des **DPI \_ AWARENESS CONTEXT \_ \_ SYSTEM** wechselt und den System-DPI erneut abfragt, kann die Antwort anders sein. Um die Verwendung eines zwischengespeicherten (und möglicherweise veralteten) System-DPI-Werts zu vermeiden, verwenden Sie **GetDpiForSystem,** um den System-DPI relativ zum DPI-Bewusstseinsmodus des aufrufenden Threads abzurufen. 
</dt> </dl> </dd> </dl>
