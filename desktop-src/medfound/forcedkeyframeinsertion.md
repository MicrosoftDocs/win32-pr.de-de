---
description: Erzwungene Keyframe-Einfügung
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Erzwungene Keyframe-Einfügung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d053f97c7aff08f61fa56d07db0a28b20c797d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484075"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Erzwungene Keyframe-Einfügung (Microsoft Media Foundation)

Wenn Sie ein Video Encoder-Objekt konfigurieren, können Sie ein maximales Intervall für Keyframes im codierten Inhalt festlegen. Der Codec platziert jedoch Keyframes innerhalb dieses Intervalls, wie vom Inhalt vorgegeben. das Keyframe-Intervall ist nicht konstant. Bei manchen Anwendungen ist die Keyframe-Distanz sehr wichtig. Beispielsweise benötigt eine Anwendung zur Videobearbeitung Keyframes an Positionen, die für einen Editor logisch sind, wie bei Szenen Umbrüchen und Schlag Übergängen.

Erzwungene Keyframe-Einfügung ist eine Funktion, mit der Sie anfordern können, dass ein Eingabe Frame als Keyframe codiert wird. Der Encoder versucht, diese Anforderungen zu berücksichtigen, aber die für die Codierungs Sitzung konfigurierten Puffer Einstellungen (Bitrate und Puffer Fenster) haben immer Vorrang.

Die Video Encoder-Objekte implementieren erzwungene Keyframe-Einfügevorgänge als Antwort auf eine an das Eingabe Beispiel angefügte Erweiterung für Dateneinheiten. Weitere Informationen zu Dateneinheiten Erweiterungen finden Sie unter [Verwenden von Dateneinheiten Erweiterungen](usingdataunitextensions.md).

Die Erweiterungs Daten für erzwungene Keyframe-Einfügevorgänge werden durch den folgenden GUID-Wert identifiziert: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Die einzelnen Erweiterungen sind **boolesche** Werte. Legen Sie den Wert auf **true** fest, um eine Keyframe-Anforderung anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Dateneinheiten Erweiterungen](usingdataunitextensions.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



