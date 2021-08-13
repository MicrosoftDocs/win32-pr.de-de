---
title: So suchen Sie mithilfe des asynchronen Readers nach Framenummer
description: So suchen Sie mithilfe des asynchronen Readers nach Framenummer
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), suchen nach Framezahlen
- ASF (Advanced Systems Format), Suchen nach Framenummern
- Advanced Systems Format (ASF), asynchrone Reader
- ASF (Advanced Systems Format), asynchrone Reader
- asynchrone Reader, suchen nach Framezahlen
- Videostreams, Suchen nach Framenummern
- Videostreams, asynchrone Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e218384b1a27bb3240ac74ad9af6d8298945bb57dfaf635531cb4cbb9aaa9611
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118432613"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>So suchen Sie mithilfe des asynchronen Readers nach Framenummer

Das asynchrone Readerobjekt kann verwendet werden, um die Framezahlen von Videostreams in einer ASF-Datei zu suchen. Um die framebasierte Suche zu verwenden, muss die im Reader geladene Datei nach Frame indiziert werden. Jeder einzelne Videostream kann indiziert werden. Um zu bestimmen, ob ein Stream nach Frame indiziert wurde, können Sie das \_ g wszWMNumberOfFrames-Attribut im Header der Datei überprüfen, indem [**Sie IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)aufrufen.

Führen Sie die folgenden Schritte aus, um Daten in einer ASF-Datei anhand der Framenummer mithilfe des asynchronen Readers zu suchen.

1.  Rufen Sie einen Zeiger auf die [**IWMReaderAdvanced3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) des Readerobjekts ab, indem **Sie IWMReader::QueryInterface** aufrufen.
2.  Legen Sie die Startframenummer und -dauer fest, indem [**Sie IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)aufrufen. Sie müssen die Streamnummer eines frameindizierten Videostreams angeben. Der Reader synchronisiert die restlichen Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt mit der Übermittlung von Ausgabebeispielen.
3.  Verarbeiten Sie die Beispiele wie gewohnt in Ihrer Implementierung der **IWMReaderCallback::OnSample-Methode.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Metadaten bei der Wiedergabe**](reading-metadata-at-playback.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




