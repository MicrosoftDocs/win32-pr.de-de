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
# <a name="signal-format"></a><span data-ttu-id="67a85-103">Signal Format</span><span class="sxs-lookup"><span data-stu-id="67a85-103">Signal Format</span></span>

<span data-ttu-id="67a85-104">Das Signal Format eines DV-Camcorders kann NTSC, PAL, Standard oder Long-Play sein.</span><span class="sxs-lookup"><span data-stu-id="67a85-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="67a85-105">**Msdv-Treiber**</span><span class="sxs-lookup"><span data-stu-id="67a85-105">**MSDV Driver**</span></span>

<span data-ttu-id="67a85-106">Um das Eingabe Signal Format vom msdv-Treiber abzurufen, müssen Sie die [**IAMExtTransport:: gettransportbasicparameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) -Methode aufrufen und das ED \_ transbasic- \_ Eingabe Signal-Flag übergeben \_ .</span><span class="sxs-lookup"><span data-stu-id="67a85-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="67a85-107">Die-Methode gibt eine definierte Konstante zurück, die das Format angibt.</span><span class="sxs-lookup"><span data-stu-id="67a85-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="67a85-108">Der folgende Code überprüft das Signal Format und verwendet diesen Wert, um die durchschnittliche Zeit pro Frame zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="67a85-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="67a85-109">Der Variablen Modus empfängt die Signal Format Konstante.</span><span class="sxs-lookup"><span data-stu-id="67a85-109">The variable Mode receives the signal-format constant.</span></span>


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



<span data-ttu-id="67a85-110">Zum Abrufen des Ausgabesignal Formats müssen Sie dieselbe Methode mit dem ED \_ transbasic- \_ ausgabesignflag abrufen \_ .</span><span class="sxs-lookup"><span data-stu-id="67a85-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="67a85-111">**UVC-Treiber**</span><span class="sxs-lookup"><span data-stu-id="67a85-111">**UVC Driver**</span></span>

<span data-ttu-id="67a85-112">Um das Eingabe-oder Ausgabesignal Format vom UVC-Treiber abzurufen, nennen Sie [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in der PIN, und untersuchen Sie den Videoformat Block.</span><span class="sxs-lookup"><span data-stu-id="67a85-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="67a85-113">(Bei UVC-Geräten gibt der im vorherigen Beispiel gezeigte Code in der Regel "Ed \_ " zurück. Das transbasic- \_ Signal \_ ist unbekannt, sodass es nicht zuverlässig ist.)</span><span class="sxs-lookup"><span data-stu-id="67a85-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="67a85-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="67a85-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67a85-115">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="67a85-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



