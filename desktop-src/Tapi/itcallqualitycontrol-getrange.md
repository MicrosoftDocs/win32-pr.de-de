---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine bestimmte Eigenschaft der Aufrufqualität ab.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: ITCallQualityControl::GetRange-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8d21c9266e64a9bcb31da0028a0ea28b8de98793d56d5bcf28c791c5497756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762436"
---
# <a name="itcallqualitycontrolgetrange-method"></a>ITCallQualityControl::GetRange-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetRange-Methode** ruft den Bereich gültiger Werte für eine bestimmte [Aufrufqualitätseigenschaft ab.](callqualityproperty.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ In\]
</dt> <dd>

Member der [**CallQualityProperty-Enumerator.**](callqualityproperty.md)

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Minimal gültiger Wert für die Eingabeeigenschaft.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Maximal gültiger Wert für die Eingabeeigenschaft.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Inkrement, um das der Eigenschaftswert erhöht oder verringert werden kann.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Standardwert für den *Property-Parameter.*

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITCallQualityControl**](itcallqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**CallQualityProperty**](callqualityproperty.md)
</dt> </dl>

 

 




