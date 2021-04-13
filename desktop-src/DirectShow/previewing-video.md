---
description: Anzeigen einer Vorschau für Videos
ms.assetid: 9b401de1-910a-41f7-bf80-dda73ee4a204
title: Anzeigen einer Vorschau für Videos (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0a8f0d0a422794c4e887693e80391a99bd8d70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568314"
---
# <a name="previewing-video-directshow"></a>Anzeigen einer Vorschau für Videos (DirectShow)

Um ein Video Vorschau Diagramm zu erstellen, nennen Sie die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode wie folgt:


```C++
ICaptureGraphBuilder2 *pBuild; // Capture Graph Builder
// Initialize pBuild (not shown).

IBaseFilter *pCap; // Video capture filter.

/* Initialize pCap and add it to the filter graph (not shown). */

hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
    pCap, NULL, NULL);
```



In diesem Beispiel wird Folgendes vorausgesetzt:

-   *Pbuild* wurde initialisiert, wie unter [Informationen zum Erfassungs Diagramm](about-the-capture-graph-builder.md)-Generator beschrieben.
-   *pcap* wurde initialisiert, indem eine Instanz des Erfassungs Filters erstellt und dem Filter Diagramm hinzugefügt wurde, wie in [Auswählen eines Aufzeichnungs Geräts](selecting-a-capture-device.md)beschrieben.

Der erste Parameter für die [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode gibt eine PIN-Kategorie an. Verwenden Sie für ein Vorschau Diagramm **die \_ Kategorie \_ Vorschau der PIN**. Der zweite Parameter gibt einen Medientyp als GUID des Haupt Typs an. Verwenden Sie für Video das **\_ Video MediaType**. DV-Geräte liefern verschachtelte Audiodaten und Videos, für die der **Medientyp "MediaType \_ überlappende**" ist. (Weitere Informationen zur DV-Erfassung finden Sie unter [digitales Video in DirectShow](digital-video-in-directshow.md).)

Der dritte Parameter ist ein Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Erfassungs Filters. Die folgenden beiden Parameter sind in diesem Beispiel nicht erforderlich. Sie werden verwendet, um zusätzliche Filter anzugeben, die möglicherweise erforderlich sind, um den Stream zu erzeugen. Wenn der letzte Parameter auf **null** festgelegt wird, wählt der Erfassungs Diagramm-Generator basierend auf dem Medientyp einen Standardrenderer für den Stream aus. Für Video verwendet der Erfassungs Diagramm-Generator immer den [Videorendererfilter](video-renderer-filter.md) als Standardrenderer.

> [!Note]  
> In Windows XP und höher ist der Video Mischungs-Renderer (VMR) zwar der Standardvideorenderer für [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Methoden, aber er ist nicht der Standardrenderer für die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode. Auf jeder Plattform verwendet der Erfassungs Diagramm-Generator immer den alten Videorendererfilter, es sei denn, Sie geben andernfalls an.

 

Obwohl die PIN-Kategorie als **\_ \_ Vorschau der PIN-Kategorie** angegeben wird, spielt es keine Rolle, ob der Filter tatsächlich über eine Vorschau-Pin verfügt. es kann eine Videoport-PIN oder nur eine Erfassungs-Pin vorhanden sein. In beiden Fällen erstellt der Erfassungs Diagramm-Generator automatisch das richtige Diagramm.

Das folgende Diagramm zeigt das einfachste mögliche Diagramm für die Vorschau von Videos.

![Video Vorschau Diagramm](images/vidcap01.png)

In diesem Diagramm hat der Erfassungs Filter eine Vorschau-PIN, die eine direkte Verbindung mit dem Videorenderer herstellt.

Wenn der Erfassungs Filter nur über eine Erfassungs-Pin verfügt, fügt der Erfassungs Diagramm-Generator einen [intelligenten Tee](smart-tee-filter.md) -Filter ein, der den Stream in einen Erfassungsdaten Strom und einen Vorschau Datenstrom teilt. Dies wird unter [Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md)ausführlich beschrieben.

In einigen Fällen muss der Videostream den Überlagerungs-Mischungs Filter durchlaufen. Wenn dies der Fall ist, fügt die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode Sie automatisch dem Diagramm hinzu.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md)
</dt> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



