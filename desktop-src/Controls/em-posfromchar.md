---
title: EM_POSFROMCHAR Meldung (Winuser. h)
description: Ruft die Client Bereichs Koordinaten eines angegebenen Zeichens in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Windows-Steuerelemente für EM_POSFROMCHAR Meldung
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
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517981"
---
# <a name="em_posfromchar-message"></a>EM \_ posfromchar-Nachricht

Ruft die Client Bereichs Koordinaten eines angegebenen Zeichens in einem Bearbeitungs Steuerelement ab. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Umfassende **Bearbeitung 1,0 und 3,0:** Ein Zeiger auf eine [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur, die die Client Bereichs Koordinaten des Zeichens empfängt. Die Koordinaten befinden sich in Bildschirm Einheiten und sind relativ zur oberen linken Ecke des Client Bereichs des Steuer Elements.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Der null basierte Index des Zeichens.

</dd> <dt>

*lParam* 
</dt> <dd>

Umfassende **Bearbeitung 1,0 und 3,0:** Der null basierte Index des Zeichens.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Umfassende **Bearbeitung 1,0 und 3,0:** Der Rückgabewert wird nicht verwendet.

**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 2,0:** Der Rückgabewert enthält die Client Bereichs Koordinaten des Zeichens. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die horizontale Koordinate, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vertikale Koordinate.

## <a name="remarks"></a>Bemerkungen

Eine zurückgegebene Koordinate kann ein negativer Wert sein, wenn das angegebene Zeichen nicht im Client Bereich des Bearbeitungs Steuer Elements angezeigt wird. Die Koordinaten werden auf ganzzahlige Werte gekürzt.

Wenn das Zeichen ein Zeilen Trennzeichen ist, geben die zurückgegebenen Koordinaten einen Punkt direkt hinter dem letzten sichtbaren Zeichen in der Zeile an. Wenn der angegebene Index größer als der Index des letzten Zeichens im-Steuerelement ist, gibt das Steuerelement-1 zurück.

**Rich Edit 3,0 und höher:** Aus Gründen der Abwärtskompatibilität unterstützt Microsoft Rich Edit 3,0 die Syntax, die von Microsoft Rich Edit 2,0 verwendet wird. Wenn Microsoft Rich Edit 3,0 erkennt, dass *wParam* kein gültiger [**pointl**](/previous-versions//dd162807(v=vs.85)) -Zeiger ist, wird davon ausgegangen, dass die Nachricht mit der Microsoft Rich Edit 2,0-Syntax gesendet wurde. In diesem Fall wird der Rückgabewert verwendet, um die Koordinaten zurückzugeben.

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

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

[**EM \_ charfrompos**](em-charfrompos.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Pointl**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

