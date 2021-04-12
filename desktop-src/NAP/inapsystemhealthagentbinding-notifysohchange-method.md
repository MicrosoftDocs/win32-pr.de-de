---
title: Inapsystemhealthagentbinding notifysohchange-Methode (napsystemhealthagent. h)
description: Wird von SHAs verwendet, wenn sich Ihr SoH ändert.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Notifysohchange-Methode NAP
- Notifysohchange-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, notifysohchange-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518947"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>Inapsystemhealthagentbinding:: notifysohchange-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentbinding:: notifysohchange** -Methode wird von SHAs verwendet, wenn Ihr SoH geändert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>         | Berechtigungs Fehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>          | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt> </dl> | Das SHA wurde nicht bereits initialisiert.<br/>                                                                        |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl>     | Der NAPAgent wurde beendet. Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

SHAs dürfen diese API nicht spekulativ aufrufen, da dies zu einem SoH-Austausch im Netzwerk führt. Aufrufe dieser API sollten nur bei Bedarf durchgeführt werden.

Der NAPAgent speichert diesen Thread nicht, um die SoH-Änderung zu verarbeiten. Stattdessen wird sofort zurückgegeben, und die Änderung wird asynchron verarbeitet.

Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





