---
description: Die Set-Methode legt den Wert einer angegebenen Eigenschaft für den Qualitäts Steuerungs Wert fest.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Itcallqualitycontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361502"
---
# <a name="itcallqualitycontrolset-method"></a>Itcallqualitycontrol:: Set-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Set** -Methode legt den Wert einer angegebenen [Eigenschaft für den Qualitäts Steuerungs](callqualityproperty.md)Wert fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**callqualityproperty**](callqualityproperty.md) -Enumeration.

</dd> <dt>

*Lvalue* \[ in\]
</dt> <dd>

Der gewünschte Wert für die-Eigenschaft.

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der *Eigenschafts* Wert gesteuert werden soll.

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

[**Itcallqualitycontrol**](itcallqualitycontrol.md)
</dt> <dt>

[**Tapicontrolflags**](tapicontrolflags.md)
</dt> <dt>

[**Callqualityproperty**](callqualityproperty.md)
</dt> </dl>

 

 




