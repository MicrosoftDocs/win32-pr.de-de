---
title: INapEnforcementClientBinding Uninitialize-Methode (NapEnforcementClient.h)
description: Beendet den NapAgent-Dienst.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Uninitialize method NAP
- Uninitialize method NAP , INapEnforcementClientBinding interface (Nicht initialisieren der NAP-Methode, INapEnforcementClientBinding-Schnittstelle)
- INapEnforcementClientBinding-Schnittstelle NAP, Uninitialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613646eb169ab12c788cc294ab012962606a77b5f9fe5dfc8c041e6a4ad6fa35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940144"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>INapEnforcementClientBinding::Uninitialize-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientBinding::Uninitialize-Methode** schließt den NapAgent-Dienst ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

NapAgent blockiert die weitere Verarbeitung, bis alle vorhandenen Aufrufe der [**Schnittstellen INapEnforcementClientBinding**](inapenforcementclientbinding.md) und [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) abgeschlossen sind. Am Ende dieses Aufrufs gibt napAgent alle Seine Verweise auf COM-Zeiger des Erzwingungsclients frei.

Bevor diese Funktion aufgerufen wird, muss der Erzwinger [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) für alle aktiven Verbindungen aufrufen, damit die SHAs benachrichtigt werden können, wenn eine ihrer SoH-Requests verwaist war.

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle**](inapenforcementclientbinding.md) aufruft.

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





