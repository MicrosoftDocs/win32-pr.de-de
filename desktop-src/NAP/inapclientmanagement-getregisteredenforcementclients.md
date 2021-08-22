---
title: INapClientManagement GetRegisteredEnforcementClients-Methode (NapManagement.h)
description: Ruft Informationen zu den registrierten Erzwingungsclients ab.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- NAP-Methode "GetRegisteredEnforcementClients"
- GetRegisteredEnforcementClients-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP , GetRegisteredEnforcementClients-Methode
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
ms.openlocfilehash: ae7854a36ffb1d313a1598764c5375a8146471c1b2fd930b4022948f147acc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940208"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>INapClientManagement::GetRegisteredEnforcementClients-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **GetRegisteredEnforcementClients-Methode** ruft Informationen zu den registrierten Erzwingungsclients ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Ein Zeiger auf [**enforcementEntityCount,**](nap-datatypes.md) der die Anzahl der registrierten Erzwingungsclients enthält.

</dd> <dt>

*Erzwingen von* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NapComponentRegistrationInfo-Strukturen,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die registrierten Erzwingungsclients beschreiben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl> | NapAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





