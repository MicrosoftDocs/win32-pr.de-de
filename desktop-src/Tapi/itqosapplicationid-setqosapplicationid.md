---
description: Die setqosapplicationid-Methode legt den QoS-Bezeichner für die Anwendung fest.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Itqosapplicationid:: setqosapplicationid-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372505"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>Itqosapplicationid:: setqosapplicationid-Methode

\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **setqosapplicationid** -Methode legt den QoS-Bezeichner für die Anwendung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*papplicationid* \[ in\]
</dt> <dd>

Eindeutiger Bezeichner für den Anwendungsprozess.

</dd> <dt>

*papplicationguid* \[ in\]
</dt> <dd>

Anwendungs-GUID.

</dd> <dt>

*psugebote* \[ in\]
</dt> <dd>

Sub-IDs dem aktuellen-Befehl zugeordnet.

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

[**Itqosapplicationid**](itqosapplicationid.md)
</dt> </dl>

 

 




