---
description: Verwenden der Video Anzeige Steuerelemente
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Verwenden der Video Anzeige Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753825"
---
# <a name="using-the-video-display-controls"></a>Verwenden der Video Anzeige Steuerelemente

Die [**IMF videodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle steuert, wie der erweiterte Videorenderer (EVR) ein Video in einem Anwendungsfenster anzeigt. Diese Schnittstelle kann entweder in DirectShow oder Media Foundation verwendet werden. Intern werden die Videoanzeige Steuerelemente vom Standard Presenter von EVR bereitgestellt. Wenn Sie einen benutzerdefinierten Presenter schreiben, können Sie die gleiche Schnittstelle bereitstellen oder eine benutzerdefinierte Schnittstelle definieren.

Die korrekte Methode, einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten, hängt davon ab, ob Sie die DirectShow-Version von EVR oder die Media Foundation Version verwenden. Für den Media Foundation EVR hängt es auch davon ab, ob Sie den EVR direkt verwenden oder über die Medien Sitzung verwenden (was eher typisch ist).

Gehen Sie folgendermaßen vor, um einen Zeiger auf die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle zu erhalten:

1.  Einen Zeiger auf die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle erhalten.

    -   Wenn Sie den DirectShow-EVR-Filter verwenden, können Sie **QueryInterface** für den Filter aufzurufen.

    -   Wenn Sie die EVR-Medien Senke direkt verwenden, können Sie **QueryInterface** in der Medien Senke aufzurufen.

    -   Wenn Sie die Medien Sitzung verwenden, können Sie **QueryInterface** in der Medien Sitzung aufzurufen.

2.  Wenn Sie die Medien Sitzung verwenden, warten Sie, bis die Medien Sitzung das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) mit dem Statuswert MF \_ topostatus Ready sendet \_ . (Überspringen Sie andernfalls diesen Schritt.)

3.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) zum Abrufen der [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle. Der Dienst Bezeichner ist der Video-Rendering-Dienst von Mr \_ \_ \_ .

Sie können die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle verwenden, um die folgenden Aufgaben auszuführen:

-   Legen Sie das clippingfenster fest.

-   Legen Sie die Quell-und Ziel Rechtecke fest.

-   Aktualisieren Sie das Videofenster als Reaktion auf Fenster Meldungen.

-   Aktiviert oder deaktiviert den Vollbildmodus.

## <a name="clipping-window"></a>Clipping-Fenster

Die Anwendung muss ein Fenster bereitstellen, in dem der EVR das Video zeichnet. Um das clippingfenster festzulegen, müssen Sie [**imfvideodisplaycontrol:: setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) mit einem Handle für das Anwendungsfenster aufrufen.

Dieser Schritt ist nicht erforderlich, wenn Sie die EVR-Medien Senke über das Aktivierungs Objekt erstellen. Mithilfe des Fenster Handles, das Sie in der [**MF createvideorendereractivation**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) -Funktion angegeben haben, ruft das Aktivierungs Objekt automatisch [**setvideowindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)auf.

## <a name="source-and-destination-rectangles"></a>Quell-und Ziel Rechtecke

Während der Wiedergabe nimmt der Presenter einen Teil des zusammengesetzten Video Bilds an und zeichnet ihn in einem Bereich des Videofensters. Der Teil des zusammengesetzten Bilds ist das *Quell Rechteck*, und der Bereich des Videofensters ist das *Ziel Rechteck*.

Das Quell Rechteck wird mithilfe normalisierter Koordinaten definiert, wobei der Punkt (0,0, 0,0) der oberen linken Ecke des Videos entspricht und (1,0, 1,0) der unteren rechten Ecke des Videos entspricht. Das Quell Rechteck kann eine beliebige Region innerhalb dieses Rechtecks sein. Das Ziel Rechteck wird in Pixel relativ zum Client Bereich des Fensters angegeben. Das standardmäßige Quell Rechteck ist das gesamte Bild, und das standardmäßige Ziel Rechteck ist ein leeres Rechteck.

Um die Quell-und Ziel Rechtecke festzulegen, müssen Sie [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition)aufrufen.

Dieser Schritt ist nicht erforderlich, wenn Sie die EVR-Medien Senke über das Aktivierungs Objekt erstellen. Das Aktivierungs Objekt legt das Ziel Rechteck automatisch auf den gesamten Client Bereich des Fensters fest. Sie sollten jedoch [**setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) aufrufen, wenn Sie das Quell Rechteck ändern oder ein anderes Ziel Rechteck festlegen möchten.

## <a name="window-messages"></a>Fenster Meldungen

Während der Wiedergabe sollte Ihre Anwendung wie folgt auf bestimmte Fenster Meldungen reagieren:

-   WM \_ Paint: nennen Sie [**imfvideodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) , um das Video neu zu zeichnen. Vermeiden Sie außerdem das Zeichnen über das Ziel Rechteck, während das Video abgespielt wird, da dies zu einem Flimmern führen kann.

-   WM- \_ Größe: Sie müssen möglicherweise [**setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) aufrufen, um die Größe des Ziel Rechtecks zu ändern.

Anders als der Filter für Video Mischungs-Renderer (VMR) in DirectShow müssen Sie den EVR nicht benachrichtigen, wenn Sie eine WM \_ Display Change-Nachricht erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterter Videorenderer](enhanced-video-renderer.md)
</dt> </dl>

 

 



