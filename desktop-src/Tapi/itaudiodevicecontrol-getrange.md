---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine bestimmte Audiogeräteeigenschaft ab.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: ITAudioDeviceControl::GetRange-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87779131dea5bb01a1575074e4f019dbfa2a62addebf5b91a7eee6e9cc041710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003448"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>ITAudioDeviceControl::GetRange-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetRange-Methode** ruft den Bereich gültiger Werte für eine bestimmte [**Audiogeräteeigenschaft**](audiodeviceproperty.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ In\]
</dt> <dd>

Member der [**AudioDeviceProperty-Enumeration.**](audiodeviceproperty.md)

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Mindestens gültiger Wert für die Eingabeeigenschaft.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Maximal gültiger Wert für die Eingabeeigenschaft.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Inkrementieren, um das der Eigenschaftswert erhöht oder verringert werden kann.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Standardwert für den *Property-Parameter.*

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Der Wert der [**TAPIControlFlags-Enumeration,**](tapicontrolflags.md) der angibt, wie der *Eigenschaftswert* gesteuert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher zum Ausführen des Vorgangs vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




