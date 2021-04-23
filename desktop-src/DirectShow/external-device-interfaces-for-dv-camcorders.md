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
# <a name="external-device-interfaces-for-dv-camcorders"></a>Externe Geräteschnittstellen für DV-Anschlüsse

Der [WDM Video Capture-Filter](wdm-video-capture-filter.md) macht drei Schnittstellen zum Steuern eines -Interfacet verfügbar.



| Bezeichnung | Wert |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | Die Basisschnittstelle für die externe Gerätesteuerung. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Steuert die VCR-Funktionen.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Liest den Zeitcode vom Gerät.                 |



 

> [!Note]  
> Um diese Schnittstellen mit dem MSDV-Treiber zu verwenden, schließen Sie die Headerdatei XPrtDefs.h in Ihr Projekt ein.

 

Nachdem Sie ein Erfassungsgerät ausgewählt und eine Instanz des Erfassungsfilters erstellt haben, fragen Sie den Filter nach diesen Schnittstellen ab. Im folgenden Beispiel wird eine benutzerdefinierte -Struktur deklariert, die die Schnittstellenzeiger zusammen mit booleschen Werten enthält, die die Verfügbarkeit der einzelnen Schnittstellen angeben:


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

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



