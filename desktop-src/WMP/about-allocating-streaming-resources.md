---
title: Informationen zum Zuordnen von Streamingressourcen
description: Informationen zum Zuordnen von Streamingressourcen
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Windows Media Player-Plug-ins, audiodsp
- Plug-ins, audiodsp
- Plug-Ins für die digitale Signalverarbeitung, audiostreamingressourcen
- DSP-Plug-ins, audiostreamingressourcen
- audiodsp-Plug-ins, Streamingressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba82f150908e7b96f4e6e56c2161e1b2fdfe145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100762"
---
# <a name="about-allocating-streaming-resources"></a>Informationen zum Zuordnen von Streamingressourcen

Das Beispiel-DSP-Plug-in, das vom Assistenten für Windows-Media Player-Plug-ins generiert wurde, erfordert keine zusätzlichen streamingpuffer. Möglicherweise möchten Sie jedoch Arbeitsspeicher Ressourcen für Ihr DSP-Plug-in zuweisen. Ein Plug-in, das einen Echo Effekt erzeugt, benötigt z. b. einen sekundären Puffer, um die erforderliche Zeitverzögerung zu erzeugen.

Die **imediaobject** -Schnittstelle enthält zwei Methoden zum Behandeln dieser Situation. Der Windows-Media Player ruft **imediaobject:: Zuweisung-Ressourcen** auf, um Ihnen die Möglichkeit zu geben, alle benötigten Puffer zu erstellen. Windows Media Player wird später **imediaobject:: freestreamingresources** aufrufen, damit Sie Speicher freigeben können, den Sie zuvor zugewiesen haben. Die Beispiel Implementierung des DSP-Plug-ins ruft auch **freestreamingresources** aus *cprojectname*::**FinalRelease** auf, um sicherzustellen, dass alle Ressourcen freigegeben werden, bevor das Plug-in-Objekt zerstört wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren eines audiodsp-Plug-ins**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




