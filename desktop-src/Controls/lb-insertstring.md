---
title: LB_INSERTSTRING Meldung (Winuser. h)
description: Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Anders als bei der LB \_ AddString-Nachricht bewirkt die LB- \_ InsertString-Nachricht nicht, dass eine Liste mit dem lbs- \_ Sortier Stil sortiert wird.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- Windows-Steuerelemente für LB_INSERTSTRING Meldung
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105543"
---
# <a name="lb_insertstring-message"></a>LB- \_ InsertString-Nachricht

Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Anders als bei der [**lb \_ AddString**](lb-addstring.md) -Nachricht bewirkt die **lb- \_ InsertString** -Nachricht nicht, dass eine Liste mit dem [**lbs- \_ Sortier**](list-box-styles.md) Stil sortiert wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Position, an der die Zeichenfolge eingefügt werden soll. Wenn dieser Parameter-1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die mit NULL endende Zeichenfolge, die eingefügt werden soll. Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, wird dieser Parameter nicht als Zeichenfolge, sondern als Elementdaten gespeichert. Sie können die [**lb- \_ GetItemData**](lb-getitemdata.md) -und [**lb- \_ ltitemdata**](lb-setitemdata.md) -Nachrichten senden, um die Elementdaten abzurufen oder zu ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde. Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err. Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist der Rückgabewert "lb \_ errspace".

## <a name="remarks"></a>Bemerkungen

Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen. Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ InsertString** -Nachrichten die kürzeste Zeit in Anspruch nehmen. Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden. Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Wenn das Listenfeld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge als das Listenfeld einfügen, senden Sie eine [**lb- \_ lthorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale Bild Lauf Leiste angezeigt wird.

Für eine ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in Unicode \_ . Dies kann zu Problemen führen. Beispielsweise werden Zeichen mit untergeordneten Zeichen in einem nicht-Unicode-Listenfeld in einem japanischen Fenster gegartet. Um dieses Problem zu beheben, kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld.

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

[**LB- \_ AddString**](lb-addstring.md)
</dt> <dt>

[**LB- \_ SelectString**](lb-selectstring.md)
</dt> <dt>

[**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md)
</dt> </dl>

 

