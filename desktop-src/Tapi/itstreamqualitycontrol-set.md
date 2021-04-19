---
description: Die Set-Methode legt den Wert einer angegebenen Eigenschaft für die Streamqualität fest.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Itstreamqualitycontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372411"
---
# <a name="itstreamqualitycontrolset-method"></a>Itstreamqualitycontrol:: Set-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Set** -Methode legt den Wert einer angegebenen [**Eigenschaft für die Streamqualität**](streamqualityproperty.md)fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.

</dd> <dt>

*Lvalue* \[ in\]
</dt> <dd>

Gewünschter Wert für die input- *Eigenschaft*.

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der *Eigenschafts* Wert gesteuert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Wert                                                                                         | Bedeutung                                                         |
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

 

 




