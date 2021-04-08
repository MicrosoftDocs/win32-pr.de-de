---
title: Hardware Zeichnungsfunktionen
description: Hardware Zeichnungsfunktionen
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- Videokomprimierungs-Manager (VCM), zeichnen
- VCM (Videokomprimierungs-Manager), zeichnen
- Icgetinfo-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037063"
---
# <a name="hardware-drawing-capabilities"></a>Hardware Zeichnungsfunktionen

Einige Renderer können beim Komprimieren von Video Frames direkt auf Video Hardware zeichnen. Diese Renderer geben das vidcf- \_ Flag zum Zeichnen als Antwort auf die [**icgetinfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) -Funktion zurück. Wenn Sie diesen Renderertyp verwenden, muss die dekomprimierte Daten von der Anwendung nicht verarbeitet werden. Dadurch kann der Renderer die entkomprimierten Daten zum Zeichnen beibehalten.

Wenn Ihre Anwendung einen Renderer mit Zeichnungsfunktionen verwendet, müssen die folgenden Aufgaben ausgeführt werden:

-   Wählen Sie einen Renderer aus.
-   Geben Sie Bildformate an.
-   Initialisieren Sie den Renderer.
-   Zeichnen Sie die Daten.
-   Steuern von Zeichnungs Parametern.

## <a name="renderer-selection"></a>Auswahl für Renderer

Das [**icdrawopen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) -Makro öffnet einen Renderer, der Bilder mit dem angegebenen Format zeichnen kann. Andernfalls wird ein Handle eines Renderers zurückgegeben, wenn der Vorgang erfolgreich ist, andernfalls wird NULL zurückgegeben. Dieses Makro verwendet die [**iclocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) -Funktion, um den Renderer zu öffnen.

## <a name="specifying-image-formats"></a>Angeben von Bildformaten

Da Ihre Anwendung die dekomprimierten Daten nicht zeichnen muss, ist kein bestimmtes Ausgabeformat erforderlich. Es muss jedoch sichergestellt werden, dass der Renderer die Verwendung des Eingabe Formats mithilfe der [**ICM- \_ \_ Abfrage Nachricht zeichnen**](icm-draw-query.md) kann (oder das [**icdrawquery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) -Makro verwenden). Diese Meldung kann nicht bestimmen, ob ein Renderer eine Bitmap zeichnen kann. Wenn die Anwendung bestimmen muss, ob der Renderer die Bitmap zeichnen kann, verwenden Sie diese Meldung mit der [**icdrawbegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) -Funktion.

Die Anwendung kann einen Renderer mit der [**icdrawvorschlags Format**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) -Funktion ein Eingabeformat vorschlagen. Diese Funktion wird verwendet, wenn ein Renderer die Zeichnungsfunktionen von den dekomprimierungsfunktionen trennt. Die meisten Anwendungen, die die Zeichnungsfunktionen verwenden, müssen das Ausgabeformat nicht bestimmen.

## <a name="renderer-initialization"></a>Rendererinitialisierung

Die [**icdrawbegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) -Funktion initialisiert einen Renderer und teilt ihm das Zeichnungs Ziel mit. Mit dieser Funktion können auch die folgenden Aufgaben ausgeführt werden:

-   Bestimmen Sie, ob der Renderer ein bestimmtes Eingabeformat unterstützt.
-   Geben Sie an, ob der Zeichnungs Vorgang ein Fenster oder den gesamten Bildschirm einnimmt.
-   Gibt den Teil des Bilds an, der mithilfe des Quell Rechtecks angezeigt werden soll.
-   Hiermit wird die Wiedergabe Rate der Bildsequenz definiert.

Einige Renderer Puffern die komprimierten Daten, um effizienter zu arbeiten. Die Anwendung kann die [**ICM \_ getbufferswanted**](icm-getbufferswanted.md) -Nachricht senden (oder das [**icgetbufferswanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) -Makro verwenden), um die Anzahl von Puffern zu ermitteln, die der Renderer anfordert. Die Anwendung sollte diese Puffer vorab laden und vor dem Zeichnen an den Renderer senden.

