---
title: Öffnen Waveform-Audio Eingabegeräte
description: Öffnen Waveform-Audio Eingabegeräte
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- Wellenform-Audiodatei, Öffnen von Eingabegeräten
- Waveform-Audioschnittstelle, Öffnen von Eingabegeräten
- Aufzeichnen von Wellenform-Audiodaten, Öffnen von Eingabegeräten
- Öffnen von Waveform-audioeingabegeräten
- Wavin Open-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337647"
---
# <a name="opening-waveform-audio-input-devices"></a>Öffnen Waveform-Audio Eingabegeräte

Verwenden Sie die [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion, um ein Waveform-Audioeingabegerät für die Aufzeichnung zu öffnen. Diese Funktion öffnet das Gerät, das dem angegebenen Geräte Bezeichner zugeordnet ist, und gibt ein Handle des geöffneten Geräts zurück, indem das Handle eines angegebenen Speicher Orts geschrieben wird.

Einige Multimedia-Computer verfügen über mehrere Waveform-Audioeingabegeräte. Wenn Sie nicht wissen, dass Sie ein bestimmtes Waveform-Audioeingabegerät in einem System öffnen möchten, sollten Sie die Wave- \_ Mapper-Konstante für den Geräte Bezeichner verwenden, wenn Sie ein Gerät öffnen. Die [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion wählt das Gerät im System aus, das im angegebenen Datenformat am besten aufgezeichnet werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audiodaten](recording-waveform-audio.md)
</dt> </dl>

 

 