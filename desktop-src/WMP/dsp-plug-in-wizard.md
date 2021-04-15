---
title: DSP-Plug-in-Assistent
description: DSP-Plug-in-Assistent
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Plug-ins, Plug-in-Assistent
- Plug-Ins für die digitale Signalverarbeitung, Plug-in-Assistent
- DSP-Plug-ins, Plug-in-Assistent
- Plug-in-Assistent
- Visual Studio, DSP-Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515693"
---
# <a name="dsp-plug-in-wizard"></a>DSP-Plug-in-Assistent

Das Windows Media Player SDK bietet einen Plug-in-Assistenten, den Sie Visual Studio hinzufügen können. Der Assistent kann Beispielcode für eine Vielzahl von Plug-ins generieren, einschließlich der folgenden Typen von DSP-Plug-ins:

-   Audiodsp-Plug-in
-   Audiodsp-Plug-in (Dual-Modus)
-   Video DSP-Plug-in
-   Video DSP-Plug-in (Dual-Modus)

Jedes der beiden grundlegenden Beispiel-Plug-ins, audiodsp und Video DSP, fungiert als DirectX Media Object (DMO). Das heißt, dass jedes Plug-in-Beispiel die **imediaobject** -Schnittstelle implementiert. Jede der beiden Sample-Plug-ins im Dual-Modus kann entweder als DMO oder als Media Foundation Transformation (MFT) fungieren. Das heißt, dass die Plug-Ins für das Dual-Mode-Beispiel sowohl die **imediaobject** -Schnittstelle als auch die **IMF Transform** -Schnittstelle implementiert.

Sie können den Beispiel-Plug-in-Code kompilieren, verknüpfen, registrieren und testen. Anschließend können Sie den generierten Beispielcode ändern, um ein eigenes DSP-Plug-in zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aufbau eines DSP-Plug-ins**](building-a-dsp-plug-in.md)
</dt> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Updates des DSP-Plug-in-Assistenten für Windows Media Player 11**](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




