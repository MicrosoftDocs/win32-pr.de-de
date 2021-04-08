---
title: Inapsystemhealthagentcallback notifysystemisolationstatechange-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Notifysystemisolationstatechange-Methode NAP
- Notifysystemisolationstatechange-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, notifysystemsolationstatechange-Methode
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
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741953"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a>Inapsystemhealthagentcallback:: notifysystemsolationstatechange-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback:: notifysystemsolationstatechange** -Methode wird von NAPAgent aufgerufen, um anzugeben, dass sich der System Isolations Status oder die Endzeit der Bewährungszeit geändert hat.

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



 

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Der Integritäts-Agent kann den NAP-Systemstatus mithilfe von [**inapsystemhealthagentbinding:: getsystemsolationinfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md)Abfragen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





