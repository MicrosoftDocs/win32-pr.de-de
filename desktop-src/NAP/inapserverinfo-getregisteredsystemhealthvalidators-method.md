---
title: Inapserverinfo getregisteredsystemhealthvalidators-Methode (napservermanagement. h)
description: Ruft eine Liste registrierter SHVs ab.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Getregisteredsystemhealthvalidators-Methode NAP
- Getregisteredsystemhealthvalidators-Methode NAP, inapserverinfo-Schnittstelle
- Inapserverinfo-Schnittstelle NAP, getregisteredsystemhealthvalidators-Methode
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040875"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Inapserverinfo:: getregisteredsystemhealthvalidators-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapserverinfo:: getregisteredsystemhealthvalidators** -Methode ruft eine Liste registrierter SHVs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**systemhealthentitycount**](nap-type-constants.md) , die die Anzahl der registrierten SHVs enthält.

</dd> <dt>

*Validierungs Steuerelemente* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Struktur, die die SHV-Registrierungsinformationen enthält.

</dd> <dt>

*validatorclsids* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von IDs für die registrierten SHVs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

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

[**Napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**Inapserverinfo**](inapserverinfo.md)
</dt> </dl>

 

 





