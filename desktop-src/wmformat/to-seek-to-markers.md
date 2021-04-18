---
title: So suchen Sie Marker
description: So suchen Sie Marker
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF), suchen nach Markern
- ASF (Advanced Systems Format), suchen nach Markern
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- asynchrone Leser, suchen nach Markern
- asynchrone Leser, Marker
- Marker, suchen
- Marker, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106338652"
---
# <a name="to-seek-to-markers"></a>So suchen Sie Marker

Ein Marker ist ein benannter Speicherort in einer ASF-Datei. Sie können die Wiedergabe nur über den Speicherort eines Markers starten, indem Sie den asynchronen Reader verwenden. Sie können die Wiedergabe an einem Marker starten, indem Sie die folgenden Schritte ausführen.

1.  Rufen Sie **iwmreader:: QueryInterface** auf, um einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle zu erhalten.
2.  Rufen Sie die Gesamtanzahl der Marker in der Datei ab, indem Sie [**iwmheaderinfo:: getmarkercount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)aufrufen.
3.  Durchlaufen Sie die Marker mithilfe der in Schritt 2 abgerufenen markeranzahl. Rufen Sie den Namen und die Uhrzeit der einzelnen Marker durch Aufrufen von [**iwmheaderinfo:: getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) für jeden Marker ab. Speichern Sie den Index des gewünschten Markers.
4.  Rufen Sie **iwmreader:: QueryInterface** auf, um einen Zeiger auf die [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstelle zu erhalten.
5.  Geben Sie den Marker an, an dem die Wiedergabe durch Aufrufen von [**IWMReaderAdvanced2:: startatmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)gestartet werden soll. Sie müssen den Index des gewünschten Markers übergeben, den Sie in Schritt 3 gespeichert haben.
6.  Behandeln Sie die Beispiele wie in der Implementierung der [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marker**](markers.md)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




