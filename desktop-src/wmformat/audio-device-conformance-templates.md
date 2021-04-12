---
title: Konformitäts Vorlagen für Audiogeräte
description: Konformitäts Vorlagen für Audiogeräte
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Advanced Systems Format (ASF), Geräte Konformitäts Vorlagen
- ASF (Advanced Systems Format), Geräte Konformitäts Vorlagen
- Windows Media-Format-SDK, Vorlagen für die Konformität von Audiogeräten
- Advanced Systems Format (ASF), Audiogeräte-Konformitäts Vorlagen
- ASF (Advanced Systems Format), Formatvorlagen für Audiogeräte
- Windows Media Audio 9-Codec, Vorlagen für Audiogeräte Konformität
- Codecs, Windows Media Audio 9-Codec
- Geräte Konformitäts Vorlagen, Video
- Konformitäts Vorlagen für Audiogeräte
- Vorlagen, Konformitäts Vorlagen für Audiogeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309988"
---
# <a name="audio-device-conformance-templates"></a>Konformitäts Vorlagen für Audiogeräte

In der folgenden Tabelle werden die Geräte Konformitäts Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9-Codec oder höher aufgelistet.



| Vorlagen Zeichenfolge | Bereich für Bitrate     | Notizen                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L1            | 64 160 KBit/s | Diese Vorlage ist für eingeschränkte reine Audiogeräte gedacht.                                                                                                                                                                        |
| L2            | <= 160 KBit/s     | Diese Vorlage entspricht der Klasse 4 im Windows Media Audio portieren Kit, das die gesamte Windows Media Audio Decoder-Implementierung unterstützt.                                                                                   |
| L3            | <= 384 Kbit/s     | Diese Vorlage entspricht der Klasse 4 im Windows Media Audio portieren Kit, das die gesamte Windows Media Audio Decoder-Implementierung unterstützt. Der Bitrate Bereich ist der einzige Unterschied zwischen dieser Vorlage und L2.<br/> |
| Int             | Alle Bitraten      | Diese Vorlage ist nur für die Verwendung mit persönlichen Computern vorgesehen und wird normalerweise verwendet, um die vollständigen Funktionen des Codecs vorzustellen.                                                                                                           |



 

In der folgenden Tabelle sind die Geräte Übereinstimmungs Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9-Sprachcodec aufgeführt.



| Vorlagen Zeichenfolge | Bereich für Bitrate | Notizen                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| S1            | <= 20 kbit/s  | Diese Vorlage ist nur für Geräte mit sehr geringer Komplexität vorgesehen. Diese Vorlage ist nur sprachbasiert.<br/>                    |
| S2            | <= 20 kbit/s  | Dies ist die empfohlene Vorlage für die meisten Anwendungen. Diese Vorlage unterstützt Kombinationen von Sprache und Musik.<br/> |



 

In der folgenden Tabelle werden die Geräte Konformitäts Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9 Professional-Codec oder höher aufgelistet.



| Vorlagen Zeichenfolge | Eigenschaften                                                                                   | Notizen                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| M1            | Bitrate <= 384 kbpssampling Rate <= 48 kHz<br/> Kanäle <= 5,1<br/>   | Diese Vorlage wird für Standardfilme mit umschließenden Sound empfohlen.                                                                                                                                                                           |
| Groß            | Bitrate <= 768 kbpssampling Rate <= 96 kHz<br/> Kanäle <= 5,1<br/>   | Diese Vorlage wird für hoch Definitions Filme mit umschließenden Sound empfohlen.                                                                                                                                                                    |
| Kubikmeter            | Bitrate <= 1.500 kbpssampling Rate <= 96 kHz<br/> Kanäle <= 7,1<br/> | Diese Vorlage wird für hoch Definitions Filme mit 8-Kanal-Umschließungs Sound empfohlen, wie z. b. Inhalte, die für die Präsentation in Theatern codiert sind.                                                                                                    |
| "M"             | Alle Bitraten alle Samplings an<br/> Alle Kanäle<br/>                           | Diese Vorlage ist nur für die Verwendung mit persönlichen Computern vorgesehen und wird normalerweise verwendet, um die vollständigen Funktionen des Codecs vorzustellen. Dies ist auch die Vorlagen Bezeichnung für alle Audiodaten, die mit dem Windows Media Audio 9 verlustfreien Codec codiert sind.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Parameter für die Geräte Konformitäts Vorlage**](device-conformance-template-parameters.md)
</dt> <dt>

[**Empfohlene Kombinationen von Geräte Konformitäts Vorlagen**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Vorlagen für die Konformitäts Konformität von Video Geräten**](video-device-conformance-templates.md)
</dt> </dl>

 

 





