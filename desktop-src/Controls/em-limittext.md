---
title: EM_LIMITTEXT (Winuser.h)
description: 'EM_LIMITTEXT Meldung: Legt die Textgrenze eines Bearbeitungssteuerfelds fest.'
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109788"
---
# <a name="em_limittext-message"></a>EM \_ LIMITTEXT-Meldung

Legt die Textgrenze eines Bearbeitungssteuerfelds fest. Die Textgrenze ist die maximale Textmenge in **TCHAR** s, die der Benutzer in das Bearbeitungssteuerfeld eingeben kann. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

Für Bearbeitungssteuerelemente und Microsoft Rich Edit 1.0 werden Bytes verwendet. Für Microsoft Rich Edit 2.0 und höher werden Zeichen verwendet.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die maximale Anzahl von **TCHAR-S,** die der Benutzer eingeben kann. Für ANSI-Text ist dies die Anzahl von Bytes. für Unicode-Text ist dies die Anzahl von Zeichen. Diese Zahl schließt das beendende NULL-Zeichen nicht ein.

**Umfangreiche Bearbeitungssteuerelemente:** Wenn dieser Parameter null ist, wird die Textlänge auf 64.000 Zeichen festgelegt.

Wenn dieser Parameter 0 (null) ist, wird die Textlänge auf 0x7FFFFFFE Zeichen für einzeilenbasierte Bearbeitungssteuerelemente oder -1 für mehrzeilenbasierte Bearbeitungssteuerelemente festgelegt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **EM \_ LIMITTEXT-Meldung** schränkt nur den Text ein, den der Benutzer eingeben kann. Sie wirkt sich weder auf Text aus, der bereits im Bearbeitungssteuerfeld enthalten ist, wenn die Nachricht gesendet wird, noch auf die Länge des Texts, der von der [**WM \_ SETTEXT-Nachricht**](/windows/desktop/winmsg/wm-settext) in das Bearbeitungssteuerfeld kopiert wird. Wenn eine Anwendung die **WM \_ SETTEXT-Nachricht** verwendet, um mehr Text in ein Bearbeitungssteuerfeld zu platzieren, als in der **EM \_ LIMITTEXT-Meldung** angegeben ist, kann der Benutzer den gesamten Inhalt des Bearbeitungssteuerfelds bearbeiten.

Bevor **EM \_ LIMITTEXT** aufgerufen wird, beträgt der Standardgrenzwert für die Textmenge, die ein Benutzer in ein Bearbeitungssteuerfeld eingeben kann, 32.767 Zeichen.

Bei einzeilenbasierten Bearbeitungssteuerelementen beträgt der Textgrenzwert 0x7FFFFFFE Bytes oder den Wert des *wParam-Parameters,* je nach Kleinerem. Bei mehrzeiligen Bearbeitungssteuerelementen ist dieser Wert entweder -1 Byte oder der Wert des *wParam-Parameters,* je nachdem, welcher Wert kleiner ist.

**Rich Edit:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Verwenden Sie die Meldung [**EM \_ EXLIMITTEXT**](em-exlimittext.md) für Textlängenwerte, die größer als 64.000 sind. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (windows.h einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ EXLIMITTEXT**](em-exlimittext.md)
</dt> <dt>

[**Bearbeiten von \_ LimitText**](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

