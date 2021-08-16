---
title: Indizes
description: Indizes
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Medienformat-SDK, Indizes
- Advanced Systems Format (ASF), Indizes
- ASF (Advanced Systems Format), Indizes
- Windows Medienformat-SDK, temporale Indizes
- Advanced Systems Format (ASF), temporale Indizes
- ASF (Advanced Systems Format), temporale Indizes
- Windows Medienformat-SDK, framebasierte Indizes
- Advanced Systems Format (ASF), framebasierte Indizes
- ASF (Advanced Systems Format), framebasierte Indizes
- Windows Medienformat-SDK, SMPTE-Zeitcodes
- Advanced Systems Format (ASF), SMPTE-Zeitcodes
- ASF (Advanced Systems Format), SMPTE-Zeitcodes
- Indizes, Informationen
- Temporale Indizes
- framebasierte Indizes
- SMPTE-Zeitcodes, Indizes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71af891ba2986d3ece1eb2d4cc7eb7ff4086c06eee1f60eabb2210bdc8b6bacd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702484"
---
# <a name="indexes"></a>Indizes

Eine häufige Anforderung für Anwendungen, die digitale Mediendateien lesen, ist die Möglichkeit, zu einem bestimmten Punkt im Inhalt zu suchen. Die Suche kann schwierig sein, da es keine Garantie gibt, dass die verschiedenen Streams in einer Datei Stichproben mit gleichzeitigen Startzeiten aufweisen. Dieses Problem wird durch die Verwendung von *Indizes* behoben. Ein Index ist ein Objekt in einer ASF-Datei, das Videobeispiele mit ihren Präsentationszeiten gleichsetzt. Für Audiostreams ist kein Index erforderlich, da Audiodaten stärker mit der Präsentationszeit verbunden sind als Videodaten.

Das Indexerobjekt des Windows Media Format SDK kann drei verschiedene Arten von Indizes erstellen: temporale Indizes, framebasierte Indizes und SMPTE-Zeitcodeindizes.

Temporale Indizes sind der gängigste Typ. Sie entsprechen einfach Videobeispielen den entsprechenden Präsentationszeiten.

Ein framebasierter Index entspricht Videobeispielen mit Videoframenummern und Präsentationszeiten. Framenummern sind besonders nützlich in Anwendungen, die Videos bearbeiten.

Ein SMTPE-Zeitcodeindex ist der seltenste Indextyp. Er verwendet SMPTE-Zeitcode als Grundlage für den Index und kann nur für Datenströme verwendet werden, in denen SMPTE-Zeitstempel in ihren Stichproben enthalten sind. Weitere Informationen zum SMPTE-Zeitcode finden Sie unter Unterstützung von [SMPTE-Zeitcode.](smpte-time-code-support.md)

Eine ASF-Datei kann einen Index jedes Typs für jeden darin enthaltenen Videostream enthalten. Standardmäßig ist ein temporaler Index für jeden Videostream in Dateien enthalten, die vom Writer-Objekt erstellt werden. Sie können die Einstellungen für die automatische Indizierung für Ihre Dateien ihren Anforderungen entsprechend ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Arbeiten mit Indizes**](working-with-indexes.md)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




