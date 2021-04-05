---
title: So suchen Sie nach Zeit mithilfe des asynchronen Readers
description: So suchen Sie nach Zeit mithilfe des asynchronen Readers
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), Suche nach Zeit
- ASF (Advanced Systems Format), Suche nach Zeit
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723565"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>So suchen Sie nach Zeit mithilfe des asynchronen Readers

Wenn Sie eine bestimmte Präsentationszeit in einer ASF-Datei suchen möchten, muss die Datei ordnungsgemäß konfiguriert sein. Standardmäßig können Sie in Audiodateien suchen, Videodateien müssen jedoch vor der Suche indiziert werden. Wenn Sie sich nicht sicher sind, wie eine Datei erstellt wurde, können Sie das Attribut "g \_ wszwmseekable" im Header der Datei durch Aufrufen von " [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)" überprüfen.

Um mithilfe des asynchronen Readers mithilfe des asynchronen Readers mithilfe des asynchronen Readers nach Daten in einer ASF-Datei zu suchen, nennen Sie [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), und übergeben Sie die gewünschte Zeit und Dauer des Teils der Datei, die Sie als *cnsstart* bzw. *cnsduration* lesen möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Metadaten bei der Wiedergabe**](reading-metadata-at-playback.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




