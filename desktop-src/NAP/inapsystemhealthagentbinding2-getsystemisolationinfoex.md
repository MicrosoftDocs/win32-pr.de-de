---
title: INapSystemHealthAgentBinding2 getsystemisolationinfoex-Methode (napsystemhealthagent. h)
description: Wird von SHAs aufgerufen, um den systemisolations Status und den erweiterten Isolations Status zu bestimmen.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Getsystemisolationinfoex-Methode NAP
- Getsystemisolationinfoex-Methode NAP, INapSystemHealthAgentBinding2-Schnittstelle
- INapSystemHealthAgentBinding2 Interface NAP, getsystemisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517933"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>INapSystemHealthAgentBinding2:: getsystemisolationinfoex-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentBinding2:: getsystemsolationinfoex** -Methode wird von SHAs aufgerufen, um den systemisolations Status und den erweiterten Isolations Status zu bestimmen.

> [!Note]  
> Verwenden Sie [**inapsystemhealthagentbinding:: getsystemsolationinfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) , um nur den Isolations Status des Systems zu ermitteln.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die den erweiterten Isolations Zustand des Systems für bekannte Verbindungen enthält. *IsolationInfo* gibt an, ob sich das System in einem Zustand mit eingeschränktem Zugriff, Bewährung oder uneingeschränktem Zugriff befindet, sowie [**extendedisolationstate**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) -Informationen.

</dd> <dt>

*unknownconnections* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen **booleschen** Wert, der **true** ist, wenn sich Verbindungen in einem unbekannten Zustand befinden, andernfalls **false** .

</dd> </dl>

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

Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.

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

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





