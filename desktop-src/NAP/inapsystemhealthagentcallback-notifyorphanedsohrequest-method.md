---
title: INapSystemHealthAgentCallback NotifyOrphanedSoHRequest-Methode (NapSystemHealthAgent.h)
description: Wird aufgerufen, wenn eine SoHRequest vom SHA abgefragt wurde, aber die Antwort nie zurückgerufen wurde.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- NotifyOrphanedSoHRequest-Methode NAP
- NotifyOrphanedSoHRequest-Methode NAP, INapSystemHealthAgentCallback-Schnittstelle
- INapSystemHealthAgentCallback-Schnittstelle NAP , NotifyOrphanedSoHRequest-Methode
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
ms.openlocfilehash: 171191c266ae3fd59ab1ba8f55acd73eb143e9aa220fb3d2989a7ced9f716513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621181"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest-Methode** wird aufgerufen, wenn eine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) vom SHA abgefragt wurde, aber die Antwort nie zurückgerufen wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ In\]
</dt> <dd>

Ein Zeiger auf die eindeutige [**CorrelationId-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-correlationid) die die verwaiste [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                          | Beschreibung                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Gibt die erfolgreiche Ausführung an.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Rückrufmethode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.

Diese Methode kann vom System in den folgenden Fällen aufgerufen werden:

-   Eine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) konnte nicht über das Kabel gesendet werden.
-   Eine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) wurde über die Leitung gesendet, aber es wurde keine **SoHResponse** zurückgesendet, d. h., für den Erzwinger ist ein Time out aufgetreten, oder es gab keine entsprechende SHV auf serverseitiger Seite.
-   Die Verbindung wurde getrennt, oder ein Erzwinger wurde offline geschaltet.

Dies ist nur eine Best-Effort-Benachrichtigung, sodass SHAs sich nicht auf diese Informationen verlassen dürfen, um den Zustand zu bereinigen. Es gibt mehrere Situationen, in denen ein SHA nicht benachrichtigt wird:

-   Wenn sich ein Erzwinger nicht verhält, d. h. er benachrichtigt den SHA nicht, wenn der Verbindungsstatus nicht mehr besteht.
-   Wenn ein Erzwingungserzwinger abstürzt.
-   Bei Fehlerbedingungen, d. h., der NapAgent ist nicht genügend Arbeitsspeicher.

SHAs erhalten möglicherweise einige falsche Benachrichtigungen, wenn sie zum ersten Mal an napAgent gebunden werden, z. B. wenn ein SoH-Austausch ausgeführt wird, wenn die SHA-Bindung erfolgt, und dann tritt ein Times out auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





