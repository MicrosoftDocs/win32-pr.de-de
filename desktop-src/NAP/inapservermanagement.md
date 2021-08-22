---
title: INapServerManagement-Schnittstelle (NapServerManagement.h)
description: Werden zum Verwalten des NAP-Servers verwendet.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- INapServerManagement-Schnittstelle NAP
- INapServerManagement-Schnittstelle NAP , beschrieben
topic_type:
- apiref
api_name:
- INapServerManagement
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b324f32c542a6a300266d26ceb5981bb6e14d0feff28aa225698d6b32bbe94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012528"
---
# <a name="inapservermanagement-interface"></a>INapServerManagement-Schnittstelle

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

**INapServerManagement** stellt Methoden bereit, die zum Verwalten des NAP-Servers verwendet werden.

## <a name="members"></a>Member

Die **INapServerManagement-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapServerManagement** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **INapServerManagement-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                                                                       | Beschreibung                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**INapServerManagement::RegisterSystemHealthValidator**](inapservermanagement-registersystemhealthvalidator-method.md)     | Registriert eine SHV.<br/>                         |
| [**INapServerManagement::SetFailureCategoryMappings**](inapservermanagement-setfailurecategorymappings-method.md)           | Legt die Fehlerkategoriezuordnungen der SHV fest.<br/> |
| [**INapServerManagement::UnregisterSystemHealthValidator**](inapservermanagement-unregistersystemhealthvalidator-method.md) | Lädt die Registrierung einer SHV beim NAP-Server zurück.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

