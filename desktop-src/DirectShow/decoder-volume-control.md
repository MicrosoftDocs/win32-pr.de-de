---
description: Decoder-Volumesteuerung
ms.assetid: 94d68722-a0c2-47a7-a0a0-ae315f8f31ed
title: Decoder-Volumesteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e96ed9efb17a4fb32c41d8b10313edbe015c202b7f7d1f4287e1af20cca559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953149"
---
# <a name="decoder-volume-control"></a>Decoder-Volumesteuerung

Anwendungen steuern das Audiovolumen über die [**IBasicAudio-Schnittstelle.**](/windows/desktop/api/Control/nn-control-ibasicaudio) Für KSProxy wird **ein IBasicAudio-Schnittstellenhandler** bereitgestellt. Damit ein Decoder die Volumebefehle von KSProxy verarbeiten kann, muss er im Setupskript mehrere Registrierungsschlüssel hinzufügen und den **KSPROPSETID \_ Wave-Eigenschaftensatz** unterstützen.

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



Um die Volumesteuerung zu implementieren, muss der Treiber auch **KSPROPSETID \_ Wave** zusammen mit KsProperty.Id = KSPROPERTY \_ WAVE VOLUME \_ unterstützen. Diese Eigenschaft wird über die [**Methoden IKsPropertySet::Get**](ikspropertyset-get.md) und [**IKsPropertySet::Set**](ikspropertyset-set.md) an den Treiber übergeben. Die Felder LeftAttenuation und RightAttentuation geben die lautstärken links/rechten Lautsprecher als lineare Werte von 0x0000 bis 0xffff.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Decoderschnittstellen und Spezifikationen](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



