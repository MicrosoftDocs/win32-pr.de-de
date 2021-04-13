---
title: EM_SETEVENTMASK Meldung (RichEdit. h)
description: Legt die Ereignis Maske für ein Rich-Edit-Steuerelement fest. Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Windows-Steuerelemente für EM_SETEVENTMASK Meldung
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478567"
---
# <a name="em_seteventmask-message"></a>EM- \_ Nachricht

Legt die Ereignis Maske für ein Rich-Edit-Steuerelement fest. Die Ereignis Maske gibt an, welche Benachrichtigungs Codes das Steuerelement an das übergeordnete Fenster sendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue Ereignis Maske für das Rich Edit-Steuerelement. Eine Liste der Ereignis Masken finden Sie unter [**Rich Edit Control Event Mask Flags**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die vorherige Ereignis Maske zurück.

## <a name="remarks"></a>Bemerkungen

Die Standard Ereignis Maske (bevor Any festgelegt ist) ist "ENM \_ None".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ GetEventMask**](em-geteventmask.md)
</dt> <dt>

[**Rich-Flags für Bearbeitungs Steuerelemente-Ereignis Maske**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





