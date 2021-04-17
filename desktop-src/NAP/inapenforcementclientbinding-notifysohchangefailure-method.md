---
title: Inapenforcementclientbinding notifysohchangefailure-Methode (napforcementclient. h)
description: Wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger inapenforcementclientcallback notifysohchange nicht verarbeitet werden konnte.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Notifysohchangefailure-Methode NAP
- Notifysohchangefailure-Methode NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, notifysohchangefailure-Methode
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
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479263"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>Inapenforcementclientbinding:: notifysohchangefailure-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding:: notifysohchangefailure** -Methode wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeitet werden konnte.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt> </dl> | Der Enforcer wurde nicht bereits initialisiert.<br/>       |



 

## <a name="remarks"></a>Bemerkungen

Als Ergebnis dieses Methoden Aufrufs versucht NAPAgent, die SoH-Änderung zu einem späteren Zeitpunkt zu übernehmen, indem [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md) erneut aufgerufen wird. Nachdem der Erzwingungs Client [**inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md)aufgerufen hat, muss er die Änderung anwenden, d. h., nach diesem Punkt werden keine Fehler von der NAPAgent behandelt.

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
</dt> <dt>

[**Inapenforcementclientbinding:: getsohrequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**Inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





