---
title: Inapenforcementclientbinding getsohrequest-Methode (napforcementclient. h)
description: Wird vom Erzwingungs Client zum Abrufen einer SoH-Anforderung für eine bestimmte Verbindung verwendet.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, getsohrequest-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949669"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>Inapenforcementclientbinding:: getsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding:: getsohrequest** -Methode wird vom Erzwingungs Client zum Abrufen einer SoH-Anforderung für eine bestimmte Verbindung verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ in\]
</dt> <dd>

Ein com-Zeiger auf eine [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstelle. Der NAPAgent enthält keine Verweise auf das-Objekt, das dieser Schnittstelle zugeordnet ist, nachdem die-Methode abgeschlossen wurde.

</dd> <dt>

*retriggerhint* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **booleschen** Wert, der angibt, ob die Verbindung erneut ausgelöst werden soll. Es ist **true** , wenn sich der [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) seit dem letzten Aufruf dieser Funktion geändert hat oder wenn [**probationtime**](nap-datatypes.md) abgelaufen ist. Andernfalls wird **false** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt> </dl> | Der Enforcer wurde nicht bereits initialisiert.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Der NAPAgent legt die [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) für das Verbindungs Objekt fest.

Wenn für diese Verbindung eine [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) aussteht, wird sie verworfen, und die SHAs werden über verwaiste **sohrequests** benachrichtigt.

Der Erzwingungs Client muss die [**inapenforcementclientbinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) -Methode aufrufen, bevor diese oder eine andere Methode der [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle aufgerufen wird.

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


</dt> <dt>

[**Inapenforcementclientbinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





