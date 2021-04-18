---
title: Inapsystemhealthagentbinding flushcache-Methode (napsystemhealthagent. h)
description: Wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Flushcache-Methode NAP
- Flushcache-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, flushcache-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338316"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a>Inapsystemhealthagentbinding:: FLUSHCACHE-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentbinding:: FLUSHCACHE** -Methode wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.

## <a name="syntax"></a>Syntax


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                         | Beschreibung                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>               | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>     | Berechtigungs Fehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>      | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                                                             |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl> | Der NAPAgent wurde beendet. Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der NAPAgent verwaltet einen Cache aktueller SoHs, die von verschiedenen SHAs bereitgestellt werden. Dieser Cache ist nützlich, um die Leistung der Start Zeit zu optimieren, wenn SHAs an das System gebunden werden kann.

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

 

 





