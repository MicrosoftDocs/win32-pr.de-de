---
title: CB_INSERTSTRING (Winuser.h)
description: Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinationsfelds ein. Im Gegensatz zur CB ADDSTRING-Nachricht führt die CB INSERTSTRING-Nachricht nicht dazu, dass eine Liste mit dem \_ \_ CBS \_ SORT-Format sortiert wird.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING meldungssteuerelemente Windows
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
ms.openlocfilehash: bcebd3ed5c52a40f3ca5d49031948f76edfa9d6d98974cec104c4b8e283c101a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089070"
---
# <a name="cb_insertstring-message"></a>CB \_ INSERTSTRING-Nachricht

Fügt eine Zeichenfolge oder Elementdaten in die Liste eines Kombinationsfelds ein. Im Gegensatz [**zur CB \_ ADDSTRING-Nachricht**](cb-addstring.md) führt **die CB \_ INSERTSTRING-Nachricht** nicht dazu, dass eine Liste mit dem [**CBS \_ SORT-Format**](combo-box-styles.md) sortiert wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der Position, an der die Zeichenfolge eingefügt werden soll. Wenn dieser Parameter -1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL terminierte Zeichenfolge, die eingefügt werden soll. Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ HASSTRINGS-Stil**](combo-box-styles.md) erstellen, wird der Wert des *lParam-Parameters* gespeichert und nicht die Zeichenfolge, auf die er andernfalls verweisen würde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde. Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ ERR. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolge verfügbar ist, ist dies CB \_ ERRSPACE.

Wenn das Kombinationsfeld [**das Format WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) aufgibt und Sie eine Zeichenfolge einfügen, die größer als das Kombinationsfeld ist, sollten Sie eine [**LB \_ SETHORIZONTALEXTENT-Meldung**](lb-sethorizontalextent.md) senden, um sicherzustellen, dass die horizontale Scrollleiste angezeigt wird.

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

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> </dl>

 

