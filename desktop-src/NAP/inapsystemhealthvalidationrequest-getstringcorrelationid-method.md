---
title: INapSystemHealthValidationRequest GetStringCorrelationId-Methode (NapSystemHealthValidator.h)
description: Wird von System Health Validators (SHVs) verwendet, die diese Informationen protokollieren müssen.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- NAP-Methode "GetStringCorrelationId"
- GetStringCorrelationId-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP , GetStringCorrelationId-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5818ebd219dd38633da92a269e63d5641f393371cfa67b6910844523c37929ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939361"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a>INapSystemHealthValidationRequest::GetStringCorrelationId-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidationRequest::GetStringCorrelationId-Methode** wird von System Health Validators (SHVs) verwendet, die diese Informationen protokollieren müssen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*correlationId* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf eine eindeutige [**StringCorrelationId**](nap-type-constants.md) für den SoH-Austausch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Andere COM-spezifische Fehlercodes können ebenfalls zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





