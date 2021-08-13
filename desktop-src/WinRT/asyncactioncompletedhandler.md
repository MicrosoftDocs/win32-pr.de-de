---
description: Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: AsyncActionCompletedHandler-Schnittstelle
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
ms.openlocfilehash: 5d7e091ab250dc8b7475dbf17a1d1502cd1c4aa110106584c8c8b190c927f4aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561175"
---
# <a name="asyncactioncompletedhandler-interface"></a>AsyncActionCompletedHandler-Schnittstelle

Stellt die Methode dar, die aufgerufen wird, wenn eine asynchrone Aktion abgeschlossen ist.

## <a name="members"></a>Member

Die **AsyncActionCompletedHandler-Schnittstelle** erbt von [**IAsyncInfo.**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) **AsyncActionCompletedHandler** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **AsyncActionCompletedHandler-Schnittstelle** verfügt über diese Methoden.



| Methode                                               | Beschreibung                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Invoke**](asyncactioncompletedhandler-invoke.md) | Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Weisen Sie einer [**IAsyncActionAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) einen **AsyncActionCompletedHandler** zu, um eine Benachrichtigung zu erhalten, wenn die asynchrone Aktion abgeschlossen ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                    |
| Header<br/>                   | <dl> <dt>Windows. Foundation.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

