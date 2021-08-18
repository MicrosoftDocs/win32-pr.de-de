---
title: INapEnforcementClientConnection SetConnectionId-Methode (NapEnforcementClient.h)
description: Wird zum Festlegen der eindeutigen ID der Verbindung verwendet und muss vom Erzwingungsclient festgelegt werden, sobald die Verbindung erstellt wird.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- SetConnectionId-Methode NAP
- SetConnectionId-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, SetConnectionId-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fdde438be329627645c7615453ff198e9c4f01f540684c27e8e3a5699e48499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939651"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a>INapEnforcementClientConnection::SetConnectionId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::SetConnectionId-Methode** wird zum Festlegen der eindeutigen ID der Verbindung verwendet und muss vom Erzwingungsclient festgelegt werden, sobald die Verbindung erstellt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*connectionId* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**ConnectionId,**](nap-datatypes.md) die eine Verbindung eindeutig identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese ConnectionID wird hauptsächlich zu Protokollierungszwecken verwendet.

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

 

 





