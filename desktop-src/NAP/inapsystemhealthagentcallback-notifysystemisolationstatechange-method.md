---
title: INapSystemHealthAgentCallback NotifySystemIsolationStateChange-Methode (NapSystemHealthAgent.h)
description: Wird vom NapAgent aufgerufen, um anzugeben, dass sich der Isolationsstatus des Systems oder die Endzeit der Probe geändert hat.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- NotifySystemIsolationStateChange-Methode NAP
- NotifySystemIsolationStateChange-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP, NotifySystemIsolationStateChange-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc75686801148e0866f8996dabdb31af66eac9b55c60473782a794ea59f7463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621151"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>INapSystemHealthAgentCallback::NotifySystemIsolationStateChange-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange-Methode** wird vom NapAgent aufgerufen, um anzugeben, dass sich der Isolationsstatus des Systems oder die Endzeit der Probe geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Gibt die erfolgreiche Ausführung an.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der Integritäts-Agent kann den NAP-Systemstatus mithilfe von [**INapSystemHealthAgentBinding::GetSystemIsolationInfo abfragen.**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





