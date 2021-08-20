---
title: INapEnforcementClientBinding-Schnittstelle (NapEnforcementClient.h)
description: Erzwingungsclients verwenden , um mit NapAgent zu kommunizieren.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding-Schnittstelle NAP
- INapEnforcementClientBinding-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad90e7f96a981a28e4c44351d5a2a4f55c75184826154e0e2effba54157049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134066"
---
# <a name="inapenforcementclientbinding-interface"></a>INapEnforcementClientBinding-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**Die INapEnforcementClientBinding** stellt Methoden bereit, mit denen Erzwingungsclients mit napAgent kommunizieren.

## <a name="members"></a>Member

Die **INapEnforcementClientBinding-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapEnforcementClientBinding** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapEnforcementClientBinding-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                           | Beschreibung                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapEnforcementClientBinding::CreateConnection**](inapenforcementclientbinding-createconnection-method.md)                   | Wird von Erzwingern zum Erstellen von Verbindungsobjekten verwendet.<br/>                                                                                                                                                            |
| [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)                         | Wird vom Erzwingungsclient verwendet, wenn er eine SoH-Anforderung für eine bestimmte Verbindung benötigt.<br/>                                                                                                                   |
| [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md)                               | Startet den NapAgent-Dienst. Der Erzwingungsclient muss diese Methode aufrufen, bevor er eine andere Methode dieser Schnittstelle aufruft.<br/>                                                                            |
| [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | Wird verwendet, um NapAgent darüber zu informieren, dass eine Verbindung mit einem Erzwingungsclient nicht mehr hergestellt wurde.<br/>                                                                                                                      |
| [**INapEnforcementClientBinding::NotifySoHChangeFailure**](inapenforcementclientbinding-notifysohchangefailure-method.md)       | Wird vom Erzwingungsclient verwendet, um napAgent darüber zu informieren, dass er einen [**vorherigen INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeiten konnte.<br/> |
| [**INapEnforcementClientBinding::P rocessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md)               | Wird von Erzwingungsclients verwendet, wenn sie ein SoH-Response Datenblob vom Erzwingungsserver erhalten.<br/>                                                                                                       |
| [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)                           | Schließt den NapAgent-Dienst für diese Clientverbindung ab.<br/>                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Alle APIs in dieser Schnittstelle geben RPC \_ E \_ DISCONNECTED zurück, wenn NapAgent beendet wird. Dieses Objekt wird nach dem Neustart automatisch wiederhergestellt und wieder an den NapAgent-Agent bindungiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
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

 

