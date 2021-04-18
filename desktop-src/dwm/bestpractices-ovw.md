---
title: Überlegungen zur Leistung und bewährte Methoden
description: In diesem Thema werden bewährte Methoden für die Verwendung der Desktopfenster-Manager-APIs (DWM) vorgestellt.
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- Desktopfenster-Manager (DWM), bewährte Methoden
- Dwm (Desktopfenster-Manager), bewährte Methoden
- Desktopfenster-Manager (DWM), Anwendungspraktiken
- Dwm (Desktopfenster-Manager), Anwendungspraktiken
- Desktopfenster-Manager (DWM), Zeichnen von Methoden
- Dwm (Desktopfenster-Manager), Zeichnen von Methoden
- Desktopfenster-Manager (DWM), weich zeichnerhintergrund
- Dwm (Desktopfenster-Manager), weich zeichnerhintergrund
- Anwendungspraktiken
- Zeichnungs Methoden
- weichzeichnerhintergrund
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340930"
---
# <a name="performance-considerations-and-best-practices"></a>Überlegungen zur Leistung und bewährte Methoden

In diesem Thema werden bewährte Methoden für die Verwendung der Desktopfenster-Manager-APIs (DWM) vorgestellt.

Dieses Thema enthält folgende Abschnitte:

-   [Anwendungspraktiken für dwm](#application-practices-for-dwm)
-   [Zeichnungs Methoden für dwm](#drawing-practices-for-dwm)
-   [DWM-Blur-Behind Client Region](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a>Anwendungspraktiken für dwm

Wenn Ihre Anwendung die DPI-Skalierung (dpi) verarbeitet, können Sie eine Anwendung als dpi-fähig deklarieren und die automatische Skalierung verhindern, indem Sie das dpi-abhängige Flag im Programm Manifest festlegen oder die [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) -Funktion während der Programm Initialisierung aufrufen.

Wenn die DWM-Komposition aktiviert ist, empfangen verdeckte Anwendungen keine [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldungen mehr und werden nicht aufgefordert, Sie erneut zu erstellen. Der Inhalt jedes Fensters ist bereits zum Verfassen des Bildschirm Bilds verfügbar.

[**\_ \_ Transparente WS-Ex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Fenster der obersten Ebene sollten bei Treffer Tests mit einem in **WS- \_ Ex \_ geschichteten** Stil kombiniert werden. **WS \_ Die \_ transparente Transparenz** ist im klassischen Sinne und ohne Umleitung nützlich für untergeordnete Fenster in einer Hierarchie von Fenstern, die zum selben Thread gehören, aber nicht für Windows der obersten Ebene vorgesehen sind.

Verwenden Sie Bereiche oder Schichten, um formatierte oder gemischte Fenster zu erstellen. Beachten Sie, dass in Windows Vista und höheren Versionen von Windows der benutzerdefinierte Zeichnungs Bereich eines Fensters der obersten Ebene nicht die gewünschten veralteten Inhalte in undrawn-Regionen bereitstellt.

Mithilfe von APIs, wie z. b. [**getdcorgex**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) , können bestimmte tatsächliche Werte bestimmt werden. Wenn Sie über einen Gerätekontext (DC) für ein umgeleitetes Fenster verfügen, entspricht der von **getdcorgex** zurückgegebene Ursprung nicht dem Ursprung Ihres Fensters auf dem Bildschirm. Der Ursprung ist stattdessen der Ursprung der Hintergrund Puffer Oberfläche für das Fenster: (0,0).

Wenn alle anderen Fehler ausfallen, deaktivieren Sie das Fenster Rendering durch Aufrufen der Funktion [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) .

## <a name="drawing-practices-for-dwm"></a>Zeichnungs Methoden für dwm

Vermeiden Sie es, direkt auf die primäre Anzeige Oberfläche zu zeichnen. Dadurch wird die DWM gezwungen, die Komposition zu deaktivieren, bis die primäre Geräteoberfläche von der Anwendung freigegeben wird.

Evaluieren Sie, ob Ihre Anwendung ihre eigene doppelte Pufferung bereitstellen muss. Der DWM verdoppelt Inhalt und stellt das Fenster in einem einzelnen Frame dar.

Vermeiden Sie Lese-oder Schreibvorgänge auf einem anzeigen Domänen Controller. Obwohl es von DWM unterstützt wird, wird es aufgrund einer verringerten Leistung nicht empfohlen.

Vermeiden Sie das Zeichnen im nicht-Client Bereich. Obwohl die Anwendung auf diesen Bereich zugreifen kann und das Zeichnen von der Microsoft Win32-API unterstützt wird, kann dies dazu führen, dass das Fenster einen beliebigen Glasrahmen verliert.

Vermeiden Sie das Mischen von Windows Graphics Device Interface (GDI) und Microsoft DirectX, es sei denn, Sie überlappen sich nicht Wenn eine Mischung erforderlich ist, zeichnen Sie den GDI-Inhalt in eine DirectX-Software Oberfläche, und kombinieren Sie diese vor der Komposition auf dem Bildschirm, oder zeichnen Sie Sie in separaten Fenstern.

Verwenden Sie die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -oder die [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) -Funktion anstelle von Windows GDI+, um die Zeichnung zum Rendern darzustellen. GDI+ rendert jeweils eine Scan Zeile mit Software Rendering. Dies kann zu einem Flimmern in Ihren Anwendungen führen.

## <a name="dwm-blur-behind-client-region"></a>DWM-Blur-Behind Client Region

Das Rendern des weich Zeichnens-Effekts ist ein ressourcenintensiver Vorgang für die CPU und die Grafikverarbeitungseinheit (GPU). Anwendungsentwickler werden dazu aufgefordert, die Auswirkungen der Verwendung von Client Bereichs Unschärfe zu berücksichtigenden, sodass Sie nicht übermäßig viele Ressourcen verbraucht. In den folgenden Fällen sollten Sie eine besondere Vorsicht walten lassen:

-   Wenn Sie davon ausgehen, dass die Größe des Client Bereichs weich ist, ist dies auch dann der Fall, wenn keine Updates im unscharfen Bereich selbst auftreten. Die Unschärfe muss für den Fall gerendert werden, dass im unscharfen Bereich des Fensters Updates auftreten, was zu CPU-und GPU-Kosten führt. Außerdem verursachen Fenster Vorgänge im Fenster (verschieben/ändern der Größe/Übergänge) Mehrkosten.
-   Wenn Sie im unscharfen Client Bereich beträchtliche Updates erwarten. Dies erfordert eine Umgestaltung der weich Zeichnung bei jedem Update und eine übermäßige Ressourcennutzung.
-   Wenn der Weichzeichner einen erheblichen Bereich abdecken soll und auch Updates für diesen Bereich erwartet werden, wird dringend empfohlen, den Client Bereich nicht zu verwischen.

 

 