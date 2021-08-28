---
title: INapEnforcementClientConnection GetCorrelationId-Methode (NapEnforcementClient.h)
description: Ruft die ID ab, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- GetCorrelationId-Methode NAP
- GetCorrelationId-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, GetCorrelationId-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1045513d672afbbd4e53f956f03b1f4db2a925cf756c158303a17998bcf219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940077"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>INapEnforcementClientConnection::GetCorrelationId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::GetCorrelationId-Methode** ruft die ID ab, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Eine eindeutige [**CorrelationId-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-correlationid) die diesen SoH-Austausch identifiziert.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





