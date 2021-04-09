---
title: Mixed-Mode DPI-Skalierung und dpi-abhängige APIs
description: .
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9f8a8f72b199aaba195002134855155925b30d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948608"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode DPI-Skalierung und dpi-abhängige APIs

## <a name="sub-process-dpi-awareness-support"></a>Unterstützung für Sub-Process dpi-Erkennung

[**Setthreaddpiawareness Context**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) ermöglicht die Verwendung verschiedener dpi-Skalierungs Modi innerhalb eines einzelnen Prozesses. Vor dem Windows 10 Anniversary Update wurde das dpi-Bewusstsein eines Fensters an den Prozess weiten dpi-Informationsmodus gebunden (dpi-Informationen, System-dpi-fähig oder Per-Monitor dpi-fähig). Mit " **setthreaddpiawareness Context**" können jedoch Fenster der obersten Ebene einen dpi-Modus aufweisen, der sich von dem Prozess weiten dpi-Bild Modus unterscheidet. Dies wirkt sich auch auf untergeordnete Fenster aus, da Sie immer denselben dpi-Sensibilisierungs Modus wie das übergeordnete Fenster aufweisen.

Die Verwendung von **setthreaddpiawarenesscontext** ermöglicht Entwicklern, zu entscheiden, wo Sie Ihre Entwicklungsaktivitäten konzentrieren möchten, wenn Sie ein dpi-spezifisches Verhalten für Desktop Anwendungen definieren. Beispielsweise könnte das primäre Fenster der obersten Ebene einer Anwendung pro Monitor skaliert werden, während sekundäre Fenster der obersten Ebene mithilfe von Bitmapskalierung durch das Betriebssystem skaliert werden könnten.

## <a name="the-dpi-awareness-context"></a>Der Kontext der dpi-Erkennung

Vor der Verfügbarkeit von **setthreaddpiawareness Context** wurde das dpi-Bewusstsein eines Prozesses entweder im Manifest der Anwendungs Binärdatei oder über einen Aufrufen von [**setprocessdpiawareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) während der Prozess Initialisierung definiert. Mit **setthreaddpiawareness Context** kann jeder Thread über einen individuellen dpi-Kontext verfügen, der sich von dem Prozess weiten dpi-Informationsmodus unterscheiden kann. Der Kontext für den dpi-Kontext eines Threads wird mit dem * * * * dpi-Kontexttyp [ \_ \_ * * * *](dpi-awareness-context.md) dargestellt und verhält sich wie folgt:

-   Ein Thread kann den dpi-Awareness-Kontext jederzeit ändern.
-   Alle API-Aufrufe, die nach dem Ändern des Kontexts erfolgen, werden im entsprechenden dpi-Kontext ausgeführt (und können virtualisiert werden).
-   Wenn ein Fenster erstellt wird, wird sein dpi-Bewusstsein als das dpi-Bewusstsein des aufrufenden Threads zu diesem Zeitpunkt definiert.
-   Wenn die Fenster Prozedur für ein Fenster aufgerufen wird, wird der Thread automatisch in den dpi-Kontext gewechselt, der beim Erstellen des Fensters verwendet wurde.

Ein gängiges Szenario für die Verwendung von **setthreaddpiawareness Context** lautet wie folgt: beginnen Sie mit einem Thread, der mit einem Kontext ausgeführt wird (z. b. der **dpi- \_ \_ Kontext \_ pro \_ Monitor \_**-fähig), und wechseln Sie vorübergehend in einen anderen Kontext (der **dpi-Kontext ist \_ \_ \_ nicht bekannt**), erstellen Sie ein Fenster, und wechseln Sie sofort wieder in den vorherigen Zustand Im erstellten Fenster wird der dpi-Kontext des dpi-kontokontexts **\_ \_ \_ nicht** beachtet, während der Kontext für den aufrufenden Thread mit einem nachfolgenden Aufruf von **setthreaddpiawareness Context** in den dpi-Kontext für den dpi-Kontext wieder hergestellt wird. **\_ \_ \_ \_ \_** In diesem Szenario würde das Fenster, das dem aufrufenden Thread zugeordnet ist, mit einem Kontext pro Monitor ausgeführt werden (und somit nicht durch das Betriebssystem durch Bitmap gestreckt), während das neu erstellte Fenster nicht dpi-fähig wäre (und daher automatisch Bitmap auf eine Anzeige festgelegt wird, die auf >100%-Skalierung festgelegt ist).

In Abbildung 1 wird veranschaulicht, wie der Hauptprozess Thread mit **dpi- \_ Awareness- \_ Kontext \_ pro \_ Monitor** ausgeführt wird, seinen Kontext in den Kontext des dpi-Kontexts wechselt und ein neues Fenster erstellt. **\_ \_ \_** Das neu erstellte Fenster wird dann mit einem dpi-kontextkontext des dpi-Kontexts ausgeführt, der **\_ \_ \_ nicht weiß** , wann immer eine Nachricht an ihn gesendet wird, oder es werden API-Aufrufe von diesem Unmittelbar nach dem Erstellen des neuen Fensters wird der Haupt Thread im vorherigen Kontext des dpi-Kontexts **\_ \_ \_ pro \_ Monitor** wieder hergestellt.

