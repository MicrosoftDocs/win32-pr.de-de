---
title: EM_CHARFROMPOS (Winuser.h)
description: Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Clientbereich eines Bearbeitungssteuerzeichens am nächsten liegt. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS meldungssteuerelemente Windows
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
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915960"
---
# <a name="em_charfrompos-message"></a>EM \_ CHARFROMPOS-Nachricht

Ruft Informationen über das Zeichen ab, das einem angegebenen Punkt im Clientbereich eines Bearbeitungssteuerzeichens am nächsten liegt. Sie können diese Nachricht entweder an ein Bearbeitungssteuer steuerelement oder an ein Rich Edit-Steuerelement senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Die Koordinaten eines Punkts im Clientbereich des Steuerelements. Die Koordinaten befinden sich in Bildschirmeinheiten und sind relativ zur oberen linken Ecke des Clientbereichs des Steuerelements.

**Umfangreiche Bearbeitungssteuerelemente:** Ein Zeiger auf eine [**POINTL-Struktur,**](/previous-versions//dd162807(v=vs.85)) die die horizontalen und vertikalen Koordinaten enthält.

**Steuerelemente bearbeiten:** Das [**LOWORD enthält**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) die horizontale Koordinate. Das [**HIWORD enthält**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) die vertikale Koordinate.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**Umfangreiche Bearbeitungssteuerelemente:** Der Rückgabewert gibt den nullbasierten Zeichenindex des Zeichens an, das dem angegebenen Punkt am nächsten liegt. Der Rückgabewert gibt das letzte Zeichen im Bearbeitungssteuerzeichen an, wenn der angegebene Punkt hinter dem letzten Zeichen im Steuerelement liegt.

**Steuerelemente bearbeiten:** Das [**LOWORD gibt**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) den nullbasierten Index des Zeichens an, das dem angegebenen Punkt am nächsten liegt. Dieser Index ist relativ zum Anfang des Steuerelements, nicht zum Anfang der Zeile. Wenn der angegebene Punkt außerhalb des letzten Zeichens im Bearbeitungssteuerzeichen liegt, gibt der Rückgabewert das letzte Zeichen im Steuerelement an. Das [**HIWORD gibt**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) den nullbasierten Index der Zeile an, die das Zeichen enthält. Bei einzeilenbasierten Bearbeitungssteuerelementen ist dieser Wert 0 (null). Der Index gibt das Zeilentrennzeichen an, wenn der angegebene Punkt hinter dem letzten sichtbaren Zeichen in einer Zeile liegt.

## <a name="remarks"></a>Hinweise

**Umfangreiche Bearbeitung:** Wird in Microsoft Rich Edit 1.0 und höher unterstützt. Informationen zur Kompatibilität von Rich Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter [Informationen zu Rich Edit-Steuerelementen.](about-rich-edit-controls.md)

Wenn ein Punkt als *lParam* an **EM \_ CHARFROMPOS** übergeben wird und der Punkt außerhalb der Grenzen des Bearbeitungssteuerpunkts liegt, ist *das lResult* (65535, 65535).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ POSFROMCHAR**](em-posfromchar.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

