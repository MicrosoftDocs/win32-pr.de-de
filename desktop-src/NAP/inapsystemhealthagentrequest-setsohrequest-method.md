---
title: Inapsystemhealthagentrequest-setsohrequest-Methode (napsystemhealthagent. h)
description: Wird von Integritäts-Agents zum Schreiben der SoH-Anforderung verwendet, die sich aus dem Aufrufen von "inapsystemhealthagentcallback getsohrequest" ergibt.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Setsohrequest-Methode NAP
- Setsohrequest-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, setsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337312"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a>Inapsystemhealthagentrequest:: setsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentrequest:: setsohrequest** -Methode wird von Health-Agents verwendet, um Ihre SoH-Anforderung zu schreiben, die sich aus dem Aufrufen von [**inapsystemhealthagentcallback:: getsohrequest**](inapsystemhealthagentcallback-getsohrequest-method.md)ergibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohrequest* \[ in\]
</dt> <dd>

Ein Zeiger auf ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.

</dd> <dt>

*cachesohforlateral use* \[ in\]
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

 

 





