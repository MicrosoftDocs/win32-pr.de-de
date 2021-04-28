---
title: EM_SETLIMITTEXT (Winuser.h)
description: 'EM_SETLIMITTEXT Meldung: Legt die Textgrenze eines Bearbeitungssteuerfelds fest.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109748"
---
# <a name="em_setlimittext-message"></a>EM \_ SETLIMITTEXT-Nachricht

Legt die Textgrenze eines Bearbeitungssteuerfelds fest. Die Textgrenze ist die maximale Textmenge in **TCHAR** s, die der Benutzer in das Bearbeitungssteuerfeld eingeben kann. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

Für Bearbeitungssteuerelemente und Microsoft Rich Edit 1.0 werden Bytes verwendet. Für Microsoft Rich Edit 2.0 und höher werden Zeichen verwendet.

Die **EM \_ SETLIMITTEXT-Nachricht** ist mit der [**EM \_ LIMITTEXT-Nachricht**](em-limittext.md) identisch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl von **TCHAR-S,** die der Benutzer eingeben kann. Für ANSI-Text ist dies die Anzahl von Bytes. für Unicode-Text ist dies die Anzahl von Zeichen. Diese Zahl schließt das beendende NULL-Zeichen nicht ein.

**Umfangreiche Bearbeitungssteuerelemente:** Wenn dieser Parameter null ist, wird die Textlänge auf 64.000 Zeichen festgelegt.

Wenn dieser Parameter null ist, wird die Textlänge auf 0x7FFFFFFE Zeichen für einzeilenbasierte Bearbeitungssteuerelemente oder 1 für mehrzeilenbasierte Bearbeitungssteuerelemente festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **EM \_ SETLIMITTEXT-Meldung** schränkt nur den Text ein, den der Benutzer eingeben kann. Sie wirkt sich weder auf Text aus, der bereits im Bearbeitungssteuerfeld enthalten ist, wenn die Nachricht gesendet wird, noch auf die Länge des Texts, der von der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) in das Bearbeitungssteuerfeld kopiert wird. Wenn eine Anwendung die **WM \_ SETTEXT-Nachricht** verwendet, um mehr Text in ein Bearbeitungssteuerfeld zu platzieren, als in der **EM \_ SETLIMITTEXT-Nachricht** angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungssteuerfelds bearbeiten.

Bevor **EM \_ SETLIMITTEXT** aufgerufen wird, beträgt der Standardgrenzwert für die Textmenge, die ein Benutzer in ein Bearbeitungssteuerfeld eingeben kann, 32.767 Zeichen.

Bei einzeiligen Bearbeitungssteuerelementen ist der Textgrenzwert entweder 0x7FFFFFFE Bytes oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist. Bei mehrzeiligen Bearbeitungssteuerelementen beträgt dieser Wert entweder 1 Byte oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Verwenden Sie die Meldung [**EM \_ EXLIMITTEXT**](em-exlimittext.md) für Textlängenwerte, die größer als 64.000 sind. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ GETLIMITTEXT**](em-getlimittext.md)
</dt> </dl>

 

