---
title: Inapsystemhealthvalidator-Schnittstelle (napsystemhealthvalidator. h)
description: Muss von SHV-Entwicklern implementiert werden, damit das NAP-System mit einem SHV kommunizieren kann.
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- Inapsystemhealthvalidator-Schnittstelle NAP
- Inapsystemhealthvalidator Interface NAP, beschrieben
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce4d47555926c2a3ad5b06315521fea23503d66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740904"
---
# <a name="inapsystemhealthvalidator-interface"></a>Inapsystemhealthvalidator-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Das **inapsystemhealthvalidator** -Steuerelement stellt Methoden bereit, die von SHV-Entwicklern implementiert werden müssen, damit das NAP-System mit einem SHV kommunizieren kann.

## <a name="members"></a>Member

Die **inapsystemhealthvalidator** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapsystemhealthvalidator** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapsystemhealthvalidator** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inapsystemhealthvalidator:: Validate**](inapsystemhealthvalidator-validate-method.md) | Das NAP-System ruft diese Anwendungs definierte Methode auf, um die von einem Client empfangene [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) zu validieren. <br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                    |
| Header<br/>                   | <dl> <dt>Napsystemhealthvalidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napsystemhealthvalidator. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

