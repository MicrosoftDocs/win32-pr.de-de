---
title: Inapservercallback-Schnittstelle (napsystemhealthvalidator. h)
description: SHVs verwenden, um den Abschluss einer asynchronen Anforderung zu signalisieren.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- Inapservercallback-Schnittstelle NAP
- Inapservercallback-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475267"
---
# <a name="inapservercallback-interface"></a>Inapservercallback-Schnittstelle

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der **inapservercallback** stellt eine Methode bereit, die SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.

## <a name="members"></a>Member

Die **inapservercallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Inapservercallback** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **inapservercallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**Inapservercallback:: OnComplete**](inapservercallback-oncomplete-method.md) | Wird von SHVs verwendet, um den Abschluss einer asynchronen Anforderung zu signalisieren.<br/> |



 

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

 

