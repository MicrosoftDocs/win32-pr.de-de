---
title: EM_EMPTYUNDOBUFFER Meldung (Winuser. h)
description: Setzt das rückgängig-Flag eines Bearbeitungs Steuer Elements zurück. Das rückgängigflag wird festgelegt, wenn ein Vorgang innerhalb des Bearbeitungs Steuer Elements rückgängig gemacht werden kann. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a4ff7bd9-f8ae-4f18-8429-4ceaaeeb0f94
keywords:
- Windows-Steuerelemente für EM_EMPTYUNDOBUFFER Meldung
topic_type:
- apiref
api_name:
- EM_EMPTYUNDOBUFFER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abbdc067b603a032b8d311ddd7930a8ca6de01c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477604"
---
# <a name="em_emptyundobuffer-message"></a>Nachricht "em \_ emptyundobuffer"

Setzt das rückgängig-Flag eines Bearbeitungs Steuer Elements zurück. Das rückgängigflag wird festgelegt, wenn ein Vorgang innerhalb des Bearbeitungs Steuer Elements rückgängig gemacht werden kann. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

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

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das rückgängig-Flag wird automatisch zurückgesetzt, wenn das Bearbeitungs Steuerelement eine [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -oder [**EM \_ SetHandle**](em-sethandle.md) -Meldung empfängt.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 1,0:** Das Steuerelement kann nur den letzten Vorgang rückgängig machen oder wiederholen.

**Rich Edit 2,0 und höher:** Die Nachricht " **EM \_ emptyundobuffer** " Leert alle rückgängig-und Wiederholungs Puffer. Rich Edit-Steuerelemente ermöglichen dem Benutzer das Rückgängigmachen oder wiederholen mehrerer Vorgänge.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ CanUndo**](em-canundo.md)
</dt> <dt>

[**EM- \_ andle**](em-sethandle.md)
</dt> <dt>

[**EM \_ rückgängig machen**](em-undo.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

