---
description: Gerätemodus
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Gerätemodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482702"
---
# <a name="device-mode"></a>Gerätemodus

IEEE 1394-und USB-Camcorder können zwischen dem Kameramodus und dem VTR-Modus (Video Tape Recorder) wechseln. Wenn ein IEEE 1394-Camcorder-Schalter Modi startet, setzt das Gerät zurück, und die Anwendung muss es erneut auflisten. Es gibt keine Möglichkeit für eine Anwendung, den Modus Programm gesteuert zu wechseln. USB-Camcorder können dagegen zwischen Kamera-und VTR-Modi wechseln, ohne sie zurückzusetzen, und die Anwendung kann den Modus ändern.

**Msdv-Treiber**

Um den aktuellen Modus auf einem IEEE 1394-Gerät abzurufen, müssen Sie die [**IAMExtDevice:: getcapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) -Methode mit dem Wert Ed \_ Devcap \_ Device \_ Type aufrufen. Wenn die Methode den Wert Ed \_ devtype \_ VCR zurückgibt, befindet sich das Gerät im VTR-Modus und verfügt über Funktionen wie anhalten, beenden, schnell vorwärts und zurückspulen. Andernfalls, wenn die Methode Ed \_ devtype Camera zurückgibt \_ , befindet sich das Gerät im Kameramodus. Im folgenden Codebeispiel wird gezeigt, wie der Gerätetyp abgefragt wird:


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



Wenn der Camcorder offline geschaltet wird, sollten Sie ihn erneut Abfragen, wenn er zum nächsten Mal verfügbar wird. Der Filter Graph-Manager stellt beim Entfernen des Geräts ein Ereignis zum [**\_ \_ Verlust eines EC-Geräts**](ec-device-lost.md) dar.

**UVC-Treiber**

Da auf USB-Videogeräten Modi ohne Zurücksetzen gewechselt werden können, ist der in den vorherigen Beispielen gezeigte Code für USB-Geräte nicht zuverlässig. Verwenden Sie stattdessen die [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) -Schnittstelle, um den aktuellen Modus zu erhalten. Sie können diese Schnittstelle auch verwenden, um Modi Programm gesteuert zu wechseln, wenn Sie vom Gerät unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



