---
title: INapClientManagement UnregisterEnforcementClient-Methode (NapManagement.h)
description: Aufheben der Registrierung eines Erzwingungsclients beim NAP-System.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- UnregisterEnforcementClient-Methode NAP
- UnregisterEnforcementClient-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP, UnregisterEnforcementClient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0298b55a5552f2a3ce7a40e048874076729f7e506475c8626de9e9e343da3b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134552"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>INapClientManagement::UnregisterEnforcementClient-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Mit **der UnregisterEnforcementClient-Methode** wird die Registrierung eines Erzwingungsclients beim NAP-System aufgehoben.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Ein [**EnforcementEntityId-Wert,**](nap-datatypes.md) der den erzwingungsclient identifiziert, der die Registrierung aufheben soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                               |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>             |
| <dl> <dt>**NAP \_ E \_ NOCH \_ GEBUNDEN**</dt> </dl> | Die Registrierung des Erzwingungsclients konnte nicht aufgehoben werden und bleibt gebunden.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                         |
| Header<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





