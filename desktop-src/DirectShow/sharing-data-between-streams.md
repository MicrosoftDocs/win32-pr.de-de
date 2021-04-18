---
description: Freigeben von Daten zwischen Streams
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Freigeben von Daten zwischen Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481974"
---
# <a name="sharing-data-between-streams"></a>Freigeben von Daten zwischen Streams

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Die Verarbeitung von Multimedia-Daten erfordert in der Regel sehr viele Systemressourcen. Daher sollten Sie möglichst vermeiden, Daten zu kopieren. Die streamingarchitektur unterstützt freigegebene streambeispiele, einen Mechanismus, der Daten aus einem Stream in einen anderen verschiebt, ohne ihn zu kopieren. Dieser Puffer ermöglicht den effizienten Datentransport zwischen zwei Datenströmen, auch wenn der Zielstream das zugrunde liegende Datenformat nicht explizit unterstützt.

Nehmen Sie beispielsweise an, dass Sie über einen Multimedia-Stream mit drei Datenströmen verfügen: Video und Audiodaten und URL-Daten mit Zeitstempel, um den Videoinhalten zuzuordnen. Sie möchten eine Anwendung schreiben, die für jeden Videoframe einen Copyright Hinweis hinzufügt und die Daten für den Speicher in einen anderen Stream schreibt, aber die Anwendung versteht keine Datenformate außer dem Videostream. Für den Videostream erstellen Sie ein Beispiel, das an die gewünschte DirectDraw-Oberfläche angefügt ist. Sie können dann einen Ausgabestream erstellen, indem Sie entweder die [**idirectdrawmediastream:: createsample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) -Methode mit diesem Zeiger auf dieselbe Oberfläche oder [**imediastream:: createsharedsample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample)aufrufen. In beiden Fällen verwenden die Eingabe-und Ausgabestreams die DirectDraw-Oberfläche. Da Sie das Videoformat verstanden haben, können Sie nach Bedarf auf diese Oberfläche zugreifen.

Zum Abrufen der anderen quellstreamzeiger (Audiodatei und URL) zählen Sie den quellcontainerstream auf und rufen Zeiger auf die nicht-Videostreams auf. Jedem dieser Quelldaten Ströme ist ein Ausgabedatenstrom im Ausgabedatenstrom Container zugeordnet. Rufen Sie diese Ausgabe Zeiger ab, indem Sie die [**imultimediastream:: getmediastream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) -Methode für den Ausgabe Container mit jedem der Quelldaten Strom Zeiger aufrufen. Dieser Vorgang wird in den folgenden Schritten beschrieben.

1.  Rufen Sie [**imultimediastream:: enummediastreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) auf, um einen Zeiger auf einen Quelldaten Strom abzurufen. Stellen Sie sicher, dass es sich nicht um den Videostream handelt, da Ihre Anwendung das Format bereits versteht.
2.  Aufrufen von [**imultimediastream:: getmediastream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) für den Ausgabe Container-Stream mit dem Zeiger aus Schritt 1. Dadurch wird ein Zeiger auf den gewünschten Ausgabestream zurückgegeben.
3.  Für den Quellstream wird "" [**zugeordnet**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) .
4.  Aufrufen von " [**kreatesharedsample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) " für den Ausgabestream.
5.  Ruft [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) für den Quellstream auf, um die Daten zu lesen.
6.  Ruft [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) für den Ausgabestream auf, um die Daten zu schreiben.

Wiederholen Sie diese Schritte für jeden Stream, dessen Format Sie nicht unterstützen. Wenn die Aktualisierung beider Beispiele abgeschlossen ist, enthält der Ausgabestream alle Daten aus dem Quelldaten Strom, und Sie sind fertig.

 

 



