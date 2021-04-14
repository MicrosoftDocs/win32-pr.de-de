---
title: Inapsystemhealthagentcallback notifis-Benachrichtigungsmethode (napsystemhealthagent. h)
description: Wird aufgerufen, wenn ein sohrequest vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Notisyorphanedsohrequest-Methode NAP
- Notisyorphanedsohrequest-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, notitelyorphanedsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392178"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>Inapsystemhealthagentcallback:: notieyorphanedsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentcallback:: notifyorphanedsohrequest** -Methode wird aufgerufen, wenn ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) vom SHA abgefragt wurde, die Antwort jedoch nie zurückgegeben wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ in\]
</dt> <dd>

Ein Zeiger auf die eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die den verwaisten [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh)identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Gibt die erfolgreiche Ausführung an.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Diese Methode kann vom System in den folgenden Fällen aufgerufen werden:

-   Ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) konnte nicht gesendet werden.
-   Ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) wurde über das Netzwerk gesendet, aber es wurde kein **sohresponse** zurückgegeben, d. h., es ist ein Timeout für den enforcern aufgetreten, oder auf der Serverseite ist kein entsprechender SHV vorhanden.
-   Die Verbindung wurde heruntergefahren, oder ein Enforcer wurde offline geschaltet.

Dies ist nur eine bestmögliche Benachrichtigung, daher dürfen sich SHAs nicht auf diese Informationen verlassen, um den Status zu bereinigen. Es gibt mehrere Situationen, in denen ein SHA nicht benachrichtigt wird:

-   Wenn ein Enforcer falsch verhält, bedeutet dies, dass das SHA nicht benachrichtigt wird, wenn der Verbindungsstatus nicht erfüllt ist.
-   , Wenn ein-Enforcer abstürzt.
-   In Fehlerzuständen, d. h., der NAPAgent verfügt nicht über genügend Arbeitsspeicher.

SHAs erhalten möglicherweise falsche Benachrichtigungen, wenn Sie zum ersten Mal eine Bindung an den NAPAgent herstellen, z. b. Wenn ein SoH-Austausch ausgeführt wird, wenn der SHA-gebunden ist, und dann ein Timeout auftritt.

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

 

 





