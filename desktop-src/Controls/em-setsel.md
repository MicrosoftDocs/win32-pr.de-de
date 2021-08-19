---
title: EM_SETSEL (Winuser.h)
description: Wählt einen Bereich von Zeichen in einem Bearbeitungssteuerzeichen aus. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- EM_SETSEL von Windows-Steuerelementen
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
ms.openlocfilehash: 190d8a62b874d3449e0a9bf5d334a515000fb0436ba73753a8657936363071b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062890"
---
# <a name="em_setsel-message"></a>EM \_ SETSEL-Meldung

Wählt einen Bereich von Zeichen in einem Bearbeitungssteuerzeichen aus. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Anfangszeichenposition der Auswahl.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Endzeichenposition der Auswahl.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Startwert kann größer als der Endwert sein. Der untere der beiden Werte gibt die Zeichenposition des ersten Zeichens in der Auswahl an. Der höhere Wert gibt die Position des ersten Zeichens nach der Auswahl an.

Der Startwert ist der Ankerpunkt der Auswahl, und der Endwert ist das aktive Ende. Wenn der Benutzer die UMSCHALTTASTE verwendet, um die Größe der Auswahl anzupassen, kann sich das aktive Ende bewegen, aber der Ankerpunkt bleibt unverändert.

Wenn der Anfang 0 und das Ende -1 ist, wird der text im Bearbeitungssteuerfeld ausgewählt. Wenn der Start -1 ist, wird jede aktuelle Auswahl deaktiviert.

**Steuerelemente bearbeiten:** Das -Steuerelement zeigt unabhängig von den relativen Werten von Start und Ende ein blinkendes Caret-Caret-Steuerelement an der Endposition an.

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

Wenn das Bearbeitungssteuerfeld über das [**ES \_ NOHIDESEL-Format**](edit-control-styles.md) verfügt, wird der ausgewählte Text hervorgehoben, unabhängig davon, ob das Steuerelement den Fokus besitzt. Ohne den **ES \_ NOHIDESEL-Stil** wird der ausgewählte Text nur hervorgehoben, wenn das Bearbeitungssteuerfeld den Fokus besitzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETSEL**](em-getsel.md)
</dt> <dt>

[**EM \_ REPLACESEL**](em-replacesel.md)
</dt> <dt>

[**EM \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**EM \_ EXSETSEL**](em-exsetsel.md)
</dt> </dl>

 

 





