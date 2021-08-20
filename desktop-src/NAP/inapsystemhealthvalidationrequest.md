---
title: INapSystemHealthValidationRequest-Schnittstelle (NapSystemHealthValidator.h)
description: Werden zur Unterstützung von Systemzustands-Validierungs-Validierungstools verwendet, die vom Anwendungsentwickler definiert werden.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest-Schnittstelle NAP
- INapSystemHealthValidationRequest-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7b6b2fdc0da8757ddd29b963445c0b984c45d19955c093270cf397fcac14b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133475"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>INapSystemHealthValidationRequest-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab dem Windows 10

 

Die **INapSystemHealthValidationRequest-Schnittstelle** stellt Methoden bereit, die zur Unterstützung von Systemzustandsvalidierungs-Validierungszeichen verwendet werden, die vom Anwendungsentwickler definiert werden.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthValidationRequest-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapSystemHealthValidationRequest** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthValidationRequest-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                               | Beschreibung                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Wird von Validierungsatoren verwendet, um die Korrelations-ID abzurufen. Das Validierungsgerät muss diese Informationen dann protokollieren.<br/>           |
| [**INapSystemHealthValidationRequest::GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Wird von Validierungsatoren zum Abrufen des Computernamens verwendet. Das Validierungsgerät muss diese Informationen dann protokollieren.<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Ermöglicht dem NapServer das Abrufen von Zustandsinformationen.<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Ermöglicht Validatoren das Abrufen und Überprüfen der SoHRequest-Informationen.<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Ruft das SoHResponse-Objekt ab.<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Wird von Validierungszeichen verwendet, um einen eindeutigen Austauschbezeichner abzurufen. Das Validierungsgerät muss diese Informationen dann protokollieren.<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Ermöglicht dem NapServer das Speichern von Zustandsinformationen.<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Ermöglicht Validierungsatoren das Festlegen von SoHResponse.<br/>                                                                  |



 

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

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

