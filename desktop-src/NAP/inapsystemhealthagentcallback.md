---
title: INapSystemHealthAgentCallback-Schnittstelle (NapSystemHealthAgent.h)
description: Werden vom System deklariert und vom SHA-Writer implementiert, damit NapAgent mit dem SHA kommunizieren kann.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- INapSystemHealthAgentCallback-Schnittstelle NAP
- INapSystemHealthAgentCallback-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7221dada78494f808ca0b98673b351a3a93c8088cc883bb7ed6324619c8ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799148"
---
# <a name="inapsystemhealthagentcallback-interface"></a>INapSystemHealthAgentCallback-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentCallback-Schnittstelle** stellt Rückrufmethoden bereit, die vom System deklariert und vom SHA-Writer implementiert werden, damit napAgent mit dem SHA kommunizieren kann.

## <a name="members"></a>Member

Die **INapSystemHealthAgentCallback-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthAgentCallback** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthAgentCallback-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                                           | Beschreibung                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthAgentCallback::CompareSoHRequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Wird vom SHA zum Vergleichen der SoHs verwendet.<br/>                                                                      |
| [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Wird vom NapAgent aufgerufen, um den Zustand des SHA zu bestimmen.<br/>                                                 |
| [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Wird vom NapAgent aufgerufen, um die SoH-Anforderung des SHA abzufragen.<br/>                                                    |
| [**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Wird aufgerufen, wenn eine SoH-Anforderung vom SHA abgefragt wurde, die Antwort jedoch nie zurückgelangt wurde.<br/>                      |
| [**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Wird vom NapAgent aufgerufen, um anzugeben, dass sich der Systemisolationsstatus oder die Testendzeit geändert haben.<br/> |
| [**INapSystemHealthAgentCallback::P rocessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Wird aufgerufen, wenn napAgent eine SoH-Antwort empfängt, die für diesen Integritäts-Agent bestimmt ist.<br/>                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

