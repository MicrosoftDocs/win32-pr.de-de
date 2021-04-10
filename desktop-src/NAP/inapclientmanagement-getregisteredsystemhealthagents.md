---
title: Inapclientmanagement getregisteredsystemhealthagents-Methode (napmanagement. h)
description: Ruft Informationen über die registrierten SHAs ab.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Getregisteredsystemhealthagents-Methode NAP
- Getregisteredsystemhealthagents-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getregisteredsystemhealthagents-Methode
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
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956770"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>Inapclientmanagement:: getregisteredsystemhealthagents-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **getregisteredsystemhealthagents** -Methode ruft Informationen über die registrierten SHAs ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen [**systemhealthentitycount**](nap-datatypes.md) , der die Anzahl der registrierten SHAs beschreibt.

</dd> <dt>

*Agents* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von [**napcomponentregistrationinfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) -Strukturen, das die registrierten SHAs beschreibt.

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

 

 





