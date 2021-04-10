---
title: Inapservermanagement-Schnittstelle (napservermanagement. h)
description: Wird verwendet, um den NAP-Server zu verwalten.
ms.assetid: 5c4f9bf1-fe82-48f5-8aa4-5c73ab01a78a
keywords:
- Inapservermanagement-Schnittstelle NAP
- Inapservermanagement-Schnittstelle NAP, beschrieben
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
ms.openlocfilehash: 5a5eed03f535653a3b9244ff1aa74fe499c1bf2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104145"
---
# <a name="inapservermanagement-interface"></a>Inapservermanagement-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **inapservermanagement** -Methode stellt Methoden bereit, die zum Verwalten des NAP-Servers verwendet werden.

## <a name="members"></a>Member

Die **inapservermanagement** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapservermanagement** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapservermanagement** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                                                       | BESCHREIBUNG                                          |
|:-----------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**Inapservermanagement:: registersystemhealthvalidator**](inapservermanagement-registersystemhealthvalidator-method.md)     | Registriert einen SHV.<br/>                         |
| [**Inapservermanagement:: setfailurecategorymappings**](inapservermanagement-setfailurecategorymappings-method.md)           | Legt die Zuordnungen der Fehler Kategorie des SHV fest.<br/> |
| [**Inapservermanagement:: unregistersystemhealthvalidator**](inapservermanagement-unregistersystemhealthvalidator-method.md) | Aufheben der Registrierung eines SHV vom NAP-Server.<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                               |
| Header<br/>                   | <dl> <dt>Napservermanagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napservermanagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Schnittstellen](nap-interfaces.md)
</dt> <dt>

[NAP-Referenz](nap-reference.md)
</dt> </dl>

 

