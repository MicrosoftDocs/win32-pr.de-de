---
title: INapClientManagement UnregisterSystemHealthAgent-Methode (NapManagement.h)
description: Aufheben der Registrierung eines SHA beim NAP-System.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- UnregisterSystemHealthAgent-Methode NAP
- UnregisterSystemHealthAgent-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP, UnregisterSystemHealthAgent-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad43df1c7edeb2525ff5c8901278d082c4ba299ea78d56c67a4380f8a7bab019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134508"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>INapClientManagement::UnregisterSystemHealthAgent-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Mit **der UnregisterSystemHealthAgent-Methode** wird die Registrierung eines SHA beim NAP-System aufgehoben.

## <a name="syntax"></a>Syntax


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Eine [**SystemHealthEntityId,**](nap-datatypes.md) die den Systemstatus-Agent identifiziert, für den die Registrierung aufgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                         | Beschreibung                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Vorgang erfolgreich.<br/>                                   |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>      | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**NAP \_ E \_ NOCH \_ GEBUNDEN**</dt> </dl> | Die SHA bleibt gebunden und konnte nicht aufgehoben werden.<br/>    |



 

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

 

 





