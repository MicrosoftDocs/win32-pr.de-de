---
title: INapSystemHealthAgentBinding-Schnittstelle (NapSystemHealthAgent.h)
description: Die SHAs verwenden für die Kommunikation mit dem NapAgent. | INapSystemHealthAgentBinding-Schnittstelle (NapSystemHealthAgent.h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- INapSystemHealthAgentBinding-Schnittstelle NAP
- INapSystemHealthAgentBinding-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38fe66a5cd6883114ff46da3e98174d299f1813e670ed5ce67ee3843dc210d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799185"
---
# <a name="inapsystemhealthagentbinding-interface"></a>INapSystemHealthAgentBinding-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

**INapSystemHealthAgentBinding** stellt Methoden zur Kommunikation mit napAgent durch die SHAs zur Auswahl.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthAgentBinding-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentBinding** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthAgentBinding-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding::FlushCache**](inapsystemhealthagentbinding-flushcache-method.md)                         | Wird von einem SHA aufgerufen, um seinen SoH-Cache zu leeren.<br/>                                                |
| [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Wird von SHAs aufgerufen, um den Isolationsstatus des Systems zu bestimmen.<br/>                                 |
| [**INapSystemHealthAgentBinding::Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Initialisiert den SHA und bindet den SHA an den NapAgent-Dienst. <br/>                         |
| [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Wird von SHAs aufgerufen, wenn sich ihr SoH ändert.<br/>                                                  |
| [**INapSystemHealthAgentBinding::Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Wird von SHAs aufgerufen, um zu bewirken, dass napAgent alle seine Verweise auf SHA-COM-Zeiger frei gibt.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle APIs in dieser Schnittstelle geben **RPC \_ E \_ DISCONNECTED** zurück, wenn der NapAgent beendet wird. Dieses Objekt wird automatisch wiederhergestellt und erneut an den NapAgent gebunden, sobald es neu gestartet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

