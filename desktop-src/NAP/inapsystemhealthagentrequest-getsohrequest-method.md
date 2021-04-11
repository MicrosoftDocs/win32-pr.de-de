---
title: Inapsystemhealthagentrequest getsohrequest-Methode (napsystemhealthagent. h)
description: Kann von SHAs, die zuvor vom NAPAgent zwischengespeichert wurden, verwendet werden.
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- Getsohrequest-Methode NAP
- Getsohrequest-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getsohrequest-Methode
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
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040934"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a>Inapsystemhealthagentrequest:: getsohrequest-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthagentrequest:: getsohrequest** -Methode kann von SHAs, die zuvor von NAPAgent zwischengespeichert wurden, verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohrequest* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf einen [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                            | Beschreibung                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Vorgang erfolgreich.<br/>                                        |
| <dl> <dt>**NAP \_ E \_ kein \_ zwischengespeichertes \_ SoH**</dt> </dl> | Der SoH wurde nicht gefunden. NAPAgent verfügt über keine zwischengespeicherte Kopie.<br/> |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl>        | Berechtigungs Fehler, Zugriff verweigert.<br/>                           |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>         | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/>     |



 

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

 

 





