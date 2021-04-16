---
title: Inapenforcementclientconnection setsohresponse-Methode (napforcementclient. h)
description: Legt den SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Setsohresponse-Methode NAP
- Setsohresponse-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setsohresponse-Methode
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
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478033"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>Inapenforcementclientconnection:: setsohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: setsohresponse** -Methode legt die SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohresponse* \[ in\]
</dt> <dd>

Ein Zeiger auf eine eindeutige [**networksohresponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Struktur, bei der es sich um ein undurchsichtiges Daten-BLOB für den-Enforcer handelt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Das SoH-Paket ist gültig.<br/>                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Paket mit 0 (null) ist gültig.

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

 

 





