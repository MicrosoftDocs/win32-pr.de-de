---
title: INapServerInfo GetRegisteredSystemHealthValidators-Methode (NapServerManagement.h)
description: Ruft eine Liste registrierter SHVs ab.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- NAP-Methode "GetRegisteredSystemHealthValidators"
- GetRegisteredSystemHealthValidators-Methode NAP, INapServerInfo-Schnittstelle
- INapServerInfo-Schnittstelle NAP , GetRegisteredSystemHealthValidators-Methode
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
ms.openlocfilehash: 54e096d706107ca812e569e46c980f56cdc7b8eba14f4742530f632570fd3d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133945"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>INapServerInfo::GetRegisteredSystemHealthValidators-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapServerInfo::GetRegisteredSystemHealthValidators-Methode** ruft eine Liste registrierter SHVs ab.

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

*count* \[ out\]
</dt> <dd>

Ein Zeiger auf ein [**SystemHealthEntityCount,das**](nap-type-constants.md) die Anzahl der registrierten SHVs enthält.

</dd> <dt>

*Validierungsprüfer* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**NapComponentRegistrationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die SHV-Registrierungsinformationen enthält.

</dd> <dt>

*validatorClsids* \[ out\]
</dt> <dd>

Zeiger auf ein Array von IDs für die registrierten SHVs.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





