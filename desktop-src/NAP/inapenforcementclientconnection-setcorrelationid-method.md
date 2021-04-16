---
title: Inapenforcementclientconnection setcorrelationid-Methode (napforcementclient. h)
description: Legt die ID fest, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Setcorrelationid-Methode NAP
- Setcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517576"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a>Inapenforcementclientconnection:: setcorrelationid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: setcorrelationid** -Methode legt die ID fest, die verwendet wird, um SoH-Requests und SoH-Antworten zu korrelieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ in\]
</dt> <dd>

Eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die einen bestimmten SoH-Austausch identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Korrelations-ID wird vom NAPAgent und auf der Grundlage der Verbindungs-ID festgelegt.

Diese ID wird verwendet, um Anforderungen und Antworten zu korrelieren, d. h., Sie beschreibt einen SoH-Austausch eindeutig und enthält immer die ID des letzten SoH, die für das Verbindungs Objekt festgelegt wurde.

Wenn ein SoH-Response empfangen wird, stellt der NAPAgent zunächst sicher, dass die IDs Stimmen. Wenn dies nicht der Fall ist, wird ein Fehler zurückgegeben, und der Enforcer muss das Paket löschen. Weitere Informationen finden Sie unter [**inapenforcementclientbinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .

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

 

 





