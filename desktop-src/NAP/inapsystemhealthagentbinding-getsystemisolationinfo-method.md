---
title: INapSystemHealthAgentBinding GetSystemIsolationInfo-Methode (NapSystemHealthAgent.h)
description: Wird von SHAs aufgerufen, um den Systemisolationsstatus zu bestimmen.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Nap-Methode "GetSystemIsolationInfo"
- GetSystemIsolationInfo-Methode NAP, INapSystemHealthAgentBinding-Schnittstelle
- INapSystemHealthAgentBinding-Schnittstelle NAP , GetSystemIsolationInfo-Methode
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
ms.openlocfilehash: 9058b78bcff60b27bb27f25f11b785a8cd341f9addafe1829c1e8a7f3fb02a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939557"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a>INapSystemHealthAgentBinding::GetSystemIsolationInfo-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentBinding::GetSystemIsolationInfo-Methode** wird von SHAs aufgerufen, um den Systemisolationsstatus zu bestimmen.

> [!Note]  
> Verwenden Sie [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx,**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) um den erweiterten Isolationsstatus des Systems zu bestimmen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isolationInfo* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo-Struktur,**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) die den Isolationsstatus des Systems für bekannte Verbindungen enthält. *isolationInfoindicates,* wenn sich das System im Zustand "Eingeschränkter Zugriff", "Test" oder "Uneingeschränkter Zugriff" befindet.

</dd> <dt>

*unknownConnections* \[ out\]
</dt> <dd>

Ein Zeiger auf eine **BOOL,** die **TRUE** ist, wenn sich Verbindungen in einem unbekannten Zustand befinden, andernfalls **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                             | Beschreibung                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Berechtigungsfehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>                                                             |
| <dl> <dt>**NAP \_ E \_ NICHT \_ INITIALISIERT**</dt> </dl> | Der SHA wurde zuvor nicht initialisiert.<br/>                                                                        |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl>     | Der NapAgent wurde beendet. Dieses Objekt wird nach dem Neustart automatisch wiederhergestellt und wieder an den NapAgent-Agent bindungiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Der SHA muss [**Initialize aufrufen,**](inapsystemhealthagentbinding-initialize-method.md) bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2-Schnittstelle**](inapsystemhealthagentbinding2.md) aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





