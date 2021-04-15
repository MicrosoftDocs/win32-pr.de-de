---
title: Inapsystemhealthagentbinding getsystemsolationinfo-Methode (napsystemhealthagent. h)
description: Wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Getsystemisolationinfo-Methode NAP
- Getsystemsolationinfo-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, getsystemsolationinfo-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479047"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>Inapsystemhealthagentbinding:: getsystemsolationinfo-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentbinding:: getsystemsolationinfo** -Methode wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.

> [!Note]  
> Verwenden Sie [**INapSystemHealthAgentBinding2:: getsystemsolationinfoex**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) , um den erweiterten Isolations Status des Systems zu ermitteln.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsolationInfo* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die den Isolations Zustand des Systems für bekannte Verbindungen enthält. *isolationinfoweist darauf hin* , dass sich das System im Zustand eingeschränkten Zugriffs, Bewährung oder uneingeschränkten Zugriffs befindet.

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

 

 





