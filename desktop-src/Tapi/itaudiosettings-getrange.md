---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine bestimmte Audioeinstellungseigenschaft ab.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: ITAudioSettings::GetRange-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f08c9eed736725bd4200c79583dcc12abde11399ec272be04805881752b19119
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992010"
---
# <a name="itaudiosettingsgetrange-method"></a>ITAudioSettings::GetRange-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetRange-Methode** ruft den Bereich gültiger Werte für eine bestimmte [**Audioeinstellungseigenschaft**](audiosettingsproperty.md)ab.

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

Member der [**AudioSettingsProperty-Enumeration.**](audiosettingsproperty.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITAudioSettings**](itaudiosettings.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioSettingsProperty**](audiosettingsproperty.md)
</dt> </dl>

 

 




