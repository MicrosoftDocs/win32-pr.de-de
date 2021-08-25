---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine bestimmte Streamqualitätseigenschaft ab.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: ITStreamQualityControl::GetRange-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13d07b848ef3be744f40ec1ba4bb4a73514f88204fa1918db661e00d36019ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774470"
---
# <a name="itstreamqualitycontrolgetrange-method"></a>ITStreamQualityControl::GetRange-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **GetRange-Methode** ruft den Bereich gültiger Werte für eine bestimmte [**Streamqualitätseigenschaft ab.**](streamqualityproperty.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ In\]
</dt> <dd>

Member der [**StreamQualityProperty-Aufenumerung.**](streamqualityproperty.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITStreamQualityControl**](itstreamqualitycontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**StreamQualityProperty**](streamqualityproperty.md)
</dt> </dl>

 

 




