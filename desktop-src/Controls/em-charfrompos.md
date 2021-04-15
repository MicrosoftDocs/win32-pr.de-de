---
title: EM_CHARFROMPOS Meldung (Winuser. h)
description: Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Client Bereich eines Bearbeitungs Steuer Elements am nächsten liegt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Windows-Steuerelemente für EM_CHARFROMPOS Meldung
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477607"
---
# <a name="em_charfrompos-message"></a>EM \_ charfrompos-Meldung

Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Client Bereich eines Bearbeitungs Steuer Elements am nächsten liegt. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Koordinaten eines Punkts im Client Bereich des Steuer Elements. Die Koordinaten befinden sich in Bildschirm Einheiten und sind relativ zur oberen linken Ecke des Client Bereichs des Steuer Elements.

**Rich Edit-Steuerelemente:** Ein Zeiger auf eine [**pointl**](/previous-versions//dd162807(v=vs.85)) -Struktur, die die horizontalen und vertikalen Koordinaten enthält.

Steuer **Elemente bearbeiten:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) enthält die horizontale Koordinate. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) enthält die vertikale Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Rich Edit-Steuerelemente:** Der Rückgabewert gibt den NULL basierten Zeichen Index des Zeichens an, das dem angegebenen Punkt am nächsten liegt. Der Rückgabewert gibt das letzte Zeichen im Bearbeitungs Steuerelement an, wenn der angegebene Punkt hinter dem letzten Zeichen im Steuerelement liegt.

Steuer **Elemente bearbeiten:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des Zeichens an, das dem angegebenen Punkt am nächsten liegt. Dieser Index ist relativ zum Anfang des Steuer Elements, nicht zum Anfang der Zeile. Wenn der angegebene Punkt hinter dem letzten Zeichen im Bearbeitungs Steuerelement liegt, gibt der Rückgabewert das letzte Zeichen im Steuerelement an. Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den NULL basierten Index der Zeile an, in der das Zeichen enthalten ist. Für einzeilige Bearbeitungs Steuerelemente ist dieser Wert 0 (null). Der Index gibt das Zeilen Trennzeichen an, wenn der angegebene Punkt hinter dem letzten sichtbaren Zeichen in einer Zeile liegt.

## <a name="remarks"></a>Bemerkungen

Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt. Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.

Wenn ein Punkt als *LPARAM* an **EM \_ charfrompos** und der Punkt außerhalb der Begrenzungen des Bearbeitungs Steuer Elements liegt, ist das *LRESULT* (65535, 65535).

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

[**EM \_ posfromchar**](em-posfromchar.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Makelparam**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**Pointl**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

