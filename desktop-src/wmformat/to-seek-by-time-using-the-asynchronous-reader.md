---
title: So suchen Sie nach Zeit mit dem asynchronen Reader
description: So suchen Sie nach Zeit mit dem asynchronen Reader
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), suchen nach Zeit
- ASF (Advanced Systems Format), suchen nach Zeit
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- asynchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070d480cade395cdbead99b1aedde8928c6fb18b4af15bf6b72c1bcc0dcd6dc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196459"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a>So suchen Sie nach Zeit mit dem asynchronen Reader

Wenn Sie eine bestimmte Präsentationszeit in einer ASF-Datei suchen möchten, muss die Datei ordnungsgemäß konfiguriert sein. Sie können standardmäßig nur Audiodateien suchen, aber Videodateien müssen vor der Suche indiziert werden. Wenn Sie nicht sicher sind, wie eine Datei erstellt wurde, können Sie das \_ g wszWMSeekable-Attribut im Header der Datei überprüfen, indem [**Sie IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)aufrufen.

Rufen Sie [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start)auf, und übergeben Sie die gewünschte Zeit und Dauer des Dateiteils, den Sie als *cnsStart* bzw. *cnsDuration* lesen möchten, um daten in einer ASF-Datei anhand der Präsentationszeit mithilfe des asynchronen Readers zu suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Metadaten bei der Wiedergabe**](reading-metadata-at-playback.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




