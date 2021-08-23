---
title: INapEnforcementClientConnection GetFlags-Methode (NapEnforcementClient.h)
description: Wird verwendet, um erste Antworten von Antworten aufgrund von SoHRequests zu unterscheiden, die von den Erzwingenden zwischengespeichert werden. | INapEnforcementClientConnection GetFlags-Methode (NapEnforcementClient.h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- GetFlags-Methode NAP
- GetFlags-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP , GetFlags-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3aea1815a8892f5d072f72d32d433070038b35cd663f10dfba08422a81153660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781050"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>INapEnforcementClientConnection::GetFlags-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection::GetFlags-Methode** wird verwendet, um Erste-Zeit-Antworten von Antworten zu unterscheiden, die von den Erzwingenden zwischengespeichert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Flag, das bestimmt, ob die [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) auf eine zwischengespeicherte **SoHRequest** zurückzuführen ist. Wenn *Flags* über den Wert [**freshSoHRequest**](nap-type-constants.md)verfügt, handelt es sich um eine neue Anforderung. Andernfalls handelt es sich um eine zwischengespeicherte Anforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





