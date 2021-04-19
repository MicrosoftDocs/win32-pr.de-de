---
title: Inapsystemhealthagentbinding-Schnittstelle (napsystemhealthagent. h)
description: Die SHAs, die für die Kommunikation mit dem NAPAgent verwendet werden. | Inapsystemhealthagentbinding-Schnittstelle (napsystemhealthagent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Inapsystemhealthagentbinding-Schnittstelle NAP
- Inapsystemhealthagentbinding-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363947"
---
# <a name="inapsystemhealthagentbinding-interface"></a>Inapsystemhealthagentbinding-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**Inapsystemhealthagentbinding** stellt Methoden bereit, die von den SHAs für die Kommunikation mit dem NAPAgent verwendet werden.

> [!Note]  
> [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **inapsystemhealthagentbinding** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsystemhealthagentbinding** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsystemhealthagentbinding** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                     | BESCHREIBUNG                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Inapsystemhealthagentbinding:: FLUSHCACHE**](inapsystemhealthagentbinding-flushcache-method.md)                         | Wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.<br/>                                                |
| [**Inapsystemhealthagentbinding:: getsystemsolationinfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | Wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.<br/>                                 |
| [**Inapsystemhealthagentbinding:: Initialize**](inapsystemhealthagentbinding-initialize-method.md)                         | Initialisiert das SHA und bindet das SHA an den NAPAgent-Dienst. <br/>                         |
| [**Inapsystemhealthagentbinding:: notifysohchange**](inapsystemhealthagentbinding-notifysohchange-method.md)               | Wird von SHAs aufgerufen, wenn sich Ihr SoH ändert.<br/>                                                  |
| [**Inapsystemhealthagentbinding:: Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md)                     | Wird von SHAs aufgerufen, damit der NAPAgent alle Verweise auf SHA-com-Zeiger freigibt.<br/> |



 

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

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

