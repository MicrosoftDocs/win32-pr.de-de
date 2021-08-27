---
title: EM_SETWORDBREAKPROC-Nachricht (Winuser.h)
description: Ersetzt die Standardmäßige Wordwrap-Funktion eines Bearbeitungssteuerelements durch eine anwendungsdefinierte Wordwrap-Funktion. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- EM_SETWORDBREAKPROC Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90617545fab7c8c5cf75babd98e9d6ef85c5713778c52a6a00966a131d0a0581
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048020"
---
# <a name="em_setwordbreakproc-message"></a>EM \_ SETWORDBREAKPROC-Meldung

Ersetzt die Standardmäßige Wordwrap-Funktion eines Bearbeitungssteuerelements durch eine anwendungsdefinierte Wordwrap-Funktion. Sie können diese Nachricht entweder an ein Bearbeitungssteuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Adresse der anwendungsdefiniert Wordwrap-Funktion. Weitere Informationen zu Breaking Lines finden Sie in der Beschreibung der [*Rückruffunktion EditWordBreakProc.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Wordwrap-Funktion scannt einen Textpuffer, der Text enthält, der an den Bildschirm gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Bildschirmzeile passt. Die Wordwrap-Funktion platziert dieses Wort am Anfang der nächsten Zeile auf dem Bildschirm.

Eine Wordwrap-Funktion definiert den Punkt, an dem das System eine Textzeile für mehrzeilige Bearbeitungssteuerelemente unterbrechen soll, in der Regel an einem Leerzeichen, das zwei Wörter trennt. Ein mehrzeiliges oder ein einzeiliges Bearbeitungssteuerelement kann diese Funktion aufrufen, wenn der Benutzer die Pfeiltasten in Kombination mit der STRG-TASTE drückt, um das Caretzeichen zum nächsten oder vorherigen Wort zu verschieben. Die Wordwrap-Standardfunktion unterbricht eine Textzeile an einem Leerzeichen. Die anwendungsdefinierte Funktion kann den Wordwrap definieren, der an einem Bindestrich oder einem anderen Zeichen als dem Leerzeichen auftreten soll.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ GETWORDBREAKPROC**](em-getwordbreakproc.md)
</dt> </dl>

 

