---
title: INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx-Methode (NapSystemHealthAgent.h)
description: Wird von SHAs aufgerufen, um den Isolationsstatus des Systems und den erweiterten Isolationsstatus zu bestimmen.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- GetSystemIsolationInfoEx-Methode NAP
- GetSystemIsolationInfoEx-Methode NAP, INapSystemHealthAgentBinding2-Schnittstelle
- INapSystemHealthAgentBinding2-Schnittstelle NAP, GetSystemIsolationInfoEx-Methode
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
ms.openlocfilehash: 4ac81d00bb953ddf3ab415e90724adcca34b302d8cc268699d8f2a820e0f34ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367828"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a>INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx-Methode** wird von SHAs aufgerufen, um den Isolationsstatus des Systems und den erweiterten Isolationsstatus zu bestimmen.

> [!Note]  
> Verwenden [**Sie INapSystemHealthAgentBinding::GetSystemIsolationInfo,**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) um nur den Isolationsstatus des Systems zu bestimmen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfoEx-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) die den erweiterten Isolationsstatus des Systems für bekannte Verbindungen enthält. *isolationInfo* gibt an, ob sich das System in einem Zustand mit eingeschränktem Zugriff, Probe oder uneingeschränktem Zugriff sowie [**ExtendedIsolationState-Informationen**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) befindet.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BOOL,** die **TRUE ist,** wenn verbindungen sich in einem unbekannten Zustand befinden, andernfalls **FALSE.**

</dd> </dl>

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

Die SHA muss die [**IsolationInfoEx-Struktur durch**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) Aufrufen [**von FreeIsolationInfoEx frei geben.**](freeisolationinfoex.md)

Der SHA muss [**Initialize aufrufen,**](inapsystemhealthagentbinding-initialize-method.md) bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2-Schnittstelle aufruft.**](inapsystemhealthagentbinding2.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