![Diagramm, das die dpi-Informationen pro Monitor in Aktion anzeigt](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Neue dpi-bezogene APIs

Zusätzlich zur Unterstützung verschiedener dpi-Informations Modi innerhalb eines einzelnen Prozesses, der von **setthreaddpiawarenstincontext** angeboten wird, wurden die folgenden dpi-spezifischen Funktionen für Desktop Anwendungen hinzugefügt:<dl> <dd>[Enablenonclientdpiscalung * * * *](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> Der dpi-Modus " **pro Monitor v2** " aktiviert diese Funktion automatisch, und das Aufrufen von **enablenonclientdpiscalseeing** ist daher in Anwendungen, die ihn verwenden, nicht erforderlich.

 

Das Aufrufen von **enablenonclientdpiscalseout** innerhalb eines Window s **WM \_ nccreate** -Handlers führt dazu, dass der nicht-Client Bereich eines Fensters der obersten Ebene automatisch für dpi skaliert wird. Wenn das Fenster der obersten Ebene dpi-abhängig ist (unabhängig davon, ob es sich um einen dpi-fähigen Prozess pro Monitor handelt oder weil das Fenster innerhalb eines dpi-fähigen Threads pro Monitor erstellt wurde), werden die Titelleiste, die Bild Lauf leisten, Menüs und Menüleisten dieser Fenster dpi-skaliert, sobald sich der dpi-Wert des Fensters ändert.
</dt> <dt>

Beachten Sie, dass nicht-Client Bereiche eines untergeordneten Fensters, z. b. nicht-Client-Bild Lauf leisten eines untergeordneten Bearbeitungs Steuer Elements, bei Verwendung dieser API nicht automatisch skaliert werden.
</dt> <dt>

> [!Note]  
> **Enablenonclientdpiscaleing** muss vom **WM- \_ nccreate** -Handler aufgerufen werden.

</dt> </dl> </dd> <dd> <b> Die * fordpi-APIs </b>

-   Einige häufig verwendete APIs, z. b. [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , verfügen nicht über einen Kontext eines HWND und haben daher keine Möglichkeit, das richtige dpi-Bewusstsein für Ihre Rückgabewerte zu ableiten. Wenn diese APIs von einem Thread aufgerufen werden, der in einem anderen dpi-Informationsmodus oder-Kontext ausgeführt wird, können Werte zurückgegeben werden, die nicht für den Kontext des aufrufenden Threads skaliert werden. [* * * * Getsystemmetricfordpi * * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)*, [* * * * systemparametersinfofordpi * * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)*, und [* * * *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) "", "", und * * * * "", wird die gleiche Funktionalität wie bei ihren dpi-Entsprechungen verwendet.
-   **Getsystemmetricfordpi** und **systemparametersinfofordpi** geben in Übereinstimmung mit der Gleichung dpi-Werte für System Metriken und Systemparameter Werte zurück:

    |                                                                 |
    |-----------------------------------------------------------------|
    | GetSystemMetrics (...) @ dpi = = getsystemmetricsfordpi (..., dpi) |

    

     

    Aus diesem Grund gibt das Aufrufen von **GetSystemMetrics** (oder **systemparametersinfofordpi**) beim Ausführen auf einem Gerät mit einem bestimmten System-dpi-Wert denselben Wert zurück, den Ihre dpi-abhängigen Varianten (**getsystemmetricsfordpi** und **systemparametersinfofordpi**) erhalten, wenn derselbe dpi-Wert wie die Eingabe verwendet wird.

-   "Setting [**windowrectexfordpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) " nimmt ein HWND an und berechnet die erforderliche Größe eines Fenster Rechtecks auf dpi-Weise.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">Getdpiforwindow</a></b><dl> <dt><b>Getdpiforwindow</b> gibt den dpi-Wert zurück, der dem angegebenen HWND zugeordnet ist. Die Antwort hängt vom dpi-Awareness-Modus des HWND ab:

| DPI-Awareness-Modus des HWND | Rückgabewert                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bewusste                    | 96                                                                                                                                                                                                            |
| System                     | Der System-dpi                                                                                                                                                                                                |
| Per-Monitor                | Der dpi-Wert zeigt an, dass sich das zugeordnete Fenster der obersten Ebene hauptsächlich unter befindet. <br/> (Wenn ein untergeordnetes Fenster bereitgestellt wird, wird der dpi-Wert des entsprechenden übergeordneten Fensters der obersten Ebene zurückgegeben.)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">Getdpiforsystem</a></b><dl> <dt>

Der Aufruf von **getdpiforsystem** ist effizienter als das Aufrufen von [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) und [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) zum Abrufen des System-dpi.
</dt> <dt>

Jede Komponente, die in einer Anwendung ausgeführt werden kann, die unter Prozess-dpi-Informationen verwendet, sollte nicht davon ausgehen, dass der System-dpi-Wert während des Lebenszyklus des Prozesses statisch ist. Wenn z. b. ein Thread, der unter dem dpi-Kontext, der den Kontext erkennt, den System-dpi-Wert abfragt, lautet die Antwort 96. **\_ \_ \_** Wenn derselbe Thread jedoch in den Kontext System-Informations Kontext des **dpi- \_ \_ Kontexts \_** gewechselt und den System-dpi-Wert erneut abgefragt, kann die Antwort anders lauten. Um die Verwendung eines zwischengespeicherten (und möglicherweise veralteten) System dpi-Werts zu vermeiden, verwenden Sie **getdpiforsystem** , um das System-dpi in Relation zum dpi-Awareness-Modus des aufrufenden Threads abzurufen. 
</dt> </dl> </dd> </dl>