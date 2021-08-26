---
title: CB_SETITEMDATA (Winuser.h)
description: Eine Anwendung sendet eine CB SETITEMDATA-Nachricht, um den Wert festzulegen, der dem angegebenen \_ Element in einem Kombinationsfeld zugeordnet ist.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA meldungssteuerelemente Windows
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
ms.openlocfilehash: 7abd50db9050178bc5d8d3b8ff556bce90f340fdb8d6692a514b0348aceeeab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089010"
---
# <a name="cb_setitemdata-message"></a>CB \_ SETITEMDATA-Nachricht

Eine Anwendung sendet eine **CB \_ SETITEMDATA-Nachricht,** um den Wert festzulegen, der dem angegebenen Element in einem Kombinationsfeld zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den nullbasierten Index des Elements an.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt den neuen Wert an, der dem Element zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ ERR.

## <a name="remarks"></a>Hinweise

Wenn sich das angegebene Element in einem vom Besitzer gezeichneten Kombinationsfeld befindet, das ohne den [**CBS \_ HASSTRINGS-Stil**](combo-box-styles.md) erstellt wurde, ersetzt diese Meldung den Wert im *lParam-Parameter* der [**CB \_ ADDSTRING-**](cb-addstring.md) oder [**CB \_ INSERTSTRING-Meldung,**](cb-insertstring.md) die das Element dem Kombinationsfeld hinzugefügt hat.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





