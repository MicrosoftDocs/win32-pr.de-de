---
title: EM_GETMODIFY Meldung (Winuser.h)
description: Ruft den Status des Änderungsflags eines Bearbeitungssteuerelements ab. Das Flag gibt an, ob der Inhalt des Bearbeitungssteuerelements geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- EM_GETMODIFY Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETMODIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34156e363824e975af68449b40ed639eeeb7e3ab76bd680b9837f3d3dd907537
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048900"
---
# <a name="em_getmodify-message"></a>EM \_ GETMODIFY-Nachricht

Ruft den Status des Änderungsflags eines Bearbeitungssteuerelements ab. Das Flag gibt an, ob der Inhalt des Bearbeitungssteuerelements geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Inhalt des Bearbeitungssteuerelements geändert wurde, ist der Rückgabewert ungleich 0 (null). Andernfalls ist es 0 (null).

## <a name="remarks"></a>Hinweise

Das System löscht das Änderungsflag automatisch auf 0 (null), wenn das Steuerelement erstellt wird. Wenn der Benutzer den Text des Steuerelements ändert, legt das System das Flag auf ungleich null fest. Sie können die [**EM \_ SETMODIFY-Nachricht**](em-setmodify.md) an das Bearbeitungssteuerelement senden, um das Flag festzulegen oder zu löschen.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ SETMODIFY**](em-setmodify.md)
</dt> </dl>

 

 





