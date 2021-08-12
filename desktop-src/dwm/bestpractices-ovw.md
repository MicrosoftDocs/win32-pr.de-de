---
title: Überlegungen zur Leistung und bewährte Methoden
description: In diesem Thema werden eine Reihe bewährter Methoden für die Verwendung der DWM-APIs (Desktopfenster-Manager) vorgestellt.
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Desktopfenster-Manager (DWM), bewährte Methoden
- DWM (Desktopfenster-Manager), bewährte Methoden
- Desktopfenster-Manager (DWM), Anwendungsmethoden
- DWM (Desktopfenster-Manager), Anwendungsmethoden
- Desktopfenster-Manager (DWM), Zeichnungsmethoden
- DWM (Desktopfenster-Manager),Zeichnungsmethoden
- Desktopfenster-Manager (DWM),Weichzeichner hinter Effekt
- DWM (Desktopfenster-Manager),Weichzeichner hinter Effekt
- Anwendungsmethoden
- Zeichnungspraktiken
- Weichzeichner hinter Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7affbbf5ebca91a4e5172e75f88da4b9fe8e33f6e1e3de1e7a735add816a313f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280273"
---
# <a name="performance-considerations-and-best-practices"></a>Überlegungen zur Leistung und bewährte Methoden

In diesem Thema werden eine Reihe bewährter Methoden für die Verwendung der DWM-APIs (Desktopfenster-Manager) vorgestellt.

Dieses Thema enthält folgende Abschnitte:

-   [Anwendungsmethoden für DWM](#application-practices-for-dwm)
-   [Zeichnungsmethoden für DWM](#drawing-practices-for-dwm)
-   [DWM Blur-Behind Clientregion](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Anwendungsmethoden für DWM

Wenn Ihre Anwendung die Skalierung von Punkten pro Zoll (DPI) verarbeitet, können Sie eine Anwendung als dpi-fähige Anwendung deklarieren und die automatische Skalierung verhindern, indem Sie das dpi-fähige Flag im Manifest des Programms festlegen oder die [**SetProcessDPIAware-Funktion**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) während der Programminitialisierung aufrufen.

Wenn die DWM-Komposition aktiviert ist, empfangen verdeckte Anwendungen keine [**WM \_ PAINT-Nachrichten**](/windows/desktop/gdi/wm-paint) mehr und werden nicht mehr zum erneuten Rendern aufgefordert. Der Inhalt jedes Fensters ist bereits zum Erstellen des Bildschirmbilds verfügbar.

[**WS EX \_ \_ TRANSPARENT-Fenster**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) der obersten Ebene sollten für Treffertests mit einem **WS \_ EX \_ LAYERED-Stil** kombiniert werden. **WS \_ EX \_ TRANSPARENT** ist im klassischen Sinn ohne Umleitung für untergeordnete Fenster in einer Hierarchie von Fenstern nützlich, die zum selben Thread gehören, aber nicht für Fenster der obersten Ebene vorgesehen sind.

Verwenden Sie Bereiche oder Ebenen, um förmige oder verblendete Fenster zu erstellen. Beachten Sie, dass in Windows Vista und neueren Versionen von Windows das benutzerdefinierte Zeichnen nur einen Teil eines Fensters der obersten Ebene nicht den gewünschten veralteten Inhalt in nicht gezeichneten Regionen bereitstellt.

APIs wie [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) können verwendet werden, um bestimmte tatsächliche Werte zu bestimmen. Wenn Sie über einen Gerätekontext (DC) für ein umgeleitetes Fenster verfügen, stimmt der von **GetDCOrgEx** zurückgegebene Ursprung nicht mit dem Ursprung Ihres Fensters auf dem Bildschirm überein. Der Ursprung ist stattdessen der Ursprung der Backpufferoberfläche für Ihr Fenster: (0, 0).

Wenn alle anderen Fehler auftreten, deaktivieren Sie das Fensterrendering, indem Sie die [**DwmSetWindowAttribute-Funktion**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) aufrufen.

## <a name="drawing-practices-for-dwm"></a>Zeichnungsmethoden für DWM

Vermeiden Sie das direkte Zeichnen auf der primären Anzeigeoberfläche. Dadurch wird der DWM dazu zwingt, die Komposition zu deaktivieren, bis Ihre Anwendung die primäre Geräteoberfläche freigibt.

Bewerten Sie, ob Ihre Anwendung eine eigene doppelte Pufferung bereitstellen muss. Der DWM puffert Inhalt effektiv doppelt und stellt das Fenster in einem einzelnen Frame dar.

Vermeiden Sie das Lesen von oder Schreiben in einen Anzeigedomänencontroller. Obwohl von DWM unterstützt, wird dies aufgrund einer geringeren Leistung nicht empfohlen.

Vermeiden Sie das Zeichnen im Nicht-Clientbereich. Obwohl auf diesen Bereich von der Anwendung zugegriffen werden kann und das Zeichnen dort von der Microsoft Win32-API unterstützt wird, kann dies dazu führen, dass das Fenster jeglichen brillenübergreifenden Rahmen verliert.

Vermeiden Sie das Mischen von Windows Graphics Device Interface (GDI) und Microsoft DirectX, es sei denn, sie überlappen sich nicht. Wenn eine Mischung erforderlich ist, zeichnen Sie entweder den GDI-Inhalt in eine DirectX-Softwareoberfläche und kombinieren sie vor dem Zusammensetzen auf dem Bildschirm, oder zeichnen Sie sie in separaten Fenstern.

Verwenden Sie die [**BitBlt-**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) oder [**StretchBlt-Funktion**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) anstelle von Windows GDI+, um Ihre Zeichnung für das Rendering darzustellen. GDI+ rendert jeweils eine Scanzeile mit Softwarerendering. Dies kann zu Flackern in Ihren Anwendungen führen.

## <a name="dwm-blur-behind-client-region"></a>DWM Blur-Behind Clientregion

Das Rendern des Weichzeichnereffekts ist ein ressourcenintensiver Vorgang für die CPU und die Grafikverarbeitungseinheit (GPU). Anwendungsentwickler werden aufgefordert, die Auswirkungen der Verwendung von Weichzeichnern im Clientbereich zu berücksichtigen, damit sie keine übermäßigen Ressourcen verbrauchen. In den folgenden Fällen sollten Sie besondere Vorsicht walten lassen:

-   Wenn Sie erwarten, dass die Größe des Clientbereichs erheblich ist, auch wenn keine Updates im unscharfen Bereich selbst auftreten. Der Weichzeichner muss gerendert werden, falls Updates unter dem unscharfen Bereich des Fensters auftreten, was CPU- und GPU-Kosten verursacht. Darüber hinaus verursachen Fenstervorgänge im Fenster (Verschieben/Ändern der Größe/Übergänge) mehr Kosten.
-   Wenn Sie erhebliche Updates im unscharf angezeigten Clientbereich erwarten. Dies erfordert bei jedem Update einen erneuten Strich des Weichzeichners und verbraucht übermäßige Ressourcen.
-   Wenn der Weichzeichner voraussichtlich einen erheblichen Bereich abdeckt und auch Aktualisierungen dieses Bereichs erwartet werden, wird dringend empfohlen, den Clientbereich nicht zu verwischen.

 

 