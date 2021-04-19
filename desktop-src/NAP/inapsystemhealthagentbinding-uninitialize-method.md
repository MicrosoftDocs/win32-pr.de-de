---
title: Inapsystemhealthagentbinding-Methode zur uninitialisierung (napsystemhealthagent. h)
description: Bewirkt, dass der NAPAgent alle Verweise auf com-Zeiger für den Systemintegritäts-Agent freigibt.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Methode "NAP initialisieren"
- Uninitialize-Methode, NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, Uninitialize-Methode
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
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339974"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a>Inapsystemhealthagentbinding:: Uninitialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentbinding:: Uninitialize** -Methode bewirkt, dass der NAPAgent alle Verweise auf com-Zeiger für den Systemintegritäts-Agent freigibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT Uninitialize();
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

Der NAPAgent blockiert die Ausführung dieses Methoden Aufrufs, bis alle vorhandenen Aufrufe an die Bindungs-und Rückruf Schnittstellen vollständig sind.

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

 

 





