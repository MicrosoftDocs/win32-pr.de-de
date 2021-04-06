---
title: Inapsystemhealthvalidationrequest-Schnittstelle (napsystemhealthvalidator. h)
description: Werden zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet, die vom Anwendungsentwickler definiert werden.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- Inapsystemhealthvalidationrequest-Schnittstelle NAP
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743536"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>Inapsystemhealthvalidationrequest-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapsystemhealthvalidationrequest** -Schnittstelle stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **inapsystemhealthvalidationrequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsystemhealthvalidationrequest** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsystemhealthvalidationrequest** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                               | BESCHREIBUNG                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Inapsystemhealthvalidationrequest:: getcorrelationid**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | Wird von Validierungs Steuerelemente verwendet, um die Korrelations-ID abzurufen. Das Validierungs Steuerelement muss diese Informationen dann protokollieren.<br/>           |
| [**Inapsystemhealthvalidationrequest:: GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | Wird von Validierungs Steuerelemente verwendet, um den Computernamen abzurufen. Das Validierungs Steuerelement muss diese Informationen dann protokollieren.<br/>             |
| [**Inapsystemhealthvalidationrequest:: getprivatedata**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | Ermöglicht dem napserver das Abrufen von Zustandsinformationen.<br/>                                                        |
| [**Inapsystemhealthvalidationrequest:: getsohrequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | Ermöglicht Validierungs Steuerelementen das Abrufen und Validieren der sohrequest-Informationen.<br/>                                     |
| [**Inapsystemhealthvalidationrequest:: getsohresponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | Ruft das sohresponse-Objekt ab.<br/>                                                                               |
| [**Inapsystemhealthvalidationrequest:: getstringcorrelationid**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | Wird von Validierungs Steuerelemente zum Abrufen eines eindeutigen Exchange-Bezeichners verwendet. Das Validierungs Steuerelement muss diese Informationen dann protokollieren.<br/> |
| [**Inapsystemhealthvalidationrequest:: setprivatedata**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | Ermöglicht dem napserver das Speichern von Zustandsinformationen.<br/>                                                           |
| [**Inapsystemhealthvalidationrequest:: setsohresponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | Ermöglicht Validierungs Steuerelementen das Festlegen der sohresponse.<br/>                                                                  |



 

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

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

