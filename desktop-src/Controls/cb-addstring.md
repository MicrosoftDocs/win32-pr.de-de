---
title: CB_ADDSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge in das Listenfeld eines Kombinations Felds ein. Wenn das Kombinations Feld nicht den CBS- \_ Sortier Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Windows-Steuerelemente für CB_ADDSTRING Meldung
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957009"
---
# <a name="cb_addstring-message"></a>CB- \_ AddString-Nachricht

Fügt eine Zeichenfolge in das Listenfeld eines Kombinations Felds ein. Wenn das Kombinations Feld nicht den CBS- [**\_ Sortier**](combo-box-styles.md) Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **LPCTSTR** -Zeiger auf die NULL-terminierte Zeichenfolge, die hinzugefügt werden soll. Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird der Wert des *LPARAM* -Parameters als Elementdaten gespeichert und nicht als die Zeichenfolge, auf die er andernfalls verweisen würde. Die Elementdaten können abgerufen oder geändert werden, indem die [**CB \_ GetItemData**](cb-getitemdata.md) - [**oder \_ CB**](cb-setitemdata.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index der Zeichenfolge im Listenfeld des Kombinations Felds. Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolge verfügbar ist, ist dies CB \_ errspace.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein vom Besitzer gezeichnetes Kombinations Feld mit dem [**CBS- \_ Sortier**](combo-box-styles.md) Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, wird die [**WM \_ compareitem**](wm-compareitem.md) -Nachricht einmal oder mehrmals an den Besitzer des Kombinations Felds gesendet, damit das neue Element ordnungsgemäß in die Liste eingefügt werden kann.

Um eine Zeichenfolge an einer bestimmten Position in der Liste einzufügen, verwenden Sie die [**CB \_ InsertString**](cb-insertstring.md) -Nachricht.

Wenn das Kombinations Feld über den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil verfügt und Sie eine Zeichenfolge hinzufügen, die größer als das Kombinations Feld ist, senden Sie eine [**lb- \_ sethorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale

**Comclt32.dll Version 5,0 oder höher:** Wenn " [**CBS \_ lowercase**](combo-box-styles.md) " oder " [**CBS \_ UpperCase**](combo-box-styles.md) " festgelegt ist, ändert die Unicode-Version von **CB \_ AddString** die Zeichenfolge. Bei Verwendung des schreibgeschützten globalen Speichers bewirkt dies, dass die Anwendung fehlschlägt.

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

[**CB- \_ dir**](cb-dir.md)
</dt> <dt>

[**CB \_ InsertString**](cb-insertstring.md)
</dt> <dt>

[**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM- \_ compareitem**](wm-compareitem.md)
</dt> </dl>

 

