---
title: INapSystemHealthAgentBinding NotifySoHChange-Methode (NapSystemHealthAgent.h)
description: Wird von SHAs verwendet, wenn sich deren SoH ändert.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- NotifySoHChange-Methode NAP
- NotifySoHChange-Methode NAP, INapSystemHealthAgentBinding-Schnittstelle
- INapSystemHealthAgentBinding-Schnittstelle NAP , NotifySoHChange-Methode
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
ms.openlocfilehash: 0a418a78e0d21178f3dd1889816873afb1c7ec7212da48be5d75e44d40d0a61d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367838"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a>INapSystemHealthAgentBinding::NotifySoHChange-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentBinding::NotifySoHChange-Methode** wird von SHAs verwendet, wenn sich deren SoH ändert.

## <a name="syntax"></a>Syntax


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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

SHAs dürfen diese API nicht spekulativ aufrufen, da sie zu einem SoH-Austausch im Kabel führt. Aufrufe dieser API sollten nur bei Bedarf erfolgen.

Der NapAgent enthält diesen Thread nicht, um die SoH-Änderung zu verarbeiten. Stattdessen wird sofort zurückgegeben und die Änderung asynchron verarbeitet.

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

 

 





