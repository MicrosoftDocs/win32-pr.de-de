---
title: Inapclientmanagement getregisteredenforcementclients-Methode (napmanagement. h)
description: Ruft Informationen zu den registrierten Erzwingungs Clients ab.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Getregisteredenforcementclients-Methode NAP
- Getregisteredenforcementclients-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getregisteredenforcementclients-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477820"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Inapclientmanagement:: getregisteredenforcementclients-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getregisteredenforcementclients** -Methode ruft Informationen zu den registrierten Erzwingungs Clients ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**enforcemententitycount**](nap-datatypes.md) , die die Anzahl der registrierten Erzwingungs Clients enthält.

</dd> <dt>

*Enforcer* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Strukturen, die die registrierten Erzwingungs Clients beschreiben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl>       | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl> | Der NAPAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Napmanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napmanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapclientmanagement**](inapclientmanagement.md)
</dt> </dl>

 

 





