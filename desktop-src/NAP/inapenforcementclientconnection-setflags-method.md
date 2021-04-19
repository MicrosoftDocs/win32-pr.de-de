---
title: Inapenforcementclientconnection setFlags-Methode (napforcementclient. h)
description: Wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden. | Inapenforcementclientconnection setFlags-Methode (napforcementclient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- SetFlags-Methode NAP
- SetFlags-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setFlags-Methode
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
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355765"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>Inapenforcementclientconnection:: setFlags-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: setFlags** -Methode wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Flags, die bestimmen, ob die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) auf einen zwischengespeicherten **sohrequest** zurückzuführen ist. Wenn *Flags* den Wert [**freshsohrequest**](nap-type-constants.md)hat, handelt es sich um eine neue Anforderung. andernfalls handelt es sich um eine zwischengespeicherte Anforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Wert wird von NAPAgent festgelegt.

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

 

 





