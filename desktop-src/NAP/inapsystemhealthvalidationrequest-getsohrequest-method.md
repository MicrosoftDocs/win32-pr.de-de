---
title: INapSystemHealthValidationRequest GetSoHRequest-Methode (NapSystemHealthValidator.h)
description: Ermöglicht es SYSTEM HEALTH Validators (SHVs), die soHRequest-Informationen abzurufen und zu überprüfen, die von ihren SHA-Entsprechungen (System Health Agent) auf dem Client gesendet werden.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- GetSoHRequest-Methode NAP
- GetSoHRequest-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP , GetSoHRequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9d9dc3b28aec92b7125dc2cad6bf8b843975945ca89687957d56be0ff562d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367728"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a>INapSystemHealthValidationRequest::GetSoHRequest-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **INapSystemHealthValidationRequest::GetSoHRequest-Methode** können System health Validators (SHVs) die [**SoHRequest-Informationen**](/windows/win32/api/naptypes/ns-naptypes-soh) abrufen und überprüfen, die von ihren SHA-Entsprechungen (System Health Agent) auf dem Client gesendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohRequest* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine [**SoHRequest-Struktur.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> <dt>

*napSystemGenerated* \[ out\]
</dt> <dd>

Eine **BOOL,** die **TRUE** ist, wenn der SoH vom NapAgent im Namen des SHA erstellt wurde, andernfalls **FALSE.** Sie wird hauptsächlich verwendet, um einen SHA-Fehler für die SHV anzugeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Der *parameter sohRequest* gibt möglicherweise **NULL** zurück, wenn der Client keine [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) an die SHV gesendet hat. In diesem Szenario kann die SHV eine **SoHResponse** mit dem Fehlercode NAP [**E MISSING \_ \_ \_ SOH**](nap-error-constants.md)auffüllen.

Wenn der *napSystemGenerated-Parameter* **TRUE** ist, lautet das Format von *SoHRequest* wie folgt:

-   [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id>
-   [**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)
-   [**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<sha-failure-error-code>**](nap-error-constants.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





