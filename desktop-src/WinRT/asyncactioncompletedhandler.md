---
description: Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Asyncactioncompletedhandler-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347181"
---
# <a name="asyncactioncompletedhandler-interface"></a>Asyncactioncompletedhandler-Schnittstelle

Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.

## <a name="members"></a>Member

Die **asyncactioncompletedhandler** -Schnittstelle erbt von [**iasyncinfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **Asyncactioncompletedhandler** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **asyncactioncompletedhandler** -Schnittstelle verfügt über diese Methoden.



| Methode                                               | BESCHREIBUNG                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Invoke**](asyncactioncompletedhandler-invoke.md) | Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Weisen Sie einer [**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) einen **asyncactioncompletedhandler** zu, um eine Benachrichtigung zu erhalten, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

