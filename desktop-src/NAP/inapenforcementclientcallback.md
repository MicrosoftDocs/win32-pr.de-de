---
title: INapEnforcementClientCallback-Schnittstelle (NapEnforcementClient.h)
description: Erzwingungsclients müssen implementieren, damit NapAgent mit ihnen kommunizieren kann.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- INapEnforcementClientCallback-Schnittstelle NAP
- INapEnforcementClientCallback-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a48c595918d28d912725353eb856de8f0af4541a68dabcb6f5a7cb0bb944496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134039"
---
# <a name="inapenforcementclientcallback-interface"></a>INapEnforcementClientCallback-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientCallback-Schnittstelle** stellt Rückrufmethoden bereit, die Erzwingungsclients implementieren müssen, damit NapAgent mit ihnen kommunizieren kann.

## <a name="members"></a>Member

Die **INapEnforcementClientCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapEnforcementClientCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                         | Beschreibung                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**INapEnforcementClientCallback::GetConnections**](inapenforcementclientcallback-getconnections-method.md)   | Wird vom NapAgent zum Abrufen von Verbindungen verwendet.<br/>                         |
| [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) | Wird vom NapAgent verwendet, um den Erzwingungsclient über SoH-Änderungen zu informieren.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



 

