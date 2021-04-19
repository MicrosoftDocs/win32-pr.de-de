---
title: Inapenforcementclientbinding-Methode zur uninitialisierung (napforcementclient. h)
description: Schließt den NAPAgent-Dienst ab.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Methode "NAP initialisieren"
- Uninitialize-Methode, NAP, inapenforcementclientbinding-Schnittstelle
- Inapenforcementclientbinding-Schnittstelle NAP, Uninitialize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342487"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>Inapenforcementclientbinding:: Uninitialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapenforcementclientbinding:: Uninitialize** -Methode beendet den NAPAgent-Dienst.

## <a name="syntax"></a>Syntax


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der NAPAgent blockiert die weitere Verarbeitung, bis alle vorhandenen Aufrufe an die [**inapenforcementclientbinding**](inapenforcementclientbinding.md) -Schnittstelle und die [**inapenforcementclientcallback**](inapenforcementclientcallback.md) -Schnittstelle vollständig sind. Am Ende dieses Aufrufes gibt der NAPAgent alle Verweise auf com-Zeiger für Erzwingungs Clients frei.

Bevor diese Funktion aufgerufen wird, muss der Enforcer für alle aktiven Verbindungen [**inapenforcementclientbinding:: notifyconnectionstatedown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) aufrufen, sodass die SHAs benachrichtigt werden können, wenn eine ihrer SoH-Requests verwaist ist.

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

[**Inapenforcementclientbinding:: notifyconnectionstatedown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**Inapenforcementclientcallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





