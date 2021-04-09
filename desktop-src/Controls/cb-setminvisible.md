---
title: CB_SETMINVISIBLE Meldung (kommstrg. h)
description: Eine Anwendung sendet eine CB \_ setminvisible-Nachricht, um die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds festzulegen.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Windows-Steuerelemente für CB_SETMINVISIBLE Meldung
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
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102986"
---
# <a name="cb_setminvisible-message"></a>CB- \_ setminvisible-Nachricht

Eine Anwendung sendet eine **CB \_ setminvisible** -Nachricht, um die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Mindestanzahl von sichtbaren Elementen an.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**". Andernfalls ist der Rückgabewert **false**.

## <a name="remarks"></a>Bemerkungen

Wenn die Anzahl der Elemente in der Dropdown Liste den minimalen Wert überschreitet, verwendet das Kombinations Feld eine Schiebe Leiste. Standardmäßig ist 30 die Mindestanzahl sichtbarer Elemente.

Diese Meldung wird ignoriert, wenn das Kombinations Feld-Steuerelement den Stil [**CBS \_ nointegralheight**](combo-box-styles.md)hat.

Um **CB \_ setminvisible** verwenden zu können, muss die Anwendung comctl32.dll Version 6 im Manifest angeben. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB \_ getminvisible**](cb-getminvisible.md)
</dt> <dt>

[**ComboBox \_ setminvisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





