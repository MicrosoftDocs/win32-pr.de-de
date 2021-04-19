---
title: Inapsystemhealthvalidationrequest getsohresponse-Methode (napsystemhealthvalidator. h)
description: Ruft die sohresponse ab.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Getsohresponse-Methode NAP
- Getsohresponse-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getsohresponse-Methode
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
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344714"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a>Inapsystemhealthvalidationrequest:: getsohresponse-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthvalidationrequest:: getsohresponse** -Methode ruft die [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sohresponse* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf einen Zeiger auf die empfangene [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh).

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

 

 





