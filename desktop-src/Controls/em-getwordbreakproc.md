---
title: EM_GETWORDBREAKPROC (Winuser.h)
description: Ruft die Adresse der aktuellen Wordwrap-Funktion ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- EM_GETWORDBREAKPROC meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f615721328ce0062d6bba9c282466744e7b47c78ad335b905343893f9c1b6343
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438060"
---
# <a name="em_getwordbreakproc-message"></a>EM \_ GETWORDBREAKPROC-Nachricht

Ruft die Adresse der aktuellen Wordwrap-Funktion ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

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

Der Rückgabewert gibt die Adresse der anwendungsdefinierten Wordwrap-Funktion an. Der Rückgabewert ist **NULL,** wenn keine Wordwrap-Funktion vorhanden ist.

## <a name="remarks"></a>Hinweise

Eine Wordwrap-Funktion scannt einen Textpuffer, der Text enthält, der an die Anzeige gesendet werden soll, und sucht nach dem ersten Wort, das nicht in die aktuelle Anzeigezeile passt. Die wordwrap-Funktion platziert dieses Wort am Anfang der nächsten Zeile in der Anzeige. Eine Wordwrap-Funktion definiert den Punkt, an dem das System eine Textzeile für Mehrzeilen-Bearbeitungssteuerelemente unterbricht, in der Regel an einem Leerzeichen, das zwei Wörter trennt.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[**EM \_ FMTLINES**](em-fmtlines.md)
</dt> <dt>

[**EM \_ SETWORDBREAKPROC**](em-setwordbreakproc.md)
</dt> </dl>

 

