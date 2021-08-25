---
description: Die SetQOSApplicationID-Methode legt den QOS-Bezeichner für die Anwendung fest.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: ITQOSApplicationID::SetQOSApplicationID-Methode (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e7783efaf8ec30ea8f70fec634eefff0acd2f5df99453fc1958258a5a26597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774590"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a>ITQOSApplicationID::SetQOSApplicationID-Methode

\[Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **SetQOSApplicationID-Methode** legt den QOS-Bezeichner für die Anwendung fest.

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

*pApplicationID* \[ In\]
</dt> <dd>

Eindeutiger Bezeichner für den Anwendungsprozess.

</dd> <dt>

*pApplicationGUID* \[ In\]
</dt> <dd>

Anwendungs-GUID.

</dd> <dt>

*pSubIDs* \[ In\]
</dt> <dd>

Sub-IDs, die dem aktuellen Aufruf zugeordnet sind.

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

[**ITQOSApplicationID**](itqosapplicationid.md)
</dt> </dl>

 

 




