---
title: INapEnforcementClientConnection SetSoHRequest-Methode (NapEnforcementClient.h)
description: Legt die SoH-Anforderung fest.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- SetSoHRequest-Methode NAP
- SetSoHRequest-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, SetSoHRequest-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2d2d3a4574b086d49cba7d9c0afda72cf62621dbed37add8550a7ae2f93cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799634"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>INapEnforcementClientConnection::SetSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientConnection::SetSoHRequest-Methode** legt die SoH-Request fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohRequest* \[ In\]
</dt> <dd>

Ein Zeiger auf eine eindeutige [**NetworkSoHRequest-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-networksoh) bei der es sich um ein nicht transparentes Datenblob für den Erzwingenden handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Das SoH-Paket ist gültig.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Dies wird vom NapAgent festgelegt und von Erzwingenden abgefragt, die über die Leitung gesendet werden sollen.

Ein SoH-Paket mit einer Länge von 0 Byte ist ungültig.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





