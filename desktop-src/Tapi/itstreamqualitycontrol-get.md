---
description: Die Get-Methode ruft den Wert einer angegebenen Stream Quality-Eigenschaft ab.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Itstreamqualitycontrol:: Get-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356501"
---
# <a name="itstreamqualitycontrolget-method"></a>Itstreamqualitycontrol:: Get-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Get** -Methode ruft den Wert einer angegebenen [**Stream Quality-Eigenschaft**](streamqualityproperty.md)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.

</dd> <dt>

*plvalue* \[ vorgenommen\]
</dt> <dd>

Der Wert der input- *Eigenschaft*.

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

 

 




