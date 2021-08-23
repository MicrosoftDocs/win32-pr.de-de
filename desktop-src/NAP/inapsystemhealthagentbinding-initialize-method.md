---
title: INapSystemHealthAgentBinding Initialize-Methode (NapSystemHealthAgent.h)
description: Initialisiert den System health agent (SHA) und bindet den SHA an den NapAgent-Dienst.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Initialisieren der NAP-Methode
- Initialisieren der NAP-Methode, INapSystemHealthAgentBinding-Schnittstelle
- INapSystemHealthAgentBinding-Schnittstelle NAP , Initialize-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbe764d477c5f176fcaebc0825bbbcd02495ec70ee669a02c59258173cfbdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802710"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>INapSystemHealthAgentBinding::Initialize-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentBinding::Initialize-Methode initialisiert** den System health agent (SHA) und bindet den SHA an den NapAgent-Dienst. Diese Methode muss aufgerufen werden, bevor eine andere Methode für die [**INapSystemHealthAgentBinding2-Schnittstelle**](inapsystemhealthagentbinding2.md) aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Eine eindeutige [SystemHealthEntityId,](nap-datatypes.md) die die ID des SHA enthält, das an den NapAgent-Dienst gebunden wird.

</dd> <dt>

*Rückruf* \[ In\]
</dt> <dd>

Ein COM-Zeiger auf eine [**INapSystemHealthAgentCallback-Schnittstelle,**](inapsystemhealthagentcallback.md) die vom NapAgent verwendet wird, um den Integritäts-Agent mit einer Benachrichtigung/einem Prozess zurückzurufen. NapAgent enthält einen Verweis auf das Objekt, das dieser Schnittstelle zugeordnet ist, bis [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Berechtigungsfehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>                                                             |
| <dl> <dt>**FEHLER \_ WURDE BEREITS \_ INITIALISIERT**</dt> </dl> | Wenn der SHA zuvor initialisiert wurde, wird dieser Fehler zurückgegeben.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ NICHT \_ REGISTRIERT**</dt> </dl>     | Wenn der SHA zuvor nicht registriert wurde, wird dieser Fehler zurückgegeben.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ DISCONNECTED**</dt> </dl>        | Der NapAgent wurde beendet. Dieses Objekt wird nach dem Neustart automatisch wiederhergestellt und wieder an den NapAgent-Agent bindungiert.<br/> |



 

## <a name="remarks"></a>Hinweise

NapAgent löst aufgrund der Initialisierung keinen SoH-Austausch aus. Ein Systemzustands-Agent muss [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) aufrufen, um nach der Initialisierung mit napAgent einen Austausch von SoH-Paketen anzufordern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





