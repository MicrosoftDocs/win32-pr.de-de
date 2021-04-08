---
title: CB_GETITEMDATA Meldung (Winuser. h)
description: Eine Anwendung sendet eine CB \_ GetItemData-Nachricht an ein Kombinations Feld, um den von der Anwendung bereitgestellten Wert abzurufen, der mit dem angegebenen Element im Kombinations Feld verknüpft ist.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Windows-Steuerelemente für CB_GETITEMDATA Meldung
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741456"
---
# <a name="cb_getitemdata-message"></a>CB \_ GetItemData-Nachricht

Eine Anwendung sendet eine **CB \_ GetItemData** -Nachricht an ein Kombinations Feld, um den von der Anwendung bereitgestellten Wert abzurufen, der mit dem angegebenen Element im Kombinations Feld verknüpft ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index des Elements.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Wert, der dem Element zugeordnet ist. Wenn ein Fehler auftritt, ist es CB \_ Err.

Wenn sich das Element in einem von einem Besitzer gezeichneten Kombinations Feld befindet, das ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellt wurde, ist der Rückgabewert der Wert, der im *LPARAM* -Parameter der [**CB \_ AddString**](cb-addstring.md) -oder [**CB \_ InsertString**](cb-insertstring.md) -Nachricht enthalten ist, die das Element dem Kombinations Feld hinzugefügt hat. Wenn der **CBS \_ hasstrings** -Stil nicht verwendet wurde, ist der Rückgabewert der *LPARAM* -Parameter in einer [**CB \_ -Nachricht**](cb-setitemdata.md) .

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

[**CB \_ InsertString**](cb-insertstring.md)
</dt> <dt>

[**CB- \_ Daten**](cb-setitemdata.md)
</dt> </dl>

 

 





