---
description: Externe Geräteschnittstellen für DV-Anschlüsse
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Externe Geräteschnittstellen für DV-Anschlüsse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909798"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="cae7d-103">Externe Geräteschnittstellen für DV-Anschlüsse</span><span class="sxs-lookup"><span data-stu-id="cae7d-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="cae7d-104">Der [WDM Video Capture-Filter](wdm-video-capture-filter.md) macht drei Schnittstellen zum Steuern eines -Interfacet verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cae7d-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="cae7d-105">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="cae7d-105">Label</span></span> | <span data-ttu-id="cae7d-106">Wert</span><span class="sxs-lookup"><span data-stu-id="cae7d-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="cae7d-107">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="cae7d-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="cae7d-108">Die Basisschnittstelle für die externe Gerätesteuerung.</span><span class="sxs-lookup"><span data-stu-id="cae7d-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="cae7d-109">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="cae7d-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="cae7d-110">Steuert die VCR-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="cae7d-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="cae7d-111">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="cae7d-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="cae7d-112">Liest den Zeitcode vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="cae7d-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="cae7d-113">Um diese Schnittstellen mit dem MSDV-Treiber zu verwenden, schließen Sie die Headerdatei XPrtDefs.h in Ihr Projekt ein.</span><span class="sxs-lookup"><span data-stu-id="cae7d-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="cae7d-114">Nachdem Sie ein Erfassungsgerät ausgewählt und eine Instanz des Erfassungsfilters erstellt haben, fragen Sie den Filter nach diesen Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="cae7d-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="cae7d-115">Im folgenden Beispiel wird eine benutzerdefinierte -Struktur deklariert, die die Schnittstellenzeiger zusammen mit booleschen Werten enthält, die die Verfügbarkeit der einzelnen Schnittstellen angeben:</span><span class="sxs-lookup"><span data-stu-id="cae7d-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="cae7d-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cae7d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cae7d-117">Steuern eines DV-Dvds</span><span class="sxs-lookup"><span data-stu-id="cae7d-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



