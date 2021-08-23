---
title: Waveform-Audio Eingabedatentypen
description: Waveform-Audio Eingabedatentypen
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- Waveformaudio, Eingabedatentypen
- Waveform-Audio-Schnittstelle, Eingabedatentypen
- Aufzeichnen von Waveformaudio, Eingabedatentypen
- HWAVEIN-Handle
- WAVEFORMATEX-Struktur
- WAVEHDR-Struktur
- WAVEINCAPS-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e131e55c404fe658a0c8f60a8f816ff231f9eb9492bcf8641a4e38781bfa78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892090"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio Eingabedatentypen

Die folgenden Datentypen sind für Waveform-Audio-Eingabefunktionen definiert.



| type                                 | BESCHREIBUNG                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Handle eines offenen Waveform-Audio-Eingabegeräts.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Struktur, die die Von einem bestimmten Waveform-Audio-Eingabegerät unterstützten Datenformate angibt. Diese Struktur wird auch für Waveform-Audio-Ausgabegeräte verwendet. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struktur, die als Header für einen Block von Waveform-Audio-Eingabedaten verwendet wird. Diese Struktur wird auch für Waveform-Audio-Ausgabegeräte verwendet.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Struktur, die verwendet wird, um die Funktionen eines bestimmten Waveform-Audio-Eingabegeräts abzufragen.                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audio](recording-waveform-audio.md)
</dt> </dl>

 

 