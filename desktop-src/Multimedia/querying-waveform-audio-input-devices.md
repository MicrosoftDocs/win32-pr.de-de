---
title: Abfragen von Waveform-Audio Eingabegeräten
description: Abfragen von Waveform-Audio Eingabegeräten
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- Wellenform-Audiodaten, Abfragen von Eingabegeräten
- Waveform-Audioschnittstelle, Abfragen von Eingabegeräten
- Aufzeichnen von Wellenform-Audiodaten, Abfragen von Eingabegeräten
- Abfragen von Waveform-Audioeingabegeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948679"
---
# <a name="querying-waveform-audio-input-devices"></a>Abfragen von Waveform-Audio Eingabegeräten

Vor dem Aufzeichnen von Wellenform-Audiodaten sollten Sie die [**waveingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) -Funktion aufrufen, um die Wellenform-audioeingabefunktionen des Systems zu ermitteln. Diese Funktion füllt eine [**waveincaps**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) -Struktur mit Informationen über die Funktionen eines angegebenen Geräts aus. Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers. Außerdem bietet die **waveincaps** -Strukturinformationen zu den standardmäßigen Waveform-Audioformaten, die das Gerät unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Waveform-Audiodaten](recording-waveform-audio.md)
</dt> </dl>

 

 