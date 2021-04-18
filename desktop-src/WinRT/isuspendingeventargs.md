---
description: Stellt Daten für ein Ereignis zum Anhalten der APP bereit.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Isuspendingeventargs-Schnittstelle (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345725"
---
# <a name="isuspendingeventargs-interface"></a>Isuspendingeventargs-Schnittstelle

Stellt Daten für ein Ereignis zum Anhalten der APP bereit.

## <a name="members"></a>Member

Die **isuspendingeventargs** -Schnittstelle erbt von [**iinspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **Isuspendingeventargs** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **isuspendingeventargs** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                           | Zugriffstyp           | BESCHREIBUNG                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**Suspendingoperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Lesen/Schreiben<br/> | Ruft den Vorgang zum Anhalten der App ab.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Auf dieses Objekt wird zugegriffen, wenn Sie Ereignishandler wie [**suspendingeventhandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**suspendingeventhandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)implementieren und anhalten [**Hinzufügen \_**](/previous-versions//hh438376(v=vs.85)) , um auf App-anhalteereignisse zu reagieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Header<br/>                   | <dl> <dt>Windows. applicationmodel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. applicationmodel. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**Isuspendingoperation**](isuspendingoperation.md)
</dt> <dt>

[**Isuspendingdeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
