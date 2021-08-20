---
title: So verwenden Sie die manuelle Streamauswahl
description: So verwenden Sie die manuelle Streamauswahl
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF), manuelle Streamauswahl
- ASF (Advanced Systems Format), manuelle Streamauswahl
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), Streamauswahl
- ASF (Advanced Systems Format), Streamauswahl
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- asynchrone Reader,manuelle Streamauswahl
- asynchrone Reader,Streamauswahl
- Streams,manuelle Auswahl
- Gegenseitiger Ausschluss, manuelle Streamauswahl
- Streams,asynchrone Reader
- Gegenseitiger Ausschluss, asynchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d73f7829736bc36f2362fde0bc86b5c88daf88a6b9e7ef22fb5d6c46ce7ee55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653885"
---
# <a name="to-use-manual-stream-selection"></a>So verwenden Sie die manuelle Streamauswahl

Wenn Sie unkomprimierte Beispiele mit dem Readerobjekt bereitstellen, können Sie sie nur nach Ausgabenummer bereitstellen. Im Fall von sich gegenseitig ausschließenden Streams bedeutet dies, dass Sie Stichproben nur von einem Datenstrom gleichzeitig im gegenseitigen Ausschluss empfangen können. Der Prozess der Auswahl des sich gegenseitig ausschließenden Streams, der zu liefern ist, wird als Streamauswahl bezeichnet.

Für den gegenseitigen Ausschluss von Bitraten trifft der Reader die Streamauswahl automatisch basierend auf den Bedingungen auf dem Hostcomputer bei der Wiedergabe. Bei anderen Arten des gegenseitigen Ausschlusses liefert der Reader Beispiele aus dem Standardstream, es sei denn, Sie wählen manuell selbst einen anderen Stream aus. Es kann auch Fälle geben, in denen Sie einen Stream manuell aus einem gegenseitigen Bitratenausschluss auswählen möchten.

Die manuelle Streamauswahl ist für die gesamte Datei entweder ein- oder ausgeschaltet. Wenn eine Datei gegenseitigen Bitratenausschluss und einen anderen gegenseitigen Ausschlusstyp enthält, müssen Sie die bitratenbasierten Streams manuell auswählen.

Um einen sich gegenseitig ausschließenden Stream manuell auszuwählen, müssen Sie die folgenden Schritte ausführen.

1.  Rufen Sie einen Zeiger auf die [**IWMReaderAdvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) des Readerobjekts ab, indem **Sie IWMReader::QueryInterface aufrufen.**
2.  Aktivieren Sie die manuelle Streamauswahl, indem [**Sie IWMReaderAdvanced::SetManualStreamSelection aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection)
3.  Um herauszufinden, ob ein bestimmter Stream ausgewählt ist, rufen Sie [**IWMReaderAdvanced::GetStreamSelected auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected) Sie müssen einen Zeiger auf eine Variable des [**WMT \_ STREAM \_ SELECTION-Enumerationstyps**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) übergeben. Wenn der Aufruf zurückgegeben wird, beschreibt der Wert in der Variablen den aktuellen Auswahltyp des Streams.
4.  Um einen Stream auszuwählen, rufen [**Sie IWMReaderAdvanced::SetStreamsSelected auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected) Mit dieser Methode können Sie mehrere Datenströme gleichzeitig für den synchronisierten Streamwechsel angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




