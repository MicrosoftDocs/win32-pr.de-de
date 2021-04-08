---
title: So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers
description: So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Advanced Systems Format (ASF), Suche nach Frame Nummern
- ASF (Advanced Systems Format), Suche nach Frame Nummern
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, suchen nach Frame Nummern
- Videostreams, suchen nach Frame Nummern
- Videostreams, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038539"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a>So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers

Das asynchrone Reader-Objekt kann verwendet werden, um die Frame Nummern von Videostreams in einer ASF-Datei zu suchen. Um Frame basiertes suchen zu verwenden, muss die im Reader geladene Datei nach Frame indiziert werden. Jeder einzelne Videostream kann indiziert werden. Um zu ermitteln, ob ein Stream nach Frame indiziert wurde, können Sie das \_ Attribut g wszwmnumofframes im Header der Datei durch Aufrufen von [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)überprüfen.

Führen Sie die folgenden Schritte aus, um mithilfe des asynchronen Readers Daten in einer ASF-Datei nach Frame Nummer zu suchen.

1.  Abrufen eines Zeigers auf die [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.
2.  Legen Sie die Nummer und Dauer des Start Rahmens durch Aufrufen von [**IWMReaderAdvanced3:: startatposition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition)fest. Sie müssen die streamnummer eines Frame indizierten Videostreams angeben. Der Reader synchronisiert den Rest der Ausgaben mit der Präsentationszeit des angegebenen Frames des angegebenen Streams und beginnt damit, Ausgabe Beispiele bereitzustellen.
3.  Behandeln Sie die Beispiele wie in der Implementierung der **iwmreadercallback:: onsample** -Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Metadaten bei der Wiedergabe**](reading-metadata-at-playback.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> </dl>

 

 




