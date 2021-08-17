---
title: EM_REPLACESEL-Nachricht (Winuser.h)
description: Ersetzt den ausgewählten Text in einem Bearbeitungssteuerelement oder einem Rich Edit-Steuerelement durch den angegebenen Text.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 478550432aa8c03a081e8de214cdd7e8337a46eca2676a0531b177a81ff20a54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831181"
---
# <a name="em_replacesel-message"></a>EM \_ REPLACESEL-Nachricht

Ersetzt den ausgewählten Text in einem Bearbeitungssteuerelement oder einem Rich Edit-Steuerelement durch den angegebenen Text.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, ob der Ersetzungsvorgang rückgängig sein kann. Wenn dies **TRUE** ist, kann der Vorgang rückgängig macht werden. Wenn dies **FALSE** ist, kann der Vorgang nicht rückgängig gemacht werden.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine auf NULL endende Zeichenfolge, die den Ersetzungstext enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **EM \_ REPLACESEL-Nachricht,** um nur einen Teil des Texts in einem Bearbeitungssteuerelement zu ersetzen. Um den gesamten Text zu ersetzen, verwenden Sie die [**WM \_ SETTEXT-Meldung.**](/windows/desktop/winmsg/wm-settext)

Wenn keine Auswahl vorhanden ist, wird der Ersatztext am Caretzeichen eingefügt.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

In einem Rich-Edit-Steuerelement übernimmt der Ersetzungstext die Formatierung des Zeichens am Caretzeichen oder , wenn eine Auswahl vorhanden ist, des ersten Zeichens in der Auswahl.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

