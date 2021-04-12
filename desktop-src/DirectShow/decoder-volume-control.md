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
# <a name="decoder-volume-control"></a>Decodersteuerelement

Anwendungen steuern das audiovolume über die [**ibasicaudioschnittstelle**](/windows/desktop/api/Control/nn-control-ibasicaudio) . Ein **ibasicaudioschnittstellen** Handler wird für ksproxy bereitgestellt. Damit ein Decoder die volumebefehle aus ksproxy verarbeiten kann, muss er mehrere Registrierungsschlüssel in seinem Setup Skript hinzufügen und den Eigenschaften Satz " **kspropsetid \_ Wave** " unterstützen.

Erstellen Sie einige neue Registrierungsschlüssel für den Treiber:


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



Um die volumesteuerung zu implementieren, muss der Treiber zusätzlich zum KsProperty.ID = ksproperty Wave Volume auch die **kspropantid- \_ Wave** unterstützen \_ \_ . Diese Eigenschaft wird über die Methoden " [**ikspropertyset:: Get**](ikspropertyset-get.md) " und " [**ikspropertyset:: set**](ikspropertyset-set.md) " an den Treiber übergeben. In den Feldern "leftdämpfung" und "rightattentuations" werden die linken/rechten Lautsprecher Volumes als lineare Werte von 0x0000 bis 0xFFFF angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Decoder-Schnittstellen und Spezifikationen](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



