---
title: Abfragen Waveform-Audio Eingabegeräten
description: Abfragen Waveform-Audio Eingabegeräten
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- Waveform-Audio, Abfragen von Eingabegeräten
- Waveform-Audio-Schnittstelle, Abfragen von Eingabegeräten
- Aufzeichnen von Waveform-Audio, Abfragen von Eingabegeräten
- Abfragen von Waveform-Audio-Eingabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371922"
---
# <a name="querying-waveform-audio-input-devices"></a>Abfragen Waveform-Audio Eingabegeräten

Vor dem Aufzeichnen von Waveform-Audio sollten Sie die [**WaveInGetDevCaps-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) aufrufen, um die Waveform-Audio-Eingabefunktionen des Systems zu bestimmen. Diese Funktion füllt eine [**WAVEINCAPS-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) mit Informationen zu den Funktionen eines angegebenen Geräts auf. Diese Informationen umfassen die Hersteller- und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers. Darüber hinaus stellt die **WAVEINCAPS-Struktur** Informationen zu den standardmäßigen Waveform-Audioformaten zur Verfügung, die das Gerät unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audio](recording-waveform-audio.md)
</dt> </dl>

 

 