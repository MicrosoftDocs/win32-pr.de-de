---
title: Erzielen Sie das beste Video für die Suche nach Leistung
description: Erzielen Sie das beste Video für die Suche nach Leistung
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media-Format-SDK, beste Video Suchleistung
- Advanced Systems Format (ASF), beste Videosuche Leistung
- ASF (Advanced Systems Format), beste Video Suchleistung
- Advanced Systems Format (ASF), Videosuche Leistung
- ASF (Advanced Systems Format), Videosuche Leistung
- Advanced Systems Format (ASF), Leistung
- ASF (Advanced Systems Format), Leistung
- Videosuche
- Leistung, Videosuche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341461"
---
# <a name="getting-the-best-video-seeking-performance"></a>Erzielen Sie das beste Video für die Suche nach Leistung

Das Suchen nach Inhalten in einer Datei ist ein sehr gängiger Vorgang, bei dem es sich um ein potenziell Leistungsproblem handelt. Das mit dem Windows Media Video 9-Codec codierte Video besteht hauptsächlich aus Delta Frames, die nur die Änderungen in Bezug auf den vorherigen Frame aufzeichnen. Das erneute Erstellen von Delta Frames nimmt Zeit in Frage, insbesondere, wenn die Keyframes weit voneinander entfernt sind. Weitere Informationen zum Konfigurieren von Keyframes für die effiziente Suche finden Sie unter [Konfigurieren von Videostreams zum Suchen der Leistung](configuring-video-streams-for-seeking-performance.md).

Zusätzlich zur ordnungsgemäßen Konfiguration können Sie die Suchleistung verbessern, indem Sie die Frame Indizierung für den Videostream verwenden. Es ist in der Regel schneller, eine Frame Nummer zu suchen, als eine Präsentationszeit zu suchen.

Wenn Sie in einer Datei mit mehreren Streams suchen, sollten Sie nur die benötigten Streams auswählen. Jeder für das Lesen konfigurierte Stream wirkt sich auf die Leistung der Suche aus, da alle ausgewählten Streams synchronisiert werden, wenn Sie zu einem Punkt in einer Datei suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**So suchen Sie nach Frame Nummer mithilfe des synchronen Readers**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**So suchen Sie nach Zeit mithilfe des asynchronen Readers**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**So suchen Sie nach Zeit mithilfe des synchronen Readers**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




