---
title: INapEnforcementClientConnection SetFlags-Methode (NapEnforcementClient.h)
description: Wird verwendet, um erstmalige Antworten von Antworten aufgrund von SoHRequests zu unterscheiden, die von den Erzwingern zwischengespeichert werden. | INapEnforcementClientConnection SetFlags-Methode (NapEnforcementClient.h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- SetFlags-Methode NAP
- SetFlags-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, SetFlags-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133992"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>INapEnforcementClientConnection::SetFlags-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::SetFlags-Methode** wird verwendet, um erstmalige Antworten von Antworten aufgrund von SoHRequests zu unterscheiden, die von den Erzwingern zwischengespeichert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Flags, die bestimmen, ob [**der SoHResponse-Wert**](/windows/win32/api/naptypes/ns-naptypes-soh) auf eine zwischengespeicherte **SoHRequest -Klasse zurückt.** Wenn *Flags* den Wert [**freshSoHRequest**](nap-type-constants.md)haben, handelt es sich um eine neue Anforderung. Andernfalls handelt es sich um eine zwischengespeicherte Anforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Wert wird vom NapAgent festgelegt.

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

 

 





