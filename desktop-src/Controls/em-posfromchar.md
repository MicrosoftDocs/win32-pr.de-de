---
title: EM_POSFROMCHAR (Winuser.h)
description: Ruft die Clientbereichkoordinaten eines angegebenen Zeichens in einem Bearbeitungssteuerzeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1d9d2dccb6ccf1bd80b44b2221f8628f13e595ee514074956e7869447d513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437880"
---
# <a name="em_posfromchar-message"></a>EM \_ POSFROMCHAR-Nachricht

Ruft die Clientbereichkoordinaten eines angegebenen Zeichens in einem Bearbeitungssteuerzeichen ab. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 1.0 und 3.0:** Ein Zeiger auf eine [**POINTL-Struktur,**](/previous-versions//dd162807(v=vs.85)) die die Clientbereichkoordinaten des Zeichens empfängt. Die Koordinaten befinden sich in Bildschirmeinheiten und sind relativ zur oberen linken Ecke des Clientbereichs des Steuerelements.

**Steuerelemente bearbeiten und Rich Edit 2.0:** Der nullbasierte Index des Zeichens.

</dd> <dt>

*lParam* 
</dt> <dd>

**Rich Edit 1.0 und 3.0:** Der nullbasierte Index des Zeichens.

**Steuerelemente bearbeiten und Rich Edit 2.0:** Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Rich Edit 1.0 und 3.0:** Der Rückgabewert wird nicht verwendet.

**Steuerelemente bearbeiten und Rich Edit 2.0:** Der Rückgabewert enthält die Clientbereichkoordinaten des Zeichens. Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die horizontale Koordinate und [**das HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die vertikale Koordinate.

## <a name="remarks"></a>Hinweise

Eine zurückgegebene Koordinate kann ein negativer Wert sein, wenn das angegebene Zeichen nicht im Clientbereich des Bearbeitungssteuerzeichens angezeigt wird. Die Koordinaten werden auf ganzzahlige Werte gekürzt.

Wenn das Zeichen ein Zeilentrennzeichen ist, geben die zurückgegebenen Koordinaten einen Punkt direkt hinter dem letzten sichtbaren Zeichen in der Zeile an. Wenn der angegebene Index größer als der Index des letzten Zeichens im -Steuerelement ist, gibt das Steuerelement -1 zurück.

**Rich Edit 3.0 und höher:** Aus Gründen der Abwärtskompatibilität unterstützt Microsoft Rich Edit 3.0 die von Microsoft Rich Edit 2.0 verwendete Syntax. Wenn Microsoft Rich Edit 3.0 erkennt, dass *wParam* kein gültiger [**POINTL-Zeiger**](/previous-versions//dd162807(v=vs.85)) ist, wird davon ausgegangen, dass die Nachricht mit der Microsoft Rich Edit 2.0-Syntax gesendet wurde. In diesem Fall wird der Rückgabewert verwendet, um die Koordinaten zurück zu geben.

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

[**EM \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

