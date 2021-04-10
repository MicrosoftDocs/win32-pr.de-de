---
title: Inapclientmanagement-Schnittstelle (napmanagement. h)
description: Stellt Methoden für die NAP-Client Verwaltung bereit. | Inapclientmanagement-Schnittstelle (napmanagement. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Inapclientmanagement-Schnittstelle NAP
- Inapclientmanagement Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961446"
---
# <a name="inapclientmanagement-interface"></a>Inapclientmanagement-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapclientmanagement** -Schnittstelle bietet Methoden für die NAP-Client Verwaltung.

> [!Note]  
> [**INapClientManagement2**](inapclientmanagement2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **inapclientmanagement** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapclientmanagement** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapclientmanagement** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                | BESCHREIBUNG                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Inapclientmanagement:: getnapclientinfo**](inapclientmanagement-getnapclientinfo.md)                               | Ruft Informationen zu einem NAP-Client ab.<br/>                          |
| [**Inapclientmanagement:: getregisteredenforcementclients**](inapclientmanagement-getregisteredenforcementclients.md) | Ruft Informationen zu den registrierten Erzwingungs Clients ab.<br/>    |
| [**Inapclientmanagement:: getregisteredsystemhealthagents**](inapclientmanagement-getregisteredsystemhealthagents.md) | Abrufen von Informationen zu einem registrierten SHA.<br/>                       |
| [**Inapclientmanagement:: getsystemisolationinfo**](inapclientmanagement-getsystemisolationinfo.md)                   | Ruft Informationen zum Isolations Status des NAP-Clients ab.<br/> |
| [**Inapclientmanagement:: registerenforcementclient**](inapclientmanagement-registerenforcementclient.md)             | Registriert einen Erzwingungs Client beim NAP-System.<br/>               |
| [**Inapclientmanagement:: registersystemhealthagent**](inapclientmanagement-registersystemhealthagent.md)             | Registriert einen SHA beim NAP-System.<br/>                              |
| [**Inapclientmanagement:: unregisterenforcementclient**](inapclientmanagement-unregisterenforcementclient.md)         | Hebt die Registrierung eines Erzwingungs Clients beim NAP-System auf.<br/>             |
| [**Inapclientmanagement:: unregistersystemhealthagent**](inapclientmanagement-unregistersystemhealthagent.md)         | Hebt die Registrierung eines SHA beim NAP-System auf.<br/>                            |



 

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

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

