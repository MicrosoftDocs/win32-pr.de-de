---
description: Die Set-Methode legt den Wert einer bestimmten audiogeräteeigenschaft fest.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Itaudiodevicecontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366913"
---
# <a name="itaudiodevicecontrolset-method"></a>Itaudiodevicecontrol:: Set-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Set** -Methode legt den Wert einer bestimmten [**audiogeräteeigenschaft**](audiodeviceproperty.md)fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Eigenschaft* \[ in\]
</dt> <dd>

Member der [**audiodeviceproperty**](audiodeviceproperty.md) -Enumeration.

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

[**Itaudiodebug econtrol**](itaudiodevicecontrol.md)
</dt> <dt>

[**Tapicontrolflags**](tapicontrolflags.md)
</dt> <dt>

[**Audiodeviceproperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




