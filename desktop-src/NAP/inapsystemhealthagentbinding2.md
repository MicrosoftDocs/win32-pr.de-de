---
title: INapSystemHealthAgentBinding2-Schnittstelle (napsystemhealthagent. h)
description: Die SHAs, die für die Kommunikation mit dem NAPAgent verwendet werden. | INapSystemHealthAgentBinding2-Schnittstelle (napsystemhealthagent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2-Schnittstelle NAP
- INapSystemHealthAgentBinding2 Interface NAP, beschrieben
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
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352798"
---
# <a name="inapsystemhealthagentbinding2-interface"></a>INapSystemHealthAgentBinding2-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**INapSystemHealthAgentBinding2** stellt Methoden bereit, die von den SHAs für die Kommunikation mit dem NAPAgent verwendet werden.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthAgentBinding2** -Schnittstelle erbt von [**inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md). **INapSystemHealthAgentBinding2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthAgentBinding2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                    | BESCHREIBUNG                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentBinding2:: getsystemisolationinfoex**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | Wird von SHAs aufgerufen, um den systemisolations Zustand und den erweiterten Isolations Status zu bestimmen.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Alle APIs in dieser Schnittstelle geben **RPC \_ E \_ getrennt** zurück, wenn der NAPAgent angehalten wird. Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





