---
title: Inapservermanagement unregistersystemhealthvalidator-Methode (napservermanagement. h)
description: Wird verwendet, um die Registrierung eines SHV beim NAP-Server aufzuheben.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Unregistersystemhealthvalidator-Methode NAP
- Unregistersystemhealthvalidator-Methode NAP, inapservermanagement-Schnittstelle
- Inapservermanagement Interface NAP, unregistersystemhealthvalidator-Methode
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0715445504b862d9ae9e8478b543f8e80378f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518629"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>Inapservermanagement:: unregistersystemhealthvalidator-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapservermanagement:: unregistersystemhealthvalidator** -Methode wird verwendet, um die Registrierung eines SHV beim NAP-Server aufzuheben.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine [**systemhealthentityid**](nap-type-constants.md) , die den eindeutigen Bezeichner des SHV enthält, dessen Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn asynchrone Aufrufe für den SHV ausstehen, werden Sie zu einem späteren Zeitpunkt abgeschlossen und verworfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napservermanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napservermanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapservermanagement**](inapservermanagement.md)
</dt> </dl>

 

 





