---
title: INapSystemHealthValidationRequest SetPrivateData-Methode (NapSystemHealthValidator.h)
description: Ermöglicht dem NapServer das Speichern von Zustandsinformationen.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- SetPrivateData-Methode NAP
- SetPrivateData-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP, SetPrivateData-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0e362eb3732d18c0e98b89f834dfe9efbc2a70ca82b7c211a96459d46a9f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037690"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a>INapSystemHealthValidationRequest::SetPrivateData-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthValidationRequest::SetPrivateData-Methode** ermöglicht dem NapServer das Speichern von Zustandsinformationen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*privateData* \[ In\]
</dt> <dd>

Ein Zeiger auf ein [**PrivateData-Datenblob,**](/windows/win32/api/naptypes/ns-naptypes-privatedata) das die nicht transparenten Zustandsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Es können auch andere COM-spezifische Fehlercodes zurückgegeben werden.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Vorgang erfolgreich.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Berechtigungsfehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Systemressourcenlimit, konnte den Vorgang nicht ausführen.<br/> |



 

## <a name="remarks"></a>Hinweise

Nur der NapServer kann das Datenblob interpretieren.

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

 

 





