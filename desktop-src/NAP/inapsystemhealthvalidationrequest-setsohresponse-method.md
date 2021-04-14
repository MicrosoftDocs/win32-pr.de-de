---
title: Inapsystemhealthvalidationrequest-setsohresponse-Methode (napsystemhealthvalidator. h)
description: Ermöglicht System Integritätsprüfungen (SHVs), die sohresponse festzulegen, die auf der Clientseite an Ihren System Integritäts-Agent (SHA)-Gegenstück gesendet wird.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Setsohresponse-Methode NAP
- Setsohresponse-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, setsohresponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392110"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>Inapsystemhealthvalidationrequest:: setsohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **inapsystemhealthvalidationrequest:: setsohresponse** -Methode können System Integritätsprüfungen (SHVs) die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festlegen, die auf der Clientseite an Ihr System Health Agent (SHA)-Gegenstück gesendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohresponse* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) -Struktur.

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





