---
title: INapEnforcementClientConnection SetSoHResponse-Methode (NapEnforcementClient.h)
description: Legt die SoH-Response fest und wird beim Empfang eines Pakets vom Erzwingungsclient verwendet.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- SetSoHResponse-Methode NAP
- SetSoHResponse-Methode NAP, INapEnforcementClientConnection-Schnittstelle
- INapEnforcementClientConnection-Schnittstelle NAP, SetSoHResponse-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a86c1a0fc86fcef9189f9d575063cee9abdf627e1cf3c58e68d669358142f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626230"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>INapEnforcementClientConnection::SetSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientConnection::SetSoHResponse-Methode** legt die SoH-Response fest und wird vom Erzwingungsclient beim Empfang eines Pakets verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohResponse* \[ In\]
</dt> <dd>

Ein Zeiger auf eine eindeutige [**NetworkSoHResponse-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-networksoh) bei der es sich um ein nicht transparentes Datenblob für den Erzwinger handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Das SoH-Paket ist gültig.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein Paket der Größe 0 (null) ist gültig.

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

 

 





