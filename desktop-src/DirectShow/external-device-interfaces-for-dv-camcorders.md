---
description: Externe Geräteschnittstellen für DV-Camcorder
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Externe Geräteschnittstellen für DV-Camcorder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860548"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="44d65-103">Externe Geräteschnittstellen für DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="44d65-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="44d65-104">Der [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter macht drei Schnittstellen zum Steuern eines Camcorder verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d65-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="44d65-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="44d65-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="44d65-106">Die Basisschnittstelle für das Steuerelement externer Geräte.</span><span class="sxs-lookup"><span data-stu-id="44d65-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="44d65-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="44d65-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="44d65-108">Steuert die VCR-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="44d65-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="44d65-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="44d65-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="44d65-110">Liest Zeitcode vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="44d65-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="44d65-111">Um diese Schnittstellen mit dem msdv-Camcorder-Treiber zu verwenden, schließen Sie die Header Datei xprtdefs. h in Ihr Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="44d65-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="44d65-112">Nachdem Sie ein Erfassungsgerät ausgewählt und eine Instanz des Erfassungs Filters erstellt haben, Fragen Sie den Filter nach diesen Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="44d65-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="44d65-113">Im folgenden Beispiel wird eine benutzerdefinierte-Struktur, die die Schnittstellen Zeiger enthält, zusammen mit booleschen Werten deklariert, die die Verfügbarkeit der einzelnen Schnittstellen angeben:</span><span class="sxs-lookup"><span data-stu-id="44d65-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="44d65-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44d65-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44d65-115">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="44d65-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



