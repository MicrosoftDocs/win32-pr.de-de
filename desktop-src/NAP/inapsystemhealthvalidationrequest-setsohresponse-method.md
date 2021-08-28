---
title: INapSystemHealthValidationRequest SetSoHResponse-Methode (NapSystemHealthValidator.h)
description: Ermöglicht es SYSTEM HEALTH Validators (SHVs), die SoHResponse so festzulegen, dass sie an ihre SHA-Entsprechung (System Health Agent) auf clientseitiger Seite gesendet wird.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- SetSoHResponse-Methode NAP
- SetSoHResponse-Methode NAP, INapSystemHealthValidationRequest-Schnittstelle
- INapSystemHealthValidationRequest-Schnittstelle NAP, SetSoHResponse-Methode
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
ms.openlocfilehash: 2af44bc3c4801a35ad311f184f3aa2763ccc401ee01dce8a96ef65a0e2496219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939138"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a>INapSystemHealthValidationRequest::SetSoHResponse-Methode

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Mit der **INapSystemHealthValidationRequest::SetSoHResponse-Methode** können System health Validators (SHVs) festlegen, dass [**die SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) an ihre SHA-Entsprechung (System Health Agent) auf clientseitiger Seite gesendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohResponse* \[ In\]
</dt> <dd>

Ein Zeiger auf eine [**SoHResponse-Struktur.**](/windows/win32/api/naptypes/ns-naptypes-soh)

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

 

 





