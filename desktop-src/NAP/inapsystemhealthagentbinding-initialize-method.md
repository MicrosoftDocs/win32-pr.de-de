---
title: Inapsystemhealthagentbinding Initialize-Methode (napsystemhealthagent. h)
description: Initialisiert den Systemintegritäts-Agent (SHA) und bindet den SHA an den NAPAgent-Dienst.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, Initialize-Methode
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
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340388"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>Inapsystemhealthagentbinding:: Initialize-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentbinding:: Initialize** -Methode initialisiert den Systemintegritäts-Agent (SHA) und bindet den SHA an den NAPAgent-Dienst. Diese Methode muss aufgerufen werden, bevor eine andere Methode in der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA enthält, der an den NAPAgent-Dienst gebunden ist.

</dd> <dt>

*Rückruf* \[ in\]
</dt> <dd>

Ein com-Zeiger auf eine [**inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md) -Schnittstelle, die vom NAPAgent verwendet wird, um den Integritäts-Agent mit einer Benachrichtigung/einem Prozess zu Rückruf. Der NAPAgent enthält einen Verweis auf das Objekt, das dieser Schnittstelle zugeordnet ist, bis die [**uninitialisierung**](inapsystemhealthagentbinding-uninitialize-method.md) aufgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                                | Beschreibung                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Vorgang erfolgreich.<br/>                                                                                                |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>            | Berechtigungs Fehler, Zugriff verweigert.<br/>                                                                                   |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>             | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>                                                             |
| <dl> <dt>**Fehler \_ bereits \_ Initialisiert**</dt> </dl> | Wenn das SHA zuvor initialisiert wurde, wird dieser Fehler zurückgegeben.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ nicht \_ registriert**</dt> </dl>     | Wenn der SHA nicht bereits zuvor registriert wurde, wird dieser Fehler zurückgegeben.<br/>                                                      |
| <dl> <dt>**RPC- \_ E \_ getrennt**</dt> </dl>        | Der NAPAgent wurde beendet. Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der "NAPAgent" löst keinen SoH-Austausch aufgrund der Initialisierung aus. Ein Systemintegritäts-Agent muss [**notifysohchange**](inapsystemhealthagentbinding-notifysohchange-method.md) anrufen, um nach der Initialisierung mit dem NAPAgent einen Austausch von SoH-Paketen anzufordern.

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

 

 





