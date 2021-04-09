---
description: Signal Format
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Signal Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860314"
---
# <a name="signal-format"></a>Signal Format

Das Signal Format eines DV-Camcorders kann NTSC, PAL, Standard oder Long-Play sein.

**Msdv-Treiber**

Um das Eingabe Signal Format vom msdv-Treiber abzurufen, müssen Sie die [**IAMExtTransport:: gettransportbasicparameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) -Methode aufrufen und das ED \_ transbasic- \_ Eingabe Signal-Flag übergeben \_ . Die-Methode gibt eine definierte Konstante zurück, die das Format angibt.

Der folgende Code überprüft das Signal Format und verwendet diesen Wert, um die durchschnittliche Zeit pro Frame zu berechnen. Der Variablen Modus empfängt die Signal Format Konstante.


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



Zum Abrufen des Ausgabesignal Formats müssen Sie dieselbe Methode mit dem ED \_ transbasic- \_ ausgabesignflag abrufen \_ .

**UVC-Treiber**

Um das Eingabe-oder Ausgabesignal Format vom UVC-Treiber abzurufen, nennen Sie [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in der PIN, und untersuchen Sie den Videoformat Block. (Bei UVC-Geräten gibt der im vorherigen Beispiel gezeigte Code in der Regel "Ed \_ " zurück. Das transbasic- \_ Signal \_ ist unbekannt, sodass es nicht zuverlässig ist.)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



