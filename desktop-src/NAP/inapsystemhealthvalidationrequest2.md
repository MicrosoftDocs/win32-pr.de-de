---
title: INapSystemHealthValidationRequest2-Schnittstelle (napsystemhealthvalidator. h)
description: Stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2-Schnittstelle NAP
- INapSystemHealthValidationRequest2 Interface NAP, beschrieben
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
ms.openlocfilehash: 12fdbfc46578a4e64a92accc46f6b910a44dd946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342883"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>INapSystemHealthValidationRequest2-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **INapSystemHealthValidationRequest2** -Schnittstelle stellt Methoden bereit, die zur Unterstützung von Systemintegritäts-Validierungs Steuerelementen verwendet werden, die vom Anwendungsentwickler definiert werden.

> [!Note]  
> Diese Schnittstelle erbt alle Methoden von [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md) und sollte stattdessen verwendet werden.

 

## <a name="members"></a>Member

Die **INapSystemHealthValidationRequest2** -Schnittstelle erbt von [**inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md). **INapSystemHealthValidationRequest2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapSystemHealthValidationRequest2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                    | BESCHREIBUNG                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2:: getconfigid**](inapsystemhealthvalidationrequest2-getconfigid.md) | Ruft die Konfigurations-ID in einer Validierungs Anforderung ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein SHV [**INapComponentConfig3**](inapcomponentconfig3.md)nicht unterstützt, wird diese Schnittstelle nicht angewendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

 





