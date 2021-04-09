---
title: Audiodaten und Videostreams
description: Audiodaten und Videostreams
ms.assetid: 809e5bb6-2bc4-4022-9117-a2be5418d7d1
keywords:
- Windows Media-Format-SDK, Audiodatenströme
- Advanced Systems Format (ASF), Audiostreams
- ASF (Advanced Systems Format), Audiostreams
- Windows Media-Format-SDK, Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Audiodatenströme, Informationen
- Videostreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d72eb46a6fb19129da2b9a841eab1710da47013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036893"
---
# <a name="audio-and-video-streams"></a>Audiodaten und Videostreams

Die gängigsten Typen von Streams, die in Dateien verwendet werden, die mit dem Windows Media-Format-SDK erstellt wurden, sind Audio-und Videostreams. Digitale Darstellungen von Audiodaten und Videodaten sind komplex und belegen große Mengen an Arbeitsspeicher. In den meisten Fällen werden sowohl Audiodaten als auch Videos komprimiert, bevor Sie zu einer ASF-Datei hinzugefügt werden. Die Komprimierung wird mithilfe von "Kompressor/Debug (Codec)" durchgeführt.

In diesem SDK sind mehrere Windows Media Codecs enthalten, die eine hervorragende Qualitäts Komprimierung für digitale Medien bereitstellen. Weitere Informationen zu den Windows Media-Codecs finden Sie unter [Codec-Features](codec-features.md). Viele andere Codecs sind aus verschiedenen Quellen verfügbar. Beim Erstellen von ASF-Dateien können Sie die gewünschten Codecs verwenden, aber nur die Windows Media-Codecs werden direkt von den Objekten dieses SDK unterstützt. Um andere Codecs verwenden zu können, müssen Sie die Beispiele komprimieren und Sie als beliebige Daten an das Writer-Objekt übergeben.

Der wichtigste Unterschied zwischen Audio-oder Videostreams und beliebigen Streams besteht darin, dass Datenströme, die Windows Media-Audiodaten oder Videodaten enthalten, von den Objekten des Windows Media Format SDK überprüft werden. Beliebige Datenströme werden nicht automatisch überprüft und sollten von Ihrer Anwendung auf Integrität überprüft werden.

Die Eigenschaften eines Audiostreams oder Videostreams werden im Profil beschrieben, das zum Erstellen der Datei verwendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Beliebige Streams**](arbitrary-streams.md)
</dt> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




