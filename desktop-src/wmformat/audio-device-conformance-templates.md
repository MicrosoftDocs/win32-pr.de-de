---
title: Audiogerätekonformitätsvorlagen
description: Audiogerätekonformitätsvorlagen
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Medienformat-SDK, Gerätekonformitätsvorlagen
- Advanced Systems Format (ASF), Gerätekonformitätsvorlagen
- ASF (Advanced Systems Format), Gerätekonformitätsvorlagen
- Windows Medienformat-SDK, Konformitätsvorlagen für Audiogeräte
- Advanced Systems Format (ASF), Konformitätsvorlagen für Audiogeräte
- ASF (Advanced Systems Format), Audiogerätekonformitätsvorlagen
- Windows Media Audio 9-Codec, Konformitätsvorlagen für Audiogeräte
- Codecs,Windows Media Audio 9-Codec
- Gerätekonformitätsvorlagen, Video
- Audiogerätekonformitätsvorlagen
- Vorlagen, Audiogerätekonformitätsvorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b66c3c414ef2132120cb0824e1e48847310396cf8002d95be13d7f841a0ff6db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840250"
---
# <a name="audio-device-conformance-templates"></a>Audiogerätekonformitätsvorlagen

In der folgenden Tabelle sind die Gerätekonformitätsvorlagen und die zugehörigen Parameter für den Windows Media Audio 9-Codec oder höher aufgeführt.



| Vorlagenzeichenfolge | Bitratenbereich     | Hinweise                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "L1"            | 64 KBit/s, 160 KBit/s | Diese Vorlage ist für eingeschränkte Audiogeräte vorgesehen.                                                                                                                                                                        |
| "L2"            | <= 160 KBit/s     | Diese Vorlage entspricht Klasse 4 im Windows Media Audio-Portierungskit, das die gesamte Implementierung Windows Media Audio-Decoders unterstützt.                                                                                   |
| "L3"            | <= 384 KBit/s     | Diese Vorlage entspricht Klasse 4 im Windows Media Audio-Portierungskit, das die gesamte Implementierung Windows Media Audio-Decoders unterstützt. Der Bitratenbereich ist der einzige Unterschied zwischen dieser Vorlage und L2.<br/> |
| "L"             | Alle Bitraten      | Diese Vorlage ist nur für die Verwendung mit PCs vorgesehen und wird in der Regel verwendet, um die vollständigen Funktionen des Codecs zu präsentieren.                                                                                                           |



 

In der folgenden Tabelle sind die Gerätekonformitätsvorlagen und die zugehörigen Parameter für den Windows Media Audio 9 Voice-Codec aufgeführt.



| Vorlagenzeichenfolge | Bitratenbereich | Hinweise                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| "S1"            | <= 20 KBit/s  | Diese Vorlage ist nur für Geräte mit sehr geringer Komplexität vorgesehen. Bei dieser Vorlage handelt es sich nur um Sprache.<br/>                    |
| "S2"            | <= 20 KBit/s  | Dies ist die empfohlene Vorlage für die meisten Anwendungen. Diese Vorlage unterstützt Kombinationen aus Sprache und Musik.<br/> |



 

In der folgenden Tabelle sind die Gerätekonformitätsvorlagen und zugehörigen Parameter für die Windows Media Audio 9 Professional Codecs oder höher aufgeführt.



| Vorlagenzeichenfolge | Eigenschaften                                                                                   | Hinweise                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "M1"            | Bitrate <= 384 KBit/sSamplingrate <= 48 kHz<br/> Kanäle <= 5,1<br/>   | Diese Vorlage wird für Standardvideos mit Surround-Sound empfohlen.                                                                                                                                                                           |
| "M2"            | Bitrate <= 768 KBit/sSamplingrate <= 96 kHz<br/> Kanäle <= 5,1<br/>   | Diese Vorlage wird für High-Definition-Filme mit Surround-Sound empfohlen.                                                                                                                                                                    |
| "M3"            | Bitrate <= 1.500 KBit/sSamplingrate <= 96 kHz<br/> Kanäle <= 7,1<br/> | Diese Vorlage wird für High-Definition-Filme mit 8-Kanal-Umschließen empfohlen, z. B. Für die Präsentation in Musiksendungen codierte Inhalte.                                                                                                    |
| "M"             | Alle BitratenAlle Samplingraten<br/> Alle Kanäle<br/>                           | Diese Vorlage ist nur für die Verwendung mit PCs vorgesehen und wird in der Regel verwendet, um die vollständigen Funktionen des Codecs zu präsentieren. Dies ist auch die Vorlagenbezeichnung für alle Audiodaten, die mit dem Windows Media Audio 9 Lossless Codec codiert sind.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Parameter der Gerätekonformitätsvorlage**](device-conformance-template-parameters.md)
</dt> <dt>

[**Empfohlene Kombinationen von Gerätekonformitätsvorlagen**](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[**Videogerätekonformitätsvorlagen**](video-device-conformance-templates.md)
</dt> </dl>

 

 





