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
# <a name="device-mode"></a><span data-ttu-id="2aead-103">Gerätemodus</span><span class="sxs-lookup"><span data-stu-id="2aead-103">Device Mode</span></span>

<span data-ttu-id="2aead-104">IEEE 1394-und USB-Camcorder können zwischen dem Kameramodus und dem VTR-Modus (Video Tape Recorder) wechseln.</span><span class="sxs-lookup"><span data-stu-id="2aead-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="2aead-105">Wenn ein IEEE 1394-Camcorder-Schalter Modi startet, setzt das Gerät zurück, und die Anwendung muss es erneut auflisten.</span><span class="sxs-lookup"><span data-stu-id="2aead-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="2aead-106">Es gibt keine Möglichkeit für eine Anwendung, den Modus Programm gesteuert zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="2aead-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="2aead-107">USB-Camcorder können dagegen zwischen Kamera-und VTR-Modi wechseln, ohne sie zurückzusetzen, und die Anwendung kann den Modus ändern.</span><span class="sxs-lookup"><span data-stu-id="2aead-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="2aead-108">**Msdv-Treiber**</span><span class="sxs-lookup"><span data-stu-id="2aead-108">**MSDV Driver**</span></span>

<span data-ttu-id="2aead-109">Um den aktuellen Modus auf einem IEEE 1394-Gerät abzurufen, müssen Sie die [**IAMExtDevice:: getcapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) -Methode mit dem Wert Ed \_ Devcap \_ Device \_ Type aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2aead-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="2aead-110">Wenn die Methode den Wert Ed \_ devtype \_ VCR zurückgibt, befindet sich das Gerät im VTR-Modus und verfügt über Funktionen wie anhalten, beenden, schnell vorwärts und zurückspulen.</span><span class="sxs-lookup"><span data-stu-id="2aead-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="2aead-111">Andernfalls, wenn die Methode Ed \_ devtype Camera zurückgibt \_ , befindet sich das Gerät im Kameramodus.</span><span class="sxs-lookup"><span data-stu-id="2aead-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="2aead-112">Im folgenden Codebeispiel wird gezeigt, wie der Gerätetyp abgefragt wird:</span><span class="sxs-lookup"><span data-stu-id="2aead-112">The following code example shows how to query the device type:</span></span>


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



<span data-ttu-id="2aead-113">Wenn der Camcorder offline geschaltet wird, sollten Sie ihn erneut Abfragen, wenn er zum nächsten Mal verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="2aead-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="2aead-114">Der Filter Graph-Manager stellt beim Entfernen des Geräts ein Ereignis zum [**\_ \_ Verlust eines EC-Geräts**](ec-device-lost.md) dar.</span><span class="sxs-lookup"><span data-stu-id="2aead-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="2aead-115">**UVC-Treiber**</span><span class="sxs-lookup"><span data-stu-id="2aead-115">**UVC Driver**</span></span>

<span data-ttu-id="2aead-116">Da auf USB-Videogeräten Modi ohne Zurücksetzen gewechselt werden können, ist der in den vorherigen Beispielen gezeigte Code für USB-Geräte nicht zuverlässig.</span><span class="sxs-lookup"><span data-stu-id="2aead-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="2aead-117">Verwenden Sie stattdessen die [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) -Schnittstelle, um den aktuellen Modus zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2aead-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="2aead-118">Sie können diese Schnittstelle auch verwenden, um Modi Programm gesteuert zu wechseln, wenn Sie vom Gerät unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2aead-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2aead-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2aead-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aead-120">Steuern eines DV-Camcorder</span><span class="sxs-lookup"><span data-stu-id="2aead-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



