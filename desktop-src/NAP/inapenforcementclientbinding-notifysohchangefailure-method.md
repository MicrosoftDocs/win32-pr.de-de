---
title: INapEnforcementClientBinding NotifySoHChangeFailure-Methode (NapEnforcementClient.h)
description: Wird vom Erzwingungsclient verwendet, um napAgent darüber zu informieren, dass er eine vorherige INapEnforcementClientCallback NotifySoHChange nicht verarbeiten konnte.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- NotifySoHChangeFailure-Methode NAP
- NotifySoHChangeFailure-Methode NAP, INapEnforcementClientBinding-Schnittstelle
- INapEnforcementClientBinding-Schnittstelle NAP , NotifySoHChangeFailure-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f91ae79656ec8909a8bff041e3ddc2714f1cbd17a65362e08731e9ca411d57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134218"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>INapEnforcementClientBinding::NotifySoHChangeFailure-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapEnforcementClientBinding::NotifySoHChangeFailure-Methode** wird vom Erzwingungsclient verwendet, um den NapAgent darüber zu informieren, dass er einen [**vorherigen INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeiten konnte.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Der Enforcer wurde zuvor nicht initialisiert.<br/>       |



 

## <a name="remarks"></a>Hinweise

Als Ergebnis dieser Methode rufen Sie die NapAgent-Wiederholungen auf, indem Sie die SoH-Änderung zu einem späteren Zeitpunkt anwenden, indem [**Sie INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) erneut aufrufen. Sobald der Erzwingungsclient [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)aufgerufen hat, muss er die Änderung anwenden, d. h., nach diesem Punkt werden keine Fehler vom NapAgent behandelt.

Der Erzwingungsclient muss die [**INapEnforcementClientBinding::Initialize-Methode**](inapenforcementclientbinding-initialize-method.md) aufrufen, bevor er diese oder eine andere Methode der [**INapEnforcementClientBinding-Schnittstelle aufruft.**](inapenforcementclientbinding.md)

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


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





