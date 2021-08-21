---
title: INapEnforcementClientBinding GetSoHRequest-Methode (NapEnforcementClient.h)
description: Wird vom Erzwingungsclient verwendet, um eine SoH-Anforderung für eine bestimmte Verbindung abzurufen.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- GetSoHRequest-Methode NAP
- GetSoHRequest-Methode NAP, INapEnforcementClientBinding-Schnittstelle
- INapEnforcementClientBinding-Schnittstelle NAP, GetSoHRequest-Methode
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
ms.openlocfilehash: 780f144c6f4613006940069896aa8382006b179631acd83283121ee3c64ec0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134336"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>INapEnforcementClientBinding::GetSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapEnforcementClientBinding::GetSoHRequest-Methode** wird vom Erzwingungsclient verwendet, um eine SoH-Anforderung für eine bestimmte Verbindung abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Verbindung* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf eine [**INapEnforcementClientConnection-Schnittstelle.**](inapenforcementclientconnection.md) Der NapAgent enthält keine Verweise auf das -Objekt, das dieser Schnittstelle zugeordnet ist, nachdem die -Methode abgeschlossen wurde.

</dd> <dt>

*retriggerHint* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BOOL,** der angibt, ob die Verbindung erneut ausgelöst werden soll. Er ist **TRUE,** wenn [**sich soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) seit dem letzten Aufrufen dieser Funktion geändert hat oder [**wenn ProbationTime**](nap-datatypes.md) abgelaufen ist. Andernfalls **wird FALSE** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Der Erzwinger wurde noch nicht initialisiert.<br/>       |



 

## <a name="remarks"></a>Hinweise

Der NapAgent legt [**soHRequest für**](/windows/win32/api/naptypes/ns-naptypes-soh) das Verbindungsobjekt fest.

Wenn für [**diese Verbindung ein SoHRequest-Objekt**](/windows/win32/api/naptypes/ns-naptypes-soh) ausbrang, wird es verworfen, und die SHAs werden über verwaiste **SoHRequests benachrichtigt.**

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle**](inapenforcementclientbinding.md) aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





