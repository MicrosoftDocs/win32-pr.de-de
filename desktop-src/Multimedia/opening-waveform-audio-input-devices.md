---
title: Öffnen Waveform-Audio Eingabegeräte
description: Öffnen Waveform-Audio Eingabegeräte
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- Waveformaudio, Öffnen von Eingabegeräten
- Waveform-Audio-Schnittstelle, Öffnen von Eingabegeräten
- Aufzeichnen von Waveformaudio, Öffnen von Eingabegeräten
- Öffnen von Waveform-Audioeingabegeräten
- waveInOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6391ca5bfe0690d2235504057865fb588f08d0359417ccbcc04b6a7e5eb082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802307"
---
# <a name="opening-waveform-audio-input-devices"></a>Öffnen Waveform-Audio Eingabegeräte

Verwenden Sie die [**WaveInOpen-Funktion,**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) um ein Waveform-Audio-Eingabegerät für die Aufzeichnung zu öffnen. Diese Funktion öffnet das Gerät, das dem angegebenen Gerätebezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicherorts geschrieben wird.

Einige Multimediacomputer verfügen über mehrere Waveform-Audio-Eingabegeräte. Wenn Sie nicht wissen, dass Sie ein bestimmtes Waveform-Audio-Eingabegerät in einem System öffnen möchten, sollten Sie beim Öffnen eines Geräts die WAVE \_ MAPPER-Konstante für die Geräte-ID verwenden. Die [**waveInOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) wählt das Gerät im System aus, das am besten im angegebenen Datenformat erfasst werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audio](recording-waveform-audio.md)
</dt> </dl>

 

 