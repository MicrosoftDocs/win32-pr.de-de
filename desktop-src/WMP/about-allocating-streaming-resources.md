---
title: Informationen zum Zuordnen von Streamingressourcen
description: Informationen zum Zuordnen von Streamingressourcen
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Windows Media Player-Plug-Ins,Audio-DSP
- Plug-Ins, Audio-DSP
- Plug-Ins für die digitale Signalverarbeitung, Audiostreamingressourcen
- DSP-Plug-Ins, Audiostreamingressourcen
- Audio-DSP-Plug-Ins,Streamingressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903730"
---
# <a name="about-allocating-streaming-resources"></a>Informationen zum Zuordnen von Streamingressourcen

Das beispielbasierte DSP-Plug-In, das vom Windows Media Player-Plug-In-Assistenten generiert wird, erfordert keine zusätzlichen Streamingpuffer. Möglicherweise möchten Sie jedoch Arbeitsspeicherressourcen für Ihr DSP-Plug-In zuordnen. Beispielsweise erfordert ein Plug-In, das einen Echoeffekt erzeugt, einen sekundären Puffer, um die erforderliche Zeitverzögerung zu erstellen.

Die **IMediaObject-Schnittstelle** enthält zwei Methoden, um diese Situation zu behandeln. Windows Media Player **IMediaObject::AllocateStreamingResources** auf, um Ihnen die Möglichkeit zu geben, alle benötigten Puffer zu erstellen. Windows Media Player später **IMediaObject::FreeStreamingResources** auf, damit Sie jeglichen zuvor zugeordneten Arbeitsspeicher frei geben können. Die Beispielimplementierung des DSP-Plug-Ins ruft auch **FreeStreamingResources** von *CProjectName*::**FinalRelease** auf, um sicherzustellen, dass alle Ressourcen frei werden, bevor das Plug-In-Objekt zerstört wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines Audio-DSP-Plug-Ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




