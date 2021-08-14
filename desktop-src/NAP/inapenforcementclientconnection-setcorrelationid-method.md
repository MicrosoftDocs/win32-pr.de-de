---
title: INapEnforcementClientConnection SetCorrelationId-Methode (NapEnforcementClient.h)
description: Legt die ID fest, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- SetCorrelationId-Methode NAP
- SetCorrelationId-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, SetCorrelationId-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be8a7fbcbe9e2accd074768b8a0e50d6ce2dcaa2bda53e063cb76d294ff92c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368260"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>INapEnforcementClientConnection::SetCorrelationId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::SetCorrelationId-Methode** legt die ID fest, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ In\]
</dt> <dd>

Eine eindeutige [**CorrelationId-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-correlationid) die einen bestimmten SoH-Austausch identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Die Korrelations-ID wird vom NapAgent festgelegt und basiert auf der Verbindungs-ID.

Diese ID wird verwendet, um Anforderungen und Antworten zu korrelieren, d. h., sie beschreibt eindeutig einen SoH-Austausch und enthält immer die ID des letzten SoH-Sets für das Verbindungsobjekt.

Wenn ein SoH-Response empfangen wird, stellt NapAgent zunächst sicher, dass die IDs übereinstimmen. Wenn dies nicht der Fall ist, wird ein Fehler zurückgegeben, und der Erzwinger muss das Paket ablegen. Weitere Informationen finden Sie unter [**INapEnforcementClientBinding::P rocessSoHResponse.**](inapenforcementclientbinding-processsohresponse-method.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





