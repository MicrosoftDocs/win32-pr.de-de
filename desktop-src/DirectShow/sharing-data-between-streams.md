---
description: Freigeben von Daten zwischen Streams
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Freigeben von Daten zwischen Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4137d56a9d90f524ee2e5c67b6a4d726d9478e824513d0fe7879c95ce094af1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072564"
---
# <a name="sharing-data-between-streams"></a>Freigeben von Daten zwischen Streams

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispielgrabberfilter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm abzurufen.

 

Für die Verarbeitung von Multimediadaten sind in der Regel viele Systemressourcen erforderlich. Daher sollten Sie nach Möglichkeit das Kopieren von Daten vermeiden. Die Streamingarchitektur unterstützt freigegebene Streambeispiele, einen Mechanismus, der Daten aus einem Stream in einen anderen verschiebt, ohne sie zu kopieren. Dieser Puffer ermöglicht den effizienten Transport von Daten zwischen zwei Datenströmen, auch wenn der Zieldatenstrom das zugrunde liegende Datenformat nicht speziell unterstützt.

Angenommen, Sie verfügen über einen Multimediadatenstrom mit drei Datenströmen: Video und Audio und URL-Daten mit Zeitstempel, um den Videoinhalten zu entsprechen. Sie möchten eine Anwendung schreiben, die einen Urheberrechtshinweis für jeden Videoframe hinzufügt und die Daten zur Speicherung in einen anderen Stream schreibt. Ihre Anwendung versteht jedoch keine Datenformate außer dem Videostream. Für den Videostream erstellen Sie ein Beispiel, das an die gewünschte DirectDraw-Oberfläche angefügt ist. Anschließend können Sie einen Ausgabestream erstellen, indem Sie entweder die [**IDirectDrawMediaStream::CreateSample-Methode**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) mit diesem Zeiger auf dieselbe Oberfläche oder [**IMediaStream::CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample)aufrufen. In beiden Fällen teilen sich die Eingabe- und Ausgabestreams die DirectDraw-Oberfläche. Da Sie das Videoformat verstehen, können Sie nach Bedarf auf diese Oberfläche zugreifen.

Um die anderen Quellstreamzeiger (Audio und URL) abzurufen, müssen Sie den Quellcontainerstream aufzählen und Zeiger auf die Nichtvideostreams abrufen. Jedem dieser Quellstreams ist ein Ausgabestream im Ausgabestreamcontainer zugeordnet. Rufen Sie diese Ausgabezeiger ab, indem Sie die [**IMultiMediaStream::GetMediaStream-Methode**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) für den Ausgabecontainer mit jedem der Quellstreamzeiger aufrufen. Dieser Vorgang wird in den folgenden Schritten beschrieben.

1.  Rufen Sie [**IMultiMediaStream::EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) auf, um einen Zeiger auf einen Quellstream abzurufen. Stellen Sie sicher, dass es sich nicht um den Videostream, da Ihre Anwendung ihr Format bereits versteht.
2.  Rufen Sie [**IMultiMediaStream::GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) im Ausgabecontainerstream mit dem Zeiger aus Schritt 1 auf. Dadurch wird ein Zeiger auf den gewünschten Ausgabestream zurückgegeben.
3.  Rufen [**Sie AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) für den Quellstream auf.
4.  Rufen [**Sie CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) im Ausgabestream auf.
5.  Rufen Sie [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) für den Quellstream auf, um die Daten zu lesen.
6.  Rufen Sie [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) für den Ausgabestream auf, um die Daten zu schreiben.

Wiederholen Sie diese Schritte für jeden Stream, dessen Format Sie nicht unterstützen. Wenn die Aktualisierung beider Beispiele abgeschlossen ist, enthält der Ausgabestream alle Daten aus dem Quellstream, und Sie sind fertig.

 

 



