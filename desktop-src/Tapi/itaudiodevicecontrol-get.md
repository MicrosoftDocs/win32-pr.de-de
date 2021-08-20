---
description: Die Get-Methode ruft den Wert einer bestimmten Audiogeräteeigenschaft ab.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: ITAudioDeviceControl::Get-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2877b48eab2ecab6259a034c9d74f4c32b9fae9233f5ceb0a0a409f43add014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865784"
---
# <a name="itaudiodevicecontrolget-method"></a>ITAudioDeviceControl::Get-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Get-Methode** ruft den Wert einer angegebenen [**Audiogeräteeigenschaft ab.**](audiodeviceproperty.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ In\]
</dt> <dd>

Member der [**AudioDeviceProperty-Enumerator.**](audiodeviceproperty.md)

</dd> <dt>

*plValue* \[ out\]
</dt> <dd>

Wert der *Eingabeeigenschaft*.

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Der Wert der [**TAPIControlFlags-Aufenumerierung,**](tapicontrolflags.md) der angibt, wie der *Eigenschaftswert* gesteuert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




