---
title: Indizes
description: Indizes
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media-Format-SDK, Indizes
- Advanced Systems Format (ASF), Indizes
- ASF (Advanced Systems Format), Indizes
- Windows Media-Format-SDK, Temporale Indizes
- Advanced Systems Format (ASF), Temporale Indizes
- ASF (Advanced Systems Format), Temporale Indizes
- Windows Media-Format-SDK, Frame basierte Indizes
- Advanced Systems Format (ASF), Frame basierte Indizes
- ASF (Advanced Systems Format), Frame basierte Indizes
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- Indizes, Informationen
- Temporale Indizes
- Frame basierte Indizes
- SMPTE-Zeit Codes, Indizes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856696"
---
# <a name="indexes"></a>Indizes

Eine häufige Anforderung für Anwendungen, die digitale Mediendateien lesen, ist die Möglichkeit, zu einem bestimmten Punkt im Inhalt zu suchen. Die Suche kann schwierig sein, da es keine Garantie dafür gibt, dass die verschiedenen Streams in einer Datei über Beispiele mit gleichzeitigen Startzeiten verfügen. Dieses Problem wird durch die Verwendung von *Indizes* gelöst. Ein Index ist ein Objekt in einer ASF-Datei, das Videobeispiele mit ihren Präsentations Zeiten gleichsetzt. Für Audiostreams ist kein Index erforderlich, da Audiodaten enger mit der Präsentationszeit verbunden sind, als Videodaten.

Das Indexer-Objekt des Windows Media Format SDK kann drei verschiedene Typen von Indizes erstellen: Temporale Indizes, Frame basierte Indizes und SMPTE-Zeit Code Indizes.

Temporale Indizes sind der häufigste Typ. Sie entsprechen einfach Videobeispielen mit den entsprechenden Präsentations Zeiten.

Ein Frame basierter Index entspricht Videobeispielen mit Video Frame Nummern und Präsentations Zeiten. Frame Nummern sind besonders nützlich für Anwendungen, die Video bearbeiten.

Ein SMTPE-Zeit Code Index ist der seltenste Indextyp. Der SMPTE-Zeit Code wird als Grundlage für den Index verwendet und kann nur in Streams verwendet werden, für die in den Beispielen SMPTE-Zeitstempel enthalten sind. Weitere Informationen zum SMPTE-Zeit Code finden Sie [unter Unterstützung von SMPTE-Zeit Code](smpte-time-code-support.md).

Eine ASF-Datei kann einen Index jedes Typs für jeden enthaltenen Videostream enthalten. Standardmäßig wird ein Temporaler Index für jeden Videostream in Dateien eingeschlossen, die vom Writer-Objekt erstellt werden. Sie können die Einstellungen für die automatische Indizierung für Ihre Dateien entsprechend Ihren Anforderungen ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




