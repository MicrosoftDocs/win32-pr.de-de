---
title: CB_SETITEMDATA Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ SetItemData-Nachricht, um den Wert festzulegen, der mit dem angegebenen Element in einem Kombinations Feld verknüpft ist.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Windows-Steuerelemente für CB_SETITEMDATA Meldung
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859058"
---
# <a name="cb_setitemdata-message"></a>CB- \_ Nachricht

Eine Anwendung sendet eine **CB \_ SetItemData** -Nachricht, um den Wert festzulegen, der mit dem angegebenen Element in einem Kombinations Feld verknüpft ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den NULL basierten Index des Elements an.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den neuen Wert an, der dem Element zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Wenn sich das angegebene Element in einem vom Besitzer gezeichneten Kombinations Feld befindet, das ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellt wurde, ersetzt diese Meldung den Wert im *LPARAM* -Parameter der [**CB \_ AddString**](cb-addstring.md) -oder [**CB \_ InsertString**](cb-insertstring.md) -Nachricht, die das Element dem Kombinations Feld hinzugefügt hat.

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

[**CB \_ AddString**](cb-addstring.md)
</dt> <dt>

[**CB \_ GetItemData**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ InsertString**](cb-insertstring.md)
</dt> </dl>

 

 





