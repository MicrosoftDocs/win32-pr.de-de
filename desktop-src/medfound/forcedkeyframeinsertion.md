---
description: Erzwungene Einfügung von Keyframes
ms.assetid: 844e5a01-96db-4a69-9704-f0fdbfee3957
title: Erzwungene Tastenrahmeneinfügung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9790a40c7fc6d2248377003005bbff7ad56b54208e1d20814d5c8150223198ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466140"
---
# <a name="forced-key-frame-insertion-microsoft-media-foundation"></a>Erzwungene Tastenrahmeneinfügung (Microsoft Media Foundation)

Wenn Sie ein Videoencoderobjekt konfigurieren, können Sie ein maximales Intervall für Keyframes im codierten Inhalt festlegen. Der Codec platzieren keyframes jedoch innerhalb dieses Intervalls gemäß dem Inhalt. das Keyframeintervall ist nicht konstant. Bei einigen Anwendungen ist die Entfernung des Keyframes sehr wichtig. Eine Videobearbeitungsanwendung benötigt z. B. Keyframes an Speicherorten, die für einen Editor logisch sind, z. B. bei Szenenunterbrechungen und Aufnahmeübergängen.

Die erzwungene Einfügung von Keyframes ist ein Feature, mit dem Sie anfordern können, dass ein Eingaberahmen als Keyframe codiert wird. Der Encoder versucht, diese Anforderungen zu berücksichtigen, aber die für die Codierungssitzung konfigurierten Puffereinstellungen (Bitrate und Pufferfenster) haben immer Vorrang.

Die Videoencoderobjekte implementieren die erzwungene Einfügung von Keyframes als Antwort auf eine Dateneinheiterweiterung, die an das Eingabebeispiel angefügt ist. Weitere Informationen zu Dateneinheitenerweiterungen finden Sie unter [Verwenden von Dateneinheitenerweiterungen.](usingdataunitextensions.md)

Die Erweiterungsdaten für die erzwungene Einfügung von Keyframes werden durch den folgenden GUID-Wert identifiziert: **F72A3C6F-6EB4-4EBC-B192-09AD9759E828**. Die einzelnen Erweiterungen sind **BOOL-Werte.** Legen Sie den Wert auf **TRUE** fest, um eine Keyframeanforderung anzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Dateneinheitenerweiterungen](usingdataunitextensions.md)
</dt> <dt>

[Arbeiten mit Videos](workingwithvideo.md)
</dt> </dl>

 

 



