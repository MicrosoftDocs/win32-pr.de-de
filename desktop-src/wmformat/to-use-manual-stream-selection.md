---
title: So verwenden Sie die manuelle Datenstrom Auswahl
description: So verwenden Sie die manuelle Datenstrom Auswahl
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF), manuelle Datenstrom Auswahl
- ASF (Advanced Systems Format), manuelle Datenstrom Auswahl
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Streamauswahl
- ASF (Advanced Systems Format), Streamauswahl
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- asynchrone Leser, manuelle Datenstrom Auswahl
- asynchrone Leser, Streamauswahl
- Streams, manuelle Auswahl
- gegenseitiger Ausschluss, manuelle Datenstrom Auswahl
- Streams, asynchrone Leser
- gegenseitiger Ausschluss, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341914"
---
# <a name="to-use-manual-stream-selection"></a>So verwenden Sie die manuelle Datenstrom Auswahl

Wenn Sie nicht komprimierte Beispiele mit dem Reader-Objekt bereitstellt, können Sie diese nur anhand der Ausgabe Nummer übermitteln. Im Fall von sich gegenseitig ausschließenden Streams bedeutet dies, dass Sie nur Beispiele von einem Stream im gegenseitigen Ausschluss gleichzeitig empfangen können. Der Prozess der Auswahl des zu über liegende, sich gegenseitig ausschließenden Streams wird als Streamauswahl bezeichnet.

Bei einem gegenseitigen Bitrate-Ausschluss macht der Reader die Streamauswahl automatisch basierend auf den Bedingungen auf dem Host Computer bei der Wiedergabe. Bei anderen Typen von gegenseitigem Ausschluss liefert der Reader Beispiele aus dem Standardstream, es sei denn, Sie wählen selbst manuell einen anderen Stream aus. Es können auch Instanzen vorhanden sein, wenn Sie einen Stream manuell aus einem Bitrate gegenseitigen Ausschluss auswählen möchten.

Die manuelle Datenstrom Auswahl ist für die gesamte Datei entweder ein-oder ausgeschaltet. Wenn eine Datei einen Bitrate gegenseitigen Ausschluss und einen anderen gegenseitigen Ausschluss Typ enthält, müssen Sie die Bitrate basierten Streams manuell auswählen.

Führen Sie die folgenden Schritte aus, um einen sich gegenseitig ausschließenden Stream manuell auszuwählen.

1.  Abrufen eines Zeigers auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.
2.  Aktivieren Sie die manuelle Datenstrom Auswahl durch Aufrufen von [**iwmreaderadvanced:: setmanualstreamselection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).
3.  Um herauszufinden, ob ein bestimmter Stream ausgewählt ist, nennen Sie [**iwmreaderadvanced:: getstreamselected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected). Sie müssen einen Zeiger an eine Variable des Enumerationstyps der [**WMT-Daten \_ Strom \_ Auswahl**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) übergeben. Wenn der-Rückruf zurückgegeben wird, beschreibt der Wert in der Variablen den aktuellen Auswahltyp des Streams.
4.  Um einen Stream auszuwählen, nennen Sie [**iwmreaderadvanced:: setstreamssgewählt**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected). Diese Methode ermöglicht es Ihnen, mehrere Streams gleichzeitig für den synchronisierten Streamwechsel anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




