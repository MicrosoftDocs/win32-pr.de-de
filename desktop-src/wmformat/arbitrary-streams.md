---
title: Beliebige Streams
description: Beliebige Streams
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Medienformat-SDK, beliebige Streams
- Advanced Systems Format (ASF), beliebige Streams
- ASF (Advanced Systems Format), beliebige Streams
- Windows Medienformat-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Beliebige Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2cc0587758af8dfa3d4ee05b1a51943a89684629fe2182f5a33fdabbdb68e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434716"
---
# <a name="arbitrary-streams"></a>Beliebige Streams

Zusätzlich zu Audio- und Videostreams und Bildstreams kann eine ASF-Datei Datenströme aufnehmen, die eine Vielzahl von Daten enthalten. Die Objekte des Windows Media Format SDK bieten Unterstützung für Skriptstreams, Dateiübertragungsdatenströme, Webstreams und beliebige Datenströme. Alle diese Streamtypen sind willkürlich, d. h., das Leseobjekt führt keine Datenvalidierung durch. Wenn Sie Streams dieser Typen in Ihre Dateien einschließen, stellen Sie sicher, dass die Leseanwendung eine Überprüfung oder Datenüberprüfung durchführt, um sicherzustellen, dass Ihre Inhalte nicht beschädigt oder absichtlich von einem böswilligen Drittanbieter beschädigt wurden.

Obwohl die Objekte dieses SDK Daten in beliebigen Datenströmen nicht überprüfen oder überprüfen, werden verschiedene Typen beliebiger Datenströme nativ unterstützt. In der folgenden Tabelle sind die vordefinierten beliebigen Streamtypen aufgeführt. Skriptstreams werden ebenfalls unterstützt, aber separat im Abschnitt [Skriptbefehle](script-commands.md) erläutert. Weitere Informationen zum Erstellen benutzerdefinierter Typen finden Sie unter [Custom Arbitrary Data Streams](custom-arbitrary-data-streams.md).



| Beliebiger Typ                   | Beschreibung                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Textstreams](text-streams.md) | Enthält Textzeichenfolgen.                                             |
| [Datei Streams](file-streams.md) | Enthält mindestens eine Datendatei.                                   |
| [Web Streams](web-streams.md)   | Enthalten Datendateien, die der zwischengespeicherten Version von Webseiten entsprechen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Audio- und Video-Streams**](audio-and-video-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




