---
title: EM_SETPASSWORDCHAR Meldung (Winuser. h)
description: Legt das Kenn Wort Zeichen für ein Bearbeitungs Steuerelement fest oder entfernt dieses. Wenn ein Kenn Wort Zeichen festgelegt ist, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 9091892c-9f37-4e06-a084-9326c5f7f31e
keywords:
- Windows-Steuerelemente für EM_SETPASSWORDCHAR Meldung
topic_type:
- apiref
api_name:
- EM_SETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd2c75039a6d447809cc17e5c44d70c6e612ede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476335"
---
# <a name="em_setpasswordchar-message"></a>EM \_ setpasswordchar-Meldung

Legt das Kenn Wort Zeichen für ein Bearbeitungs Steuerelement fest oder entfernt dieses. Wenn ein Kenn Wort Zeichen festgelegt ist, wird dieses Zeichen anstelle der vom Benutzer eingegebenen Zeichen angezeigt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Das Zeichen, das anstelle der vom Benutzer eingegebenen Zeichen angezeigt werden soll. Wenn dieser Parameter NULL ist, entfernt das Steuerelement das aktuelle Kenn Wort Zeichen und zeigt die vom Benutzer eingegebenen Zeichen an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Bearbeitungs Steuerelement die **EM \_ setpasswordchar** -Nachricht empfängt, zeichnet das Steuerelement alle sichtbaren Zeichen mithilfe des vom *wParam* -Parameter angegebenen Zeichens neu. Wenn *wParam* gleich 0 (null) ist, zeichnet das Steuerelement alle sichtbaren Zeichen mithilfe der Zeichen, die vom Benutzer eingegeben werden.

Wenn ein Bearbeitungs Steuerelement mit dem es-Kenn [**\_ Wort**](edit-control-styles.md) Stil erstellt wird, wird das standardmäßige Kenn Wort Zeichen auf ein Sternchen () festgelegt \* . Wenn ein Bearbeitungs Steuerelement ohne den es-Kenn **\_ Wort** Stil erstellt wird, gibt es kein Kenn Wort Zeichen. Der **es \_** -Kenn Wort Stil wird entfernt, wenn eine **EM \_ setpasswordchar** -Nachricht mit dem *wParam* -Parameter auf 0 (null) festgelegt wird.

Steuer **Elemente bearbeiten:** Mehrzeilige Bearbeitungs Steuerelemente unterstützen das Kenn Wort Format oder die Nachrichten nicht.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 2,0 und höher unterstützt. Sowohl einzeilige als auch mehrzeilige Bearbeitungs Steuerelemente unterstützen den Kenn Wort Stil und die Nachrichten. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getpasswordchar**](em-getpasswordchar.md)
</dt> </dl>

 

 





