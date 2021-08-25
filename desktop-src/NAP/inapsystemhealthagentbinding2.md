---
title: INapSystemHealthAgentBinding2-Schnittstelle (NapSystemHealthAgent.h)
description: Die SHAs verwenden , um mit napAgent zu kommunizieren. | INapSystemHealthAgentBinding2-Schnittstelle (NapSystemHealthAgent.h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2-Schnittstelle NAP
- INapSystemHealthAgentBinding2-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42db59c23826855ca6cda7529eb9dcbbadfb2a1ee2a5aa93d9bd45587c45a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780930"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>INapSystemHealthAgentBinding2-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**INapSystemHealthAgentBinding2** stellt Methoden bereit, die die SHAs für die Kommunikation mit NapAgent verwenden.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthAgentBinding2-Schnittstelle** erbt von [**INapSystemHealthAgentBinding.**](inapsystemhealthagentbinding.md) **INapSystemHealthAgentBinding2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthAgentBinding2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                    | Beschreibung                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Wird von SHAs aufgerufen, um den Systemisolationsstatus und den erweiterten Isolationsstatus zu bestimmen.<br/> |



 

## <a name="remarks"></a>Hinweise

Alle APIs in dieser Schnittstelle geben **RPC \_ E \_ DISCONNECTED** zurück, wenn NapAgent beendet wird. Dieses Objekt wird nach dem Neustart automatisch wiederhergestellt und wieder an den NapAgent-Agent bindungiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





