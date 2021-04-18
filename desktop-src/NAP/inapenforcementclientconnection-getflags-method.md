---
title: Inapenforcementclientconnection GetFlags-Methode (napforcementclient. h)
description: Wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden. | Inapenforcementclientconnection GetFlags-Methode (napforcementclient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- GetFlags-Methode NAP
- GetFlags-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, GetFlags-Methode
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
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106354944"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>Inapenforcementclientconnection:: GetFlags-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientconnection:: GetFlags** -Methode wird verwendet, um erstmalige Antworten von Antworten aufgrund von sohrequests zu unterscheiden, die von den-enforcern zwischengespeichert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Flag, das bestimmt, ob die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) auf einen zwischengespeicherten **sohrequest** zurückzuführen ist. Wenn *Flags* den Wert [**freshsohrequest**](nap-type-constants.md)hat, handelt es sich um eine neue Anforderung. andernfalls handelt es sich um eine zwischengespeicherte Anforderung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

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

 

 





