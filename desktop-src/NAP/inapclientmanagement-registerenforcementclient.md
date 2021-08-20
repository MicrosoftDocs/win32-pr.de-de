---
title: INapClientManagement RegisterEnforcementClient-Methode (NapManagement.h)
description: Registriert einen Erzwingungsclient beim NAP-System.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- RegisterEnforcementClient-Methode NAP
- RegisterEnforcementClient-Methode NAP, INapClientManagement-Schnittstelle
- INapClientManagement-Schnittstelle NAP, RegisterEnforcementClient-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e22deffb8f144e8f7176bd78fb18978228a26251be5591df61a322e5da17d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134562"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>INapClientManagement::RegisterEnforcementClient-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **RegisterEnforcementClient-Methode** registriert einen Erzwingungsclient beim NAP-System.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enforcer* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**NapComponentRegistrationInfo-Datenstruktur,**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) die die Registrierungsinformationen enthält, die dem Erzwingungsclient zugeordnet sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die -Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.



| Rückgabecode                                                                                            | Beschreibung                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>                |
| <dl> <dt>**\_ \_ NAP-E-KONFLIKT-ID \_**</dt> </dl> | Ein Erzwingungs-Agent, der den angegebenen Bezeichner verwendet, ist bereits registriert.<br/> |



 

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

 

 





