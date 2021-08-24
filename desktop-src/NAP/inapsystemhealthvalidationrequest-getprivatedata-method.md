---
title: INapSystemHealthValidationRequest GetPrivateData-Methode (NapSystemHealthValidator.h)
description: Ermöglicht dem NapServer das Abrufen von Zustandsinformationen.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- GetPrivateData-Methode NAP
- GetPrivateData-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP, GetPrivateData-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ea94e3f03b3816cfb62f51263d5a5f9c67cf903b7e24991fa7a0f5d06427a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780760"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a>INapSystemHealthValidationRequest::GetPrivateData-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthValidationRequest::GetPrivateData-Methode** ermöglicht dem NapServer das Abrufen von Zustandsinformationen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*privateData* \[ out\]
</dt> <dd>

Ein Zeiger auf einen [](/windows/win32/api/naptypes/ns-naptypes-privatedata) Zeiger auf ein nicht transparentes PrivateData-Datenblob, das Zustandsinformationen enthält.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





