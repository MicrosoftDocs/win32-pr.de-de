---
title: EM_GETMODIFY Meldung (Winuser. h)
description: Ruft den Zustand des änderungsflags eines Bearbeitungs Steuer Elements ab. Das Flag gibt an, ob der Inhalt des Bearbeitungs Steuer Elements geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 4229e2f2-3493-4721-8b52-8933c9dc0a77
keywords:
- Windows-Steuerelemente für EM_GETMODIFY Meldung
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
ms.openlocfilehash: 4f8c525df061717255051c49abaa3bda88f317b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858710"
---
# <a name="em_getmodify-message"></a>EM \_ getmodify-Nachricht

Ruft den Zustand des änderungsflags eines Bearbeitungs Steuer Elements ab. Das Flag gibt an, ob der Inhalt des Bearbeitungs Steuer Elements geändert wurde. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Wenn der Inhalt des Bearbeitungs Steuer Elements geändert wurde, ist der Rückgabewert ungleich 0 (null). Andernfalls ist der Wert 0 (null).

## <a name="remarks"></a>Bemerkungen

Wenn das Steuerelement erstellt wird, löscht das System das Änderungsflag automatisch auf 0 (null). Wenn der Benutzer den Text des Steuer Elements ändert, legt das System das Flag auf einen Wert ungleich 0 (null) fest. Sie können die Nachricht [**EM \_ setmodify**](em-setmodify.md) an das Bearbeitungs Steuerelement senden, um das Flag festzulegen oder zu löschen.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ setmodify**](em-setmodify.md)
</dt> </dl>

 

 





