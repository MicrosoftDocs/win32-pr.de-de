---
title: Inapenforcementclientconnection getcorrelationid-Methode (napforcementclient. h)
description: Ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- Getcorrelationid-Methode NAP
- Getcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041003"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a>Inapenforcementclientconnection:: getcorrelationid-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: getcorrelationid** -Methode ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ vorgenommen\]
</dt> <dd>

Eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die diesen SoH-Austausch identifiziert.

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

 

 





