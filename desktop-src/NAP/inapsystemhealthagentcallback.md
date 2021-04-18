---
title: Inapsystemhealthagentcallback-Schnittstelle (napsystemhealthagent. h)
description: Werden vom System deklariert und vom SHA-Writer implementiert, damit der NAPAgent mit dem SHA kommunizieren kann.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Inapsystemhealthagentcallback-Schnittstelle NAP
- Inapsystemhealthagentcallback-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341017"
---
# <a name="inapsystemhealthagentcallback-interface"></a>Inapsystemhealthagentcallback-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback** -Schnittstelle stellt Rückruf Methoden bereit, die vom System deklariert und vom SHA-Writer implementiert werden, damit der NAPAgent mit dem SHA kommunizieren kann.

## <a name="members"></a>Member

Die **inapsystemhealthagentcallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsystemhealthagentcallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsystemhealthagentcallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                                           | BESCHREIBUNG                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Inapsystemhealthagentcallback:: comparesohrequests**](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | Wird vom SHA zum Vergleichen der SoHs verwendet.<br/>                                                                      |
| [**Inapsystemhealthagentcallback:: getfixupinfo**](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | Wird von NAPAgent aufgerufen, um den Zustand des SHA zu bestimmen.<br/>                                                 |
| [**Inapsystemhealthagentcallback:: getsohrequest**](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | Wird von NAPAgent aufgerufen, um die SoH-Anforderung des SHA abzufragen.<br/>                                                    |
| [**Inapsystemhealthagentcallback:: notieyorphanedsohrequest**](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | Wird aufgerufen, wenn eine SoH-Anforderung vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.<br/>                      |
| [**Inapsystemhealthagentcallback:: notifysystemsolationstatechange**](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | Wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.<br/> |
| [**Inapsystemhealthagentcallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md)                             | Wird aufgerufen, wenn NAPAgent eine SoH-Antwort empfängt, die für diesen Integritäts-Agent bestimmt ist.<br/>                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

