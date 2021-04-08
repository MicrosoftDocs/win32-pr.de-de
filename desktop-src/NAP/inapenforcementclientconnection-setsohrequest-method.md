---
title: Inapenforcementclientconnection setsohrequest-Methode (napforcementclient. h)
description: Legt die SoH-Anforderung fest.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Setsohrequest-Methode NAP
- Setsohrequest-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setsohrequest-Methode
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
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740912"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>Inapenforcementclientconnection:: setsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: setsohrequest** -Methode legt die SoH-Anforderung fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohrequest* \[ in\]
</dt> <dd>

Ein Zeiger auf eine eindeutige [**networksohrequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein undurchsichtiges Daten-BLOB für den-Enforcer handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Das SoH-Paket ist gültig.<br/>                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dies wird von NAPAgent festgelegt und von enforcern abgefragt, um die Übertragung zu senden.

Ein SoH-Paket mit einer Länge von 0 Bytes ist ungültig.

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

[**Inapenforcementclientconnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





