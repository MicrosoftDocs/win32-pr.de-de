---
title: EM_SETSEL Meldung (Winuser. h)
description: Wählt einen Bereich von Zeichen in einem Bearbeitungs Steuerelement aus. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Windows-Steuerelemente für EM_SETSEL Meldung
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476098"
---
# <a name="em_setsel-message"></a>EM-Aktivität \_ Nachricht

Wählt einen Bereich von Zeichen in einem Bearbeitungs Steuerelement aus. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anfangs Zeichenposition der Auswahl.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Position des Endzeichens der Auswahl.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Startwert kann größer als der Endwert sein. Der untere der beiden Werte gibt die Zeichenposition des ersten Zeichens in der Auswahl an. Der höhere Wert gibt die Position des ersten Zeichens außerhalb der Auswahl an.

Der Startwert ist der Ankerpunkt der Auswahl, und der Endwert ist das aktive Ende. Wenn der Benutzer die UMSCHALTTASTE verwendet, um die Größe der Auswahl anzupassen, kann das aktive Ende verschoben werden, der Ankerpunkt bleibt jedoch unverändert.

Wenn der Start Wert 0 und das Ende-1 ist, wird der gesamte Text im Bearbeitungs Steuerelement ausgewählt. Wenn der Start-1 ist, wird jede aktuelle Auswahl deaktiviert.

Steuer **Elemente bearbeiten:** Das-Steuerelement zeigt einen blinkenden Caretzeichen an der Endposition an, unabhängig von den relativen Werten von Start und Ende.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

Wenn das Bearbeitungs Steuerelement den [**es \_ nohidesel**](edit-control-styles.md) -Stil hat, wird der ausgewählte Text unabhängig davon hervorgehoben, ob das Steuerelement den Fokus besitzt. Ohne den **es \_ nohidesel** -Stil wird der ausgewählte Text nur hervorgehoben, wenn das Bearbeitungs Steuerelement den Fokus besitzt.

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

[**EM- \_ GetSEL**](em-getsel.md)
</dt> <dt>

[**EM \_ replacesel**](em-replacesel.md)
</dt> <dt>

[**EM \_ scrollcaret**](em-scrollcaret.md)
</dt> <dt>

[**EM- \_ Ex-tsel**](em-exsetsel.md)
</dt> </dl>

 

 





