---
title: Inapsystemhealthagentrequest getcachesohflag-Methode (napsystemhealthagent. h)
description: Wird nur von NAPAgent verwendet.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Getcachesohflag-Methode NAP
- Getcachesohflag-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getcachesohflag-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518419"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a>Inapsystemhealthagentrequest:: getcachesohflag-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentrequest:: getcachesohflag** -Methode wird nur von NAPAgent verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cachesohforlateral use* 
</dt> <dd>

Ein **boolescher** Wert, der **true** ist, wenn der NAPAgent das [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) zwischenspeichern soll, andernfalls **false** .

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
| Header<br/>                   | <dl> <dt>Napsystemhealthagent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthagent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





