---
description: In diesem Beispiel wird ein Videovorschaudiagramm mithilfe der ICaptureGraphBuilder2::RenderStream-Methode in DirectShow erstellt.
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Videovorschau (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92a6fd3f34a6b2678f41f95a80caca64e47adcc62cbeb6c37f2ed7b71f8d947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748285"
---
# <a name="previewing-video-directshow"></a>Videovorschau (DirectShow)

Um ein Videovorschaudiagramm zu erstellen, rufen Sie die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) wie folgt auf:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



In diesem Beispiel wird Folgendes angenommen:

-   *pBuild* wurde initialisiert, wie unter [Informationen zum Capture Graph Builder](about-the-capture-graph-builder.md)beschrieben.
-   *pCap* wurde initialisiert, indem eine Instanz des Erfassungsfilters erstellt und dem Filterdiagramm hinzugefügt wurde, wie unter [Auswählen eines Erfassungsgeräts](selecting-a-capture-device.md)beschrieben.

Der erste Parameter für die [**ICaptureGraphBuilder2::RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) gibt eine Stecknadelkategorie an. Verwenden Sie für ein Vorschaudiagramm **PIN \_ CATEGORY \_ PREVIEW**. Der zweite Parameter gibt einen Medientyp als Haupttyp-GUID an. Verwenden Sie für Videos **MEDIATYPE \_ Video**. DV-Geräte liefern verschachtelte Audio- und Videodaten, für die der Medientyp **MEDIATYPE \_ Interleaved** lautet. (Weitere Informationen zur DV-Erfassung finden Sie unter [Digitales Video in DirectShow](digital-video-in-directshow.md).)

Der dritte Parameter ist ein Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Erfassungsfilters. Die nächsten beiden Parameter sind in diesem Beispiel nicht erforderlich. Sie werden verwendet, um zusätzliche Filter anzugeben, die möglicherweise zum Rendern des Streams erforderlich sind. Das Festlegen des letzten Parameters auf **NULL** bewirkt, dass der Capture Graph Builder basierend auf dem Medientyp einen Standardrenderer für den Stream auswählt. Für Videos verwendet der Aufzeichnungs-Graph-Generator immer den [Videorendererfilter](video-renderer-filter.md) als Standardrenderer.

> [!Note]  
> In Windows XP und höher ist der Video Mixing Renderer (VMR) zwar der Standardvideorenderer für [**IGraphBuilder-Methoden,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) aber nicht der Standardrenderer für die [**RenderStream-Methode.**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) Auf jeder Plattform verwendet capture Graph Builder immer den alten Videorendererfilter, sofern Sie nichts anderes angeben.

 

Obwohl die Stecknadelkategorie als **PIN \_ CATEGORY \_ PREVIEW** angegeben wird, spielt es keine Rolle, ob der Filter tatsächlich über einen Vorschauanschluss verfügt; es kann einen Videoportanschluss oder nur einen Aufnahmeanschluss haben. In beiden Fällen erstellt der Capture Graph Builder automatisch das richtige Diagramm.

Das folgende Diagramm zeigt das einfachste Diagramm für die Videovorschau.

![Videovorschaudiagramm](images/vidcap01.png)

In diesem Diagramm verfügt der Erfassungsfilter über einen Vorschaupin, der eine direkte Verbindung mit dem Videorenderer herstellt.

Wenn der Erfassungsfilter nur über einen Erfassungspin verfügt, fügt der Capture Graph Builder einen [Smart Tee-Filter](smart-tee-filter.md) ein, der den Datenstrom in einen Erfassungsstream und einen Vorschaustream aufteilt. Dies wird unter [Kombinieren von Videoaufnahme und Vorschau](combining-video-capture-and-preview.md)ausführlicher beschrieben.

In einigen Fällen muss der Videostream den Filter Overlay Mixer durchlaufen. In diesem Falle fügt die [**RenderStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) sie automatisch dem Diagramm hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kombinieren von Videoaufnahme und Vorschau](combining-video-capture-and-preview.md)
</dt> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



