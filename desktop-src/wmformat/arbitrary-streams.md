---
title: Beliebige Streams
description: Beliebige Streams
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows Media-Format-SDK, beliebige Streams
- Advanced Systems Format (ASF), beliebige Streams
- ASF (Advanced Systems Format), beliebige Streams
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- beliebige Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707871"
---
# <a name="arbitrary-streams"></a>Beliebige Streams

Zusätzlich zu den Audio-und Videostreams und bildstreams kann eine ASF-Datei Datenströme aufnehmen, die eine Vielzahl von Daten enthalten. Die Objekte des Windows Media SDK-SDKs unterstützen Skriptstreams, Datei Übertragungsdaten Ströme, Webstreams und beliebige Datenströme. Alle diese Streamtypen sind willkürlich, d. h., es erfolgt keine Datenüberprüfung durch das Lese Objekt. Wenn Sie Streams dieser Typen in Ihre Dateien einschließen, achten Sie darauf, dass die Leseanwendung eine Validierung oder Datenüberprüfung durchführt, um sicherzustellen, dass Ihre Inhalte nicht beschädigt oder absichtlich von einem böswilligen Drittanbieter manipuliert wurden.

Obwohl die Objekte dieses SDK die Daten in beliebigen Streams nicht überprüfen oder validieren, werden verschiedene Typen von beliebigen Datenströmen nativ unterstützt. In der folgenden Tabelle sind die vordefinierten willkürlichen Streamtypen aufgeführt. Skript Datenströme werden ebenfalls unterstützt, werden jedoch separat im Abschnitt [Skript Befehle](script-commands.md) behandelt. Weitere Informationen zum Erstellen von benutzerdefinierten Typen finden Sie unter [benutzerdefinierte beliebige Datenströme](custom-arbitrary-data-streams.md).



| Beliebiger Typ                   | BESCHREIBUNG                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Textstreams](text-streams.md) | Enthalten Text Zeichenfolgen.                                             |
| [Dateistreams](file-streams.md) | Enthalten mindestens eine Datendatei.                                   |
| [Webstreams](web-streams.md)   | Enthalten Datendateien, die der zwischengespeicherten Version von Webseiten entsprechen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Audiodaten und Videostreams**](audio-and-video-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




