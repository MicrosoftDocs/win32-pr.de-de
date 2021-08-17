---
description: Die Enumeration AudioDeviceProperty wird von den Methoden ITAudioDeviceControl::GetRange, ITAudioDeviceControl::Get und ITAudioDeviceControl::Set verwendet, um die zu adressierte Eigenschaft anzugeben.
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: AudioDeviceProperty-Enumeration (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a634caa627f5d518e8783ce056e89a69931aa981466754a9d320f36787186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948792"
---
# <a name="audiodeviceproperty-enumeration"></a>AudioDeviceProperty-Enumeration

\[Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **AudioDeviceProperty-Enumeration** wird von den [**METHODEN ITAudioDeviceControl::GetRange,**](itaudiodevicecontrol-getrange.md) [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)und [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) verwendet, um die zu adressierte Eigenschaft anzugeben.

## <a name="syntax"></a>Syntax


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

Gibt an, dass der Duplexmodus des Geräts festgelegt oder abgerufen wird.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Gibt an, dass die automatische Steuerung des Gerätegewinns festgelegt oder abgerufen wird.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioGeräte \_ AkustikEchoCancellation**
</dt> <dd>

Gibt an, dass die Akustik-Echo-Abbrucheigenschaften des Geräts festgelegt oder abgerufen werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




