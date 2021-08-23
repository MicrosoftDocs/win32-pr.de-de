---
description: Die Set-Methode legt den Wert einer angegebenen Eigenschaft für die Aufrufqualitätssteuerung fest.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: ITCallQualityControl::Set-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5506e4c318440c2b611a2404590bdf638d34a7da2353a5598d09aecf2990668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003388"
---
# <a name="itcallqualitycontrolset-method"></a>ITCallQualityControl::Set-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **Set-Methode** legt den Wert einer angegebenen Eigenschaft für die [Aufrufqualitätssteuerung fest.](callqualityproperty.md)

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

*Eigenschaft* \[ In\]
</dt> <dd>

Member der [**CallQualityProperty-Enumerator.**](callqualityproperty.md)

</dd> <dt>

*lValue* \[ In\]
</dt> <dd>

Gewünschter Wert für die Eigenschaft.

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Der Wert der [**TAPIControlFlags-Aufenumerierung,**](tapicontrolflags.md) der angibt, wie der *Property-Wert* gesteuert werden soll.

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

 

 




