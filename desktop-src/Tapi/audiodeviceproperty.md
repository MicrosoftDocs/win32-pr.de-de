---
description: 'Die audiodeviceproperty-Enumeration wird von den Methoden itaudiodevicecontrol:: GetRange, itaudiodevicecontrol:: Get und itaudiodevicecontrol:: Set verwendet, um die Eigenschaft anzugeben, die adressiert wird.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Audiodeviceproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367053"
---
# <a name="audiodeviceproperty-enumeration"></a>Audiodeviceproperty-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **audiodeviceproperty** -Enumeration wird von den Methoden [**itaudiodevicecontrol:: GetRange**](itaudiodevicecontrol-getrange.md), [**itaudiodevicecontrol:: Get**](itaudiodevicecontrol-get.md)und [**itaudiodevicecontrol**](itaudiodevicecontrol-set.md) :: Set verwendet, um die Eigenschaft anzugeben, die adressiert wird.

## <a name="syntax"></a>Syntax


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**Audiodevice- \_ duplexmode**
</dt> <dd>

Gibt an, dass der Duplex Modus des Geräts festgelegt oder abgerufen wird.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**Audiodevice \_ automaticgaincontrol**
</dt> <dd>

Gibt an, dass die automatische Erlangung der Steuerung des Geräts festgelegt oder abgerufen wird.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**Audiodevice- \_ acousticechoabbruch**
</dt> <dd>

Gibt an, dass die Eigenschaften für den akustischen Echo Abbruch des Geräts festgelegt oder abgerufen werden.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itaudiodebug econtrol:: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**Itaudiodebug econtrol:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**Itaudiode vicecontrol:: Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




