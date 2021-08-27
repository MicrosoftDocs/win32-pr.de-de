---
title: CB_SETMINVISIBLE (Commctrl.h)
description: Eine Anwendung sendet eine CB SETMINVISIBLE-Nachricht, um die Mindestanzahl von sichtbaren Elementen in der \_ Dropdownliste eines Kombinationsfelds festlegen.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- CB_SETMINVISIBLE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063320"
---
# <a name="cb_setminvisible-message"></a>CB \_ SETMINVISIBLE-Nachricht

Eine Anwendung sendet eine **CB \_ SETMINVISIBLE-Nachricht,** um die Mindestanzahl von sichtbaren Elementen in der Dropdownliste eines Kombinationsfelds zu festlegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Mindestanzahl sichtbarer Elemente an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert **TRUE.** Andernfalls ist der Rückgabewert **FALSE.**

## <a name="remarks"></a>Hinweise

Wenn die Anzahl der Elemente in der Dropdownliste größer als das Minimum ist, verwendet das Kombinationsfeld eine Bildlaufleiste. Standardmäßig ist 30 die Mindestanzahl der sichtbaren Elemente.

Diese Meldung wird ignoriert, wenn das Kombinationsfeld-Steuerelement den Stil [**CBS \_ NOINTEGRALHEIGHT auf hat.**](combo-box-styles.md)

Um **CB \_ SETMINVISIBLE verwenden zu** können, muss die Anwendung comctl32.dll 6 im Manifest angeben. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ GETMINVISIBLE**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ SetMinVisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





