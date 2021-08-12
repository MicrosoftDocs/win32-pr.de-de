---
title: INapSystemHealthValidationRequest2-Schnittstelle (NapSystemHealthValidator.h)
description: Stellt Methoden bereit, die zur Unterstützung von Systemzustands-Validierungsprüfern verwendet werden, die vom Anwendungsentwickler definiert werden.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2-Schnittstelle NAP
- INapSystemHealthValidationRequest2-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6438394120ecd901c6de6d7a8ccac40f742d9f73d27a36682de894d9c5a7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620849"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>INapSystemHealthValidationRequest2-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidationRequest2-Schnittstelle** stellt Methoden bereit, die zur Unterstützung von Systemzustandsvalidierungsvalidatoren verwendet werden, die vom Anwendungsentwickler definiert werden.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthValidationRequest2-Schnittstelle** erbt von [**INapSystemHealthValidationRequest.**](inapsystemhealthvalidationrequest.md) **INapSystemHealthValidationRequest2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthValidationRequest2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                    | Beschreibung                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | Ruft die Konfigurations-ID in einer Validierungsanforderung ab.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn eine SHV [**INapComponentConfig3**](inapcomponentconfig3.md)nicht unterstützt, gilt diese Schnittstelle nicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





