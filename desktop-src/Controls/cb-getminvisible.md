---
title: CB_GETMINVISIBLE Meldung (kommstrg. h)
description: Ruft die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds ab.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Windows-Steuerelemente für CB_GETMINVISIBLE Meldung
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858891"
---
# <a name="cb_getminvisible-message"></a>CB \_ getminvisible-Meldung

Ruft die Mindestanzahl sichtbarer Elemente in der Dropdown Liste eines Kombinations Felds ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Mindestanzahl sichtbarer Elemente.

## <a name="remarks"></a>Bemerkungen

Wenn die Anzahl der Elemente in der Dropdown Liste den minimalen Wert überschreitet, verwendet das Kombinations Feld eine Schiebe Leiste.

Diese Meldung wird ignoriert, wenn das Kombinations Feld-Steuerelement den Stil [**CBS \_ nointegralheight**](combo-box-styles.md)hat.

Um **CB \_ getminvisible** verwenden zu können, muss die Anwendung comctl32.dll Version 6 im Manifest angeben. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

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

[**CB \_ setminvisible**](cb-setminvisible.md)
</dt> <dt>

[**ComboBox \_ getminvisible**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





