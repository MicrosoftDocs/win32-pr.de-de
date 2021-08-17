---
title: INapSystemHealthAgentRequest GetSoHRequest-Methode (NapSystemHealthAgent.h)
description: Kann von SHAs verwendet werden, um SoHs abzurufen, die zuvor von NapAgent zwischengespeichert wurden.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- GetSoHRequest-Methode NAP
- GetSoHRequest-Methode NAP, INapSystemHealthAgentRequest-Schnittstelle
- INapSystemHealthAgentRequest-Schnittstelle NAP , GetSoHRequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ec520180f3524f49fa95644b03fa5f982651bd4c2322542dc46cc3f85a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133519"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>INapSystemHealthAgentRequest::GetSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthAgentRequest::GetSoHRequest-Methode** kann von SHAs verwendet werden, um SoHs abzurufen, die zuvor von NapAgent zwischengespeichert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**SoHRequest-.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ NO \_ CACHED \_ SOH**</dt> </dl> | Die SoH wurde nicht gefunden. NapAgent verfügt nicht über eine zwischengespeicherte Kopie.<br/> |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Berechtigungsfehler, Zugriff verweigert.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagentrt.dll</dt> </dl>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





