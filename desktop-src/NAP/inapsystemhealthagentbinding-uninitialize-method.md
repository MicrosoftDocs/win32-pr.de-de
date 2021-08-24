---
title: INapSystemHealthAgentBinding Uninitialize-Methode (NapSystemHealthAgent.h)
description: Bewirkt, dass napAgent alle Verweise auf COM-Zeiger des Systemzustands-Agents frei gibt.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Uninitialize method NAP
- Nicht initialisieren der NAP-Methode, INapSystemHealthAgentBinding-Schnittstelle
- INapSystemHealthAgentBinding-Schnittstelle NAP, Uninitialize-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeefaad67130772a44103c721cc9f4efd02d3b43f54fc27c8d2f1bd40983522
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802760"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>INapSystemHealthAgentBinding::Uninitialize-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentBinding::Uninitialize-Methode** bewirkt, dass napAgent alle Seine Verweise auf COM-Zeiger des Systemzustands-Agents frei gibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Die SHA wurde noch nicht initialisiert.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl>     | Der NapAgent wurde beendet. Dieses Objekt wird automatisch wiederhergestellt und erneut an den NapAgent gebunden, sobald es neu gestartet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Der NapAgent blockiert die Ausführung dieses Methodenaufrufs, bis alle vorhandenen Aufrufe der Bindungs- und Rückrufschnittstellen abgeschlossen sind.

Der SHA muss [**Initialize aufrufen,**](inapsystemhealthagentbinding-initialize-method.md) bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2-Schnittstelle aufruft.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





