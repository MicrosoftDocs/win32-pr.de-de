---
title: LB_INSERTSTRING-Nachricht (Winuser.h)
description: Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Im Gegensatz zur LB \_ ADDSTRING-Nachricht führt die LB \_ INSERTSTRING-Nachricht nicht dazu, dass eine Liste mit dem \_ LBS-SORT-Stil sortiert wird.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: dd47d08ef78c590ecb3b5900143b29bc49676b86d8facdcc91b05bb34c8f4aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085390"
---
# <a name="lb_insertstring-message"></a>LB \_ INSERTSTRING-Nachricht

Fügt eine Zeichenfolge oder Elementdaten in ein Listenfeld ein. Im Gegensatz zur [**LB \_ ADDSTRING-Nachricht**](lb-addstring.md) führt die **LB \_ INSERTSTRING-Nachricht** nicht dazu, dass eine Liste mit dem [**\_ LBS-SORT-Stil**](list-box-styles.md) sortiert wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der Position, an der die Zeichenfolge eingefügt werden soll. Wenn dieser Parameter -1 ist, wird die Zeichenfolge am Ende der Liste hinzugefügt.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die eingefügt werden soll. Wenn das Listenfeld einen vom Besitzer gezeichneten Stil hat, aber nicht den [**LBS \_ HASSTRINGS-Stil,**](list-box-styles.md) wird dieser Parameter als Elementdaten anstelle einer Zeichenfolge gespeichert. Sie können die [**LB \_ GETITEMDATA-**](lb-getitemdata.md) und [**LB \_ SETITEMDATA-Nachrichten**](lb-setitemdata.md) senden, um die Elementdaten abzurufen oder zu ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der Index der Position, an der die Zeichenfolge eingefügt wurde. Wenn ein Fehler auftritt, lautet der Rückgabewert LB \_ ERR. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolge vorhanden ist, lautet der Rückgabewert LB \_ ERRSPACE.

## <a name="remarks"></a>Hinweise

Die [**LB \_ INITSTORAGE-Nachricht**](lb-initstorage.md) beschleunigt die Initialisierung von Listenfeldern mit einer großen Anzahl von Elementen (mehr als 100). Die angegebene Arbeitsspeichermenge wird reserviert, sodass nachfolgende **LB \_ INSERTSTRING-Nachrichten** die kürzeste Zeit in Anspruch nehmen. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie überbewerten, wird der zusätzliche Arbeitsspeicher belegt. Wenn Sie dies nicht möchten, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Wenn das Listenfeld den [**WS \_ HSCROLL-Stil**](/windows/desktop/winmsg/window-styles) auf hat und Sie eine Zeichenfolge einfügen, die breiter als das Listenfeld ist, senden Sie eine [**LB \_ SETHORIZONTALEXTENT-Nachricht,**](lb-sethorizontalextent.md) um sicherzustellen, dass die horizontale Scrollleiste angezeigt wird.

Bei einer ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mit CP ACP in \_ Unicode. Dies kann Probleme verursachen. Beispielsweise werden romanische Zeichen mit Akzent in einem Nicht-Unicode-Listenfeld in japanischen Windows verschachtelt angezeigt. Kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld, um dieses Problem zu beheben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

