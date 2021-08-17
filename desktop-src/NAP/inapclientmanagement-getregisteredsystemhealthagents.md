---
title: INapClientManagement GetRegisteredSystemHealthAgents-Methode (NapManagement.h)
description: Ruft Informationen zu den registrierten SHAs ab.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- GetRegisteredSystemHealthAgents-Methode NAP
- GetRegisteredSystemHealthAgents-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP, GetRegisteredSystemHealthAgents-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d9c2792282245ad4903d77700f5413bef0d2f769a65753aed60f50ba759707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800110"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>INapClientManagement::GetRegisteredSystemHealthAgents-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **GetRegisteredSystemHealthAgents-Methode** ruft Informationen zu den registrierten SHAs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ out\]
</dt> <dd>

Ein Zeiger auf [**systemHealthEntityCount,**](nap-datatypes.md) der die Anzahl registrierter SHAs beschreibt.

</dd> <dt>

*Agents* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von [**NapComponentRegistrationInfo-Strukturen,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die registrierten SHAs beschreiben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl> | Der NapAgent wird nicht ausgeführt.<br/>                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





