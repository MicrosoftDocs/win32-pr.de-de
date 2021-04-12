---
title: Inapenforcementclientconnection-Schnittstelle (napforcementclient. h)
description: Ermöglicht die clientverbindungsverwaltung. | Inapenforcementclientconnection-Schnittstelle (napforcementclient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Inapenforcementclientconnection-Schnittstelle NAP
- Inapenforcementclientconnection-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219184"
---
# <a name="inapenforcementclientconnection-interface"></a>Inapenforcementclientconnection-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection** stellt Methoden bereit, die die Client Verbindungs Verwaltung ermöglichen.

> [!Note]  
> [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **inapenforcementclientconnection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapenforcementclientconnection** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapenforcementclientconnection** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                           | BESCHREIBUNG                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inapenforcementclientconnection:: GetConnectionID**](inapenforcementclientconnection-getconnectionid-method.md)               | Ruft die Verbindungs-ID des Clients ab.<br/>                                                                                          |
| [**Inapenforcementclientconnection:: getcorrelationid**](inapenforcementclientconnection-getcorrelationid-method.md)             | Ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.<br/>                                                                  |
| [**Inapenforcementclientconnection:: getenforcerprivatedata**](inapenforcementclientconnection-getenforcerprivatedata-method.md) | Wird vom-Enforcer verwendet, um private Daten zu erhalten.<br/>                                                                                      |
| [**Inapenforcementclientconnection:: GetFlags**](inapenforcementclientconnection-getflags-method.md)                             | Ruft den Wert des Flags ab, das erstmalige Antworten von Antworten aufgrund von sohrequests unterscheidet, die von den-enforcern zwischengespeichert wurden.<br/> |
| [**Inapenforcementclientconnection:: getisolationinfo**](inapenforcementclientconnection-getisolationinfo-method.md)             | Wird verwendet, um die Isolations Informationen des Clients zu erhalten.<br/>                                                                              |
| [**Inapenforcementclientconnection:: getmaxsize**](inapenforcementclientconnection-getmaxsize-method.md)                         | Ruft die maximale Größe des SoH-Pakets für diesen Client ab.<br/>                                                                       |
| [**Inapenforcementclientconnection:: getprivatedata**](inapenforcementclientconnection-getprivatedata-method.md)                 | Wird vom NAPAgent verwendet, um private Daten zu erhalten.<br/>                                                                                      |
| [**Inapenforcementclientconnection:: getsohrequest**](inapenforcementclientconnection-getsohrequest-method.md)                   | Ruft die SoH-Anforderung ab.<br/>                                                                                                          |
| [**Inapenforcementclientconnection:: getsohresponse**](inapenforcementclientconnection-getsohresponse-method.md)                 | Ruft den SoH-Response ab, der vom Erzwingungs Client empfangen wurde.<br/>                                                                      |
| [**Inapenforcementclientconnection:: getstringcorrelationid**](inapenforcementclientconnection-getstringcorrelationid-method.md) | Ruft die Zeichen folgen Version von CorrelationId ab. Wird hauptsächlich für Protokollierungs Zwecke verwendet.<br/>                                             |
| [**Inapenforcementclientconnection:: Initialize**](inapenforcementclientconnection-initialize-method.md)                         | Initialisiert die Verbindung<br/>                                                                                                    |
| [**Inapenforcementclientconnection:: setconnectionid**](inapenforcementclientconnection-setconnectionid-method.md)               | Legt die Verbindungs-ID des Clients fest.<br/>                                                                                          |
| [**Inapenforcementclientconnection:: setcorrelationid**](inapenforcementclientconnection-setcorrelationid-method.md)             | Legt die ID fest, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.<br/>                                                                  |
| [**Inapenforcementclientconnection:: Setup Data**](inapenforcementclientconnection-setenforcerprivatedata-method.md) | Wird vom-Enforcer verwendet, um private Daten festzulegen.<br/>                                                                                      |
| [**Inapenforcementclientconnection:: setFlags**](inapenforcementclientconnection-setflags-method.md)                             | Legt das Flag fest, das erstmalige Antworten von Antworten aufgrund von sohrequests unterscheidet, die von enforcern zwischengespeichert wurden.<br/>                  |
| [**Inapenforcementclientconnection:: Setup Info**](inapenforcementclientconnection-setisolationinfo-method.md)             | Wird von NAPAgent zum Festlegen der Isolations Informationen des Clients verwendet.<br/>                                                           |
| [**Inapenforcementclientconnection:: setmaxsize**](inapenforcementclientconnection-setmaxsize-method.md)                         | Legt die maximale Größe des SoH-Pakets für diesen Client fest.<br/>                                                                       |
| [**Inapenforcementclientconnection:: setprivatedata**](inapenforcementclientconnection-setprivatedata-method.md)                 | Wird vom NAPAgent verwendet, um private Daten festzulegen.<br/>                                                                                      |
| [**Inapenforcementclientconnection:: setsohrequest**](inapenforcementclientconnection-setsohrequest-method.md)                   | Legt die SoH-Anforderung fest.<br/>                                                                                                          |
| [**Inapenforcementclientconnection:: setsohresponse**](inapenforcementclientconnection-setsohresponse-method.md)                 | Legt den SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.<br/>                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napforcementclient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napforcementclient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

