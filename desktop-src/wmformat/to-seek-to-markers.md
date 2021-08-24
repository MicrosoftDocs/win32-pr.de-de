---
title: So suchen Sie nach Markern
description: So suchen Sie nach Markern
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF), Suche nach Markern
- ASF (Advanced Systems Format), Suche nach Markern
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- asynchrone Reader,Suche nach Markern
- asynchrone Reader,Marker
- Marker,Suchen
- Marker, asynchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807350"
---
# <a name="to-seek-to-markers"></a>So suchen Sie nach Markern

Ein Marker ist ein benannter Speicherort in einer ASF-Datei. Sie können die Wiedergabe nur über die Position eines Markers starten, indem Sie den asynchronen Reader verwenden. Sie können mit der Wiedergabe an einem Marker beginnen, indem Sie die folgenden Schritte ausführen.

1.  Rufen **Sie IWMReader::QueryInterface** auf, um einen Zeiger auf die [**IWMHeaderInfo-Schnittstelle zu**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) erhalten.
2.  Rufen Sie die Gesamtzahl der Marker in der Datei ab, indem Sie [**IWMHeaderInfo::GetMarkerCount aufrufen.**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)
3.  Schleife durch die Marker unter Verwendung der in Schritt 2 abgerufenen Markeranzahl. Rufen Sie den Namen und die Uhrzeit der einzelnen Marker ab, indem [**Sie für jede Markierung IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) aufrufen. Speichern Sie den Index des gewünschten Markers.
4.  Rufen **Sie IWMReader::QueryInterface** auf, um einen Zeiger auf die [**IWMReaderAdvanced2-Schnittstelle zu**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) erhalten.
5.  Geben Sie den Marker an, an dem die Wiedergabe gestartet werden soll, indem [**Sie IWMReaderAdvanced2::StartAtMarker aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) Sie müssen den Index des gewünschten Markers übergeben, den Sie in Schritt 3 gespeichert haben.
6.  Behandeln Sie die Beispiele wie gewohnt in Ihrer Implementierung der [**IWMReaderCallback::OnSample-Methode.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marker**](markers.md)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