## <a name="drawing-the-data"></a>Zeichnen der Daten

Sie können die [**icdraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) -Funktion verwenden, um die Daten zum Zeichnen zu decoalisieren. Der Renderer beginnt jedoch nicht mit dem Zeichnen von Daten, bis die Anwendung die [**ICM \_ Draw- \_ Start**](icm-draw-start.md) Meldung sendet (oder das [**icdrawstart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) -Makro verwendet). Wenn Ihre Anwendung diese Funktion aufruft, beginnt der Renderer mit dem Zeichnen der Frames mit der durch den dwscale *-Parameter angegebenen* Rate, dividiert durch den *dwscale* -Parameter. Diese Parameter wurden bereitgestellt, wenn die Anwendung den Renderer mithilfe der [**icdrawbegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) -Funktion initialisierte. Das Zeichnen wird fortgesetzt, bis die Anwendung die [**ICM \_ Draw- \_ Endmeldung**](icm-draw-stop.md) sendet (oder das [**icdrawstopemakro**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) verwendet).

> [!Note]  
> Wenn ein Renderer die Daten vor dem Zeichnen puffert, sollte Ihre Anwendung das **icdrawstart** -Makro erst verwenden, wenn die Anzahl der Frames gesendet wurde, die der Renderer für das Makro " **icgetbufferswanted** " zurückgegeben hat.

 

Der *ltime* -Parameter von [**icdraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) gibt die Zeit an, zu der ein Frame gezeichnet werden soll. Der Renderer dividiert diese Ganzzahl durch die mit [**icdrawbegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) angegebene Zeit Skala, um die tatsächliche Zeit zu erhalten. Die Uhrzeiten für **icdraw** -Funktionen sind relativ zu **icdrawstart**. **Icdrawstart** legt die Uhr auf 0 (null) fest. Wenn Ihre Anwendung z. b. 1000 für die Zeitskala und 75 für *ltime* angibt, zeichnet der Renderer den Frame 75 Millisekunden in die Sequenz.

## <a name="controlling-drawing-parameters"></a>Steuern von Zeichnungs Parametern

Sie können die Uhr eines Renderers überwachen, indem Sie die [**ICM \_ Draw \_ GetTime**](icm-draw-gettime.md) -Nachricht senden (oder das [**icdrawgettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) -Makro verwenden), und Sie können die Uhr eines Renderers festlegen, der Daten zeichnen kann, indem Sie die [**ICM \_ Draw \_ setTime**](icm-draw-settime.md) -Nachricht senden (oder das [**icdrawsettime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) -Makro verwenden).

Wenn Sie die aktuelle Position während des Zeichnens eines Renderers ändern möchten, kann die Anwendung die ICM-Meldung zum [**\_ Zeichnen \_**](icm-draw-window.md) des Fensters (oder das [**icdrawwindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) -Makro) zum Neupositionieren des Fensters senden. Anwendungen verwenden diese Meldung in der Regel, wenn sich das Fenster ändert.

Wenn das Wiedergabe Fenster eine Fehlermeldung erhält, muss die Anwendung die [**ICM \_ Draw \_**](icm-draw-realize.md) -Nachricht senden (oder das [**icdraw-**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) Makro verwenden), damit der Renderer die Palette für die Wiedergabe wieder erkennt. Anwendungen können die Palette ändern, indem Sie die ICM-Nachricht zum [**\_ Zeichnen von \_ changepalette**](icm-draw-changepalette.md) senden (oder das [**icdrawchangepalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) -Makro verwenden) und die aktuelle Palette abrufen, indem [**Sie die ICM-zeichnen- \_ \_ \_ palettennachricht**](icm-draw-get-palette.md) senden.

Einige Renderer müssen explizit angewiesen werden, Frames anzuzeigen, die an Sie übergeben werden. Das Senden der [**ICM \_ Draw- \_ renderbuffer**](icm-draw-renderbuffer.md) -Nachricht (oder die Verwendung des [**icdrawrenderbuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) -Makros) bewirkt, dass diese Renderer den Frame zeichnen.

 

 




