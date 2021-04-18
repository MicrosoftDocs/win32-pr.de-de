---
description: Die GetRange-Methode ruft den Bereich der gültigen Werte für eine angegebene Eigenschaft der Streamqualität ab.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'Itstreamqualitycontrol:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372412"
---
# <a name="itstreamqualitycontrolgetrange-method"></a>Itstreamqualitycontrol:: GetRange-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **GetRange** -Methode ruft den Bereich der gültigen Werte für eine angegebene [**Eigenschaft der Streamqualität**](streamqualityproperty.md)ab.

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

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.

</dd> <dt>

*plmin* \[ vorgenommen\]
</dt> <dd>

Der minimale gültige Wert für die Input-Eigenschaft.

</dd> <dt>

*plmax* \[ vorgenommen\]
</dt> <dd>

Maximal gültiger Wert für die Eingabe Eigenschaft.

</dd> <dt>

*plsteppingdelta* \[ vorgenommen\]
</dt> <dd>

Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.

</dd> <dt>

*pldefault* \[ vorgenommen\]
</dt> <dd>

Der Standardwert für den *Property* -Parameter.

</dd> <dt>

*plflags* \[ vorgenommen\]
</dt> <dd>

Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                   | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Methode war erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itstreamqualitycontrol**](itstreamqualitycontrol.md)
</dt> <dt>

[**Tapicontrolflags**](tapicontrolflags.md)
</dt> <dt>

[**Streamqualityproperty**](streamqualityproperty.md)
</dt> </dl>

 

 




