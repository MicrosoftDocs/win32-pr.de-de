---
title: INapSystemHealthValidationRequest GetSoHResponse-Methode (NapSystemHealthValidator.h)
description: Ruft die SoHResponse ab.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- GetSoHResponse-Methode NAP
- GetSoHResponse-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP , GetSoHResponse-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da93f53f3dcc9f4e566703d4d2f63415bb7feb9b0c00d5086fe598ab442e1d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799057"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>INapSystemHealthValidationRequest::GetSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidationRequest::GetSoHResponse-Methode** ruft die [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf den empfangenen [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

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

 

 





