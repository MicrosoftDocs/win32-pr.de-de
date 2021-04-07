---
title: Eingabe Datentypen Waveform-Audio
description: Eingabe Datentypen Waveform-Audio
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- Wellenform-Audiodaten, Eingabe Datentypen
- Waveform-Audioschnittstelle, Eingabe Datentypen
- Aufzeichnen von Wellenform-Audiodaten, Eingabe Datentypen
- Hwavein-handle
- WaveFormatEx-Struktur
- Wavehdr-Struktur
- Wavin Caps-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038921"
---
# <a name="waveform-audio-input-data-types"></a>Eingabe Datentypen Waveform-Audio

Die folgenden Datentypen werden für die Eingabefunktionen von Waveform-Audiodaten definiert.



| type                                 | BESCHREIBUNG                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hwavein**                          | Handle eines geöffneten Waveform-Audioeingabegeräts.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | -Struktur, die die von einem bestimmten Waveform-Audioeingabegerät unterstützten Datenformate angibt. Diese Struktur wird auch für Waveform-Audioausgabegeräte verwendet. |
| [**Wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Struktur, die als Header für einen Block von Waveform-audioeingabedaten verwendet wird. Diese Struktur wird auch für Waveform-Audioausgabegeräte verwendet.                             |
| [**Wavin Caps**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Struktur, die verwendet wird, um die Funktionen eines bestimmten Waveform-Audioeingabegeräts zu Fragen.                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audiodaten](recording-waveform-audio.md)
</dt> </dl>

 

 