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
# <a name="external-device-interfaces-for-dv-camcorders"></a>Externe Geräteschnittstellen für DV-Camcorder

Der [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter macht drei Schnittstellen zum Steuern eines Camcorder verfügbar.



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Die Basisschnittstelle für das Steuerelement externer Geräte. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Steuert die VCR-Funktionen.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Liest Zeitcode vom Gerät.                 |



 

> [!Note]  
> Um diese Schnittstellen mit dem msdv-Camcorder-Treiber zu verwenden, schließen Sie die Header Datei xprtdefs. h in Ihr Projekt ein.

 

Nachdem Sie ein Erfassungsgerät ausgewählt und eine Instanz des Erfassungs Filters erstellt haben, Fragen Sie den Filter nach diesen Schnittstellen ab. Im folgenden Beispiel wird eine benutzerdefinierte-Struktur, die die Schnittstellen Zeiger enthält, zusammen mit booleschen Werten deklariert, die die Verfügbarkeit der einzelnen Schnittstellen angeben:


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



