---
title: INapEnforcementClientConnection-Schnittstelle (NapEnforcementClient.h)
description: Lassen Sie die Clientverbindungsverwaltung zu. | INapEnforcementClientConnection-Schnittstelle (NapEnforcementClient.h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- INapEnforcementClientConnection-Schnittstelle NAP
- INapEnforcementClientConnection-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba017ca0948c5769466be9ad43ef68dc5ff60e75ecea430c96a1e8b0c36ab1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686250"
---
# <a name="inapenforcementclientconnection-interface"></a>INapEnforcementClientConnection-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

**INapEnforcementClientConnection bietet** Methoden, die die Clientverbindungsverwaltung ermöglichen.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapEnforcementClientConnection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientConnection** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapEnforcementClientConnection-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                           | Beschreibung                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientConnection::GetConnectionId**](inapenforcementclientconnection-getconnectionid-method.md)               | Ruft die Verbindungs-ID des Clients ab.<br/>                                                                                          |
| [**INapEnforcementClientConnection::GetCorrelationId**](inapenforcementclientconnection-getcorrelationid-method.md)             | Ruft die ID ab, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.<br/>                                                                  |
| [**INapEnforcementClientConnection::GetEnforcerPrivateData**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Wird vom Erzwinger verwendet, um private Daten zu erhalten.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Ruft den Wert des Flags ab, das erstmalige Antworten von Antworten aufgrund von SoHRequests unterscheidet, die von den Erzwingern zwischengespeichert werden.<br/> |
| [**INapEnforcementClientConnection::GetIsolationInfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Wird verwendet, um die Isolationsinformationen des Clients zu erhalten.<br/>                                                                              |
| [**INapEnforcementClientConnection::GetMaxSize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Ruft die maximale Größe des SoH-Pakets für diesen Client ab.<br/>                                                                       |
| [**INapEnforcementClientConnection::GetPrivateData**](inapenforcementclientconnection-getprivatedata-method.md)                 | Wird vom NapAgent verwendet, um private Daten zu erhalten.<br/>                                                                                      |
| [**INapEnforcementClientConnection::GetSoHRequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Ruft die SoH-Anforderung ab.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::GetSoHResponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Ruft die SoH-Response, die vom Erzwingungsclient empfangen werden.<br/>                                                                      |
| [**INapEnforcementClientConnection::GetStringCorrelationId**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Ruft die Zeichenfolgenversion der CorrelationId ab. Wird hauptsächlich zu Protokollierungszwecken verwendet.<br/>                                             |
| [**INapEnforcementClientConnection::Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Initialisiert die Verbindung<br/>                                                                                                    |
| [**INapEnforcementClientConnection::SetConnectionId**](inapenforcementclientconnection-setconnectionid-method.md)               | Legt die Verbindungs-ID des Clients fest.<br/>                                                                                          |
| [**INapEnforcementClientConnection::SetCorrelationId**](inapenforcementclientconnection-setcorrelationid-method.md)             | Legt die ID fest, die zum Korrelieren von SoH-Anforderungen und SoH-Antworten verwendet wird.<br/>                                                                  |
| [**INapEnforcementClientConnection::SetEnforcerPrivateData**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Wird vom Erzwinger zum Festlegen privater Daten verwendet.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetFlags**](inapenforcementclientconnection-setflags-method.md)                             | Legt das Flag fest, das erstmalige Antworten von Antworten aufgrund von SoHRequests unterscheidet, die von Erzwingern zwischengespeichert werden.<br/>                  |
| [**INapEnforcementClientConnection::SetIsolationInfo**](inapenforcementclientconnection-setisolationinfo-method.md)             | Wird vom NapAgent zum Festlegen der Isolationsinformationen des Clients verwendet.<br/>                                                           |
| [**INapEnforcementClientConnection::SetMaxSize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Legt die maximale Größe des SoH-Pakets für diesen Client fest.<br/>                                                                       |
| [**INapEnforcementClientConnection::SetPrivateData**](inapenforcementclientconnection-setprivatedata-method.md)                 | Wird vom NapAgent zum Festlegen privater Daten verwendet.<br/>                                                                                      |
| [**INapEnforcementClientConnection::SetSoHRequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Legt die SoH-Anforderung fest.<br/>                                                                                                          |
| [**INapEnforcementClientConnection::SetSoHResponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Legt die SoH-Response fest und wird beim Empfang eines Pakets vom Erzwingungsclient verwendet.<br/>                                             |



 

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

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

