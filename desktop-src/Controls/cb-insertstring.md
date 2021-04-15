---
title: CB_INSERTSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinations Felds ein. Im Gegensatz zur CB \_ AddString-Nachricht bewirkt die CB \_ InsertString-Nachricht nicht, dass eine Liste mit dem CBS- \_ Sortier Stil sortiert wird.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Windows-Steuerelemente für CB_INSERTSTRING Meldung
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476650"
---
# <a name="cb_insertstring-message"></a>CB \_ InsertString-Nachricht

Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinations Felds ein. Im Gegensatz zur [**CB \_ AddString**](cb-addstring.md) -Nachricht bewirkt die **CB \_ InsertString** -Nachricht nicht, dass eine Liste mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil sortiert wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Position, an der die Zeichenfolge eingefügt werden soll. Wenn dieser Parameter-1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die mit NULL endende Zeichenfolge, die eingefügt werden soll. Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird der Wert des *LPARAM* -Parameters anstelle der Zeichenfolge gespeichert, auf die er andernfalls verweisen würde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde. Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err. Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist dies CB \_ errspace.

Wenn das Kombinations Feld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge einfügen, die breiter als das Kombinations Feld ist, sollten Sie eine [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md) -Nachricht senden, um sicherzustellen, dass die horizontale Bild Lauf Leiste

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

[**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB- \_ dir**](cb-dir.md)
</dt> </dl>

 

