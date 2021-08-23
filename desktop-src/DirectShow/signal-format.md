---
description: Signalformat
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Signalformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66add7467f2f497985094c603aaea83b55967f6b2c07eba4cacde080503ef2e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583180"
---
# <a name="signal-format"></a>Signalformat

Das Signalformat eines DV-Dv-Formats kann NTSC oder PAL, Standard oder LongPlay sein.

**MSDV-Treiber**

Um das Eingabesignalformat vom MSDV-Treiber zu erhalten, rufen Sie die [**IAMExtTransport::GetTransportBasicParameters-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) auf, und übergeben Sie das Flag ED \_ TRANSBASIC \_ INPUT \_ SIGNAL. Die -Methode gibt eine definierte Konstante zurück, die das Format angibt.

Der folgende Code überprüft das Signalformat und berechnet mit diesem Wert die durchschnittliche Zeit pro Frame. Der Variablenmodus empfängt die Konstante signalformat.


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



Um das Ausgabesignalformat zu erhalten, rufen Sie dieselbe Methode mit dem Flag ED \_ TRANSBASIC \_ OUTPUT \_ SIGNAL auf.

**UVC-Treiber**

Um das Eingabe- oder Ausgabesignalformat vom UVC-Treiber zu erhalten, rufen Sie [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) auf dem Pin auf, und untersuchen Sie den Videoformatblock. (Bei UVC-Geräten gibt der im vorherigen Beispiel gezeigte Code in der Regel ED zurück. \_ TRANSBASIC \_ SIGNAL \_ UNKNOWN, daher ist es nicht zuverlässig.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Dvd](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



