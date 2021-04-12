---
description: Decodersteuerelement
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Decodersteuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ce525f8b39e873d2c0002ac283014a9bcbe87c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392830"
---
# <a name="decoder-volume-control"></a><span data-ttu-id="c68e8-103">Decodersteuerelement</span><span class="sxs-lookup"><span data-stu-id="c68e8-103">Decoder Volume Control</span></span>

<span data-ttu-id="c68e8-104">Anwendungen steuern das audiovolume über die [**ibasicaudioschnittstelle**](/windows/desktop/api/Control/nn-control-ibasicaudio) .</span><span class="sxs-lookup"><span data-stu-id="c68e8-104">Applications control audio volume through the [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio) interface.</span></span> <span data-ttu-id="c68e8-105">Ein **ibasicaudioschnittstellen** Handler wird für ksproxy bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c68e8-105">An **IBasicAudio** interface handler is provided for KSProxy.</span></span> <span data-ttu-id="c68e8-106">Damit ein Decoder die volumebefehle aus ksproxy verarbeiten kann, muss er mehrere Registrierungsschlüssel in seinem Setup Skript hinzufügen und den Eigenschaften Satz " **kspropsetid \_ Wave** " unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c68e8-106">For a decoder to handle the volume commands from KSProxy, it must add several registry keys in its setup script and support the **KSPROPSETID\_Wave** property set.</span></span>

<span data-ttu-id="c68e8-107">Erstellen Sie einige neue Registrierungsschlüssel für den Treiber:</span><span class="sxs-lookup"><span data-stu-id="c68e8-107">Create some new registry keys for the driver:</span></span>


```C++
HKLM\SYSTEM\
  CurrentControlSet\Control
    DeviceClasses
      (decoder guid, eg 2721AE....)
        (Pnp id, eg ##?#VDGENDEV#...)
          #GLOBAL
            Device Parameters
              CLSID      REG_SZ   {17CCA...}
                FriendlyName   REG_SZ   WDM DVD Driver
                  Interfaces <--- create this key
                  {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
    MediaInterfaces
      {b9f8ac3e-0f71-11d2-b72c-00c04fb6bd3d} // Create this key.
        (default)  REG_SZ   'KsProxy IBasicAudio handler' // Set this value.
        IID        REG_SZ   56 a8 68 b3 0a d4 11 ce b0 3a 00 20 af 0b a7 70 
                            // Create this key.
```



<span data-ttu-id="c68e8-108">Um die volumesteuerung zu implementieren, muss der Treiber zusätzlich zum KsProperty.ID = ksproperty Wave Volume auch die **kspropantid- \_ Wave** unterstützen \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c68e8-108">To implement volume control, the driver also must support **KSPROPSETID\_Wave**, along with KsProperty.Id = KSPROPERTY\_WAVE\_VOLUME.</span></span> <span data-ttu-id="c68e8-109">Diese Eigenschaft wird über die Methoden " [**ikspropertyset:: Get**](ikspropertyset-get.md) " und " [**ikspropertyset:: set**](ikspropertyset-set.md) " an den Treiber übergeben.</span><span class="sxs-lookup"><span data-stu-id="c68e8-109">This property is passed to the driver through the [**IKsPropertySet::Get**](ikspropertyset-get.md) and [**IKsPropertySet::Set**](ikspropertyset-set.md) methods.</span></span> <span data-ttu-id="c68e8-110">In den Feldern "leftdämpfung" und "rightattentuations" werden die linken/rechten Lautsprecher Volumes als lineare Werte von 0x0000 bis 0xFFFF angegeben.</span><span class="sxs-lookup"><span data-stu-id="c68e8-110">The LeftAttenuation and RightAttentuation fields specify the left/right speaker volumes as linear values from 0x0000 to 0xffff.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c68e8-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c68e8-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c68e8-112">Decoder-Schnittstellen und Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="c68e8-112">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



