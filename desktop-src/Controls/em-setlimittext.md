---
title: EM_SETLIMITTEXT Meldung (Winuser. h)
description: Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Windows-Steuerelemente für EM_SETLIMITTEXT Meldung
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
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742008"
---
# <a name="em_setlimittext-message"></a>EM \_ SetLimitText-Nachricht

Legt den Text Grenzwert eines Bearbeitungs Steuer Elements fest. Das Text Limit ist die maximale Text Menge in **TCHAR** s, die der Benutzer in das Bearbeitungs Steuerelement eingeben kann. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

Für Bearbeitungs Steuerelemente und Microsoft Rich Edit 1,0 werden Bytes verwendet. Für Microsoft Rich Edit 2,0 und höher werden Zeichen verwendet.

Die **EM- \_ SetLimitText** -Nachricht ist mit der [**EM- \_ limittext**](em-limittext.md) Nachricht identisch.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl von **TCHAR**-s, die der Benutzer eingeben kann. Bei ANSI-Text ist dies die Anzahl der Bytes. bei Unicode-Text ist dies die Anzahl der Zeichen. Diese Zahl umfasst nicht das abschließende Null Zeichen.

**Rich Edit-Steuerelemente:** Wenn dieser Parameter 0 (null) ist, wird die Textlänge auf 64.000 Zeichen festgelegt.

Wenn dieser Parameter 0 (null) ist, wird die Textlänge für einzeilige Bearbeitungs Steuerelemente auf 0x7ffffffe-Zeichen oder für mehrzeilige Bearbeitungs Steuerelemente auf 1 festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die " **EM \_ SetLimitText** "-Nachricht schränkt nur den Text ein, den der Benutzer eingeben kann. Er wirkt sich nicht auf Text aus, der sich bereits im Bearbeitungs Steuerelement befindet, wenn die Nachricht gesendet wird, und wirkt sich nicht auf die Länge des Texts aus, der durch die [**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext) -Nachricht in das Bearbeitungs Steuerelement kopiert wird Wenn eine Anwendung die **WM- \_ SetText** -Nachricht verwendet, um mehr Text in ein Bearbeitungs Steuerelement zu platzieren, als in der **EM- \_ SetLimitText** -Meldung angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungs Steuer Elements bearbeiten.

Bevor **EM \_ SetLimitText** aufgerufen wird, ist der Standard Grenzwert für die Textmenge, die ein Benutzer in einem Bearbeitungs Steuerelement eingeben kann, 32.767 Zeichen.

Für einzeilige Bearbeitungs Steuerelemente ist das Text Limit entweder 0x7ffffffe Bytes oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist. Für mehrzeilige Bearbeitungs Steuerelemente ist dieser Wert entweder 1 Byte oder der Wert des *wParam* -Parameters, je nachdem, welcher Wert kleiner ist.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Verwenden Sie den [**\_ exlimittext**](em-exlimittext.md) der Nachricht EM für Textlängen Werte größer als 64.000. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getlimittext**](em-getlimittext.md)
</dt> </dl>

 

