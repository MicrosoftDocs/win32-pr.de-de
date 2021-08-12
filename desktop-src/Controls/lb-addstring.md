---
title: LB_ADDSTRING Meldung (Winuser.h)
description: Fügt einem Listenfeld eine Zeichenfolge hinzu. Wenn das Listenfeld nicht über den LBS \_ SORT-Stil verfügt, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671686"
---
# <a name="lb_addstring-message"></a>LB \_ ADDSTRING-Nachricht

Fügt einem Listenfeld eine Zeichenfolge hinzu. Wenn das Listenfeld nicht über den [**LBS \_ SORT-Stil**](list-box-styles.md) verfügt, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt, und die Liste wird sortiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL endende Zeichenfolge, die hinzugefügt werden soll.

Wenn das Listenfeld einen vom Besitzer gezeichneten Stil hat, aber nicht den [**LBS \_ HASSTRINGS-Stil,**](list-box-styles.md) wird dieser Parameter als Elementdaten anstelle einer Zeichenfolge gespeichert. Sie können die **LB \_ GETITEMDATA-** und **LB \_ SETITEMDATA-Nachrichten** senden, um die Elementdaten abzurufen oder zu ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der nullbasierte Index der Zeichenfolge im Listenfeld. Wenn ein Fehler auftritt, lautet der Rückgabewert LB \_ ERR. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolge vorhanden ist, lautet der Rückgabewert LB \_ ERRSPACE.

## <a name="remarks"></a>Hinweise

Wenn das Listenfeld einen vom Besitzer gezeichneten Stil und den [**LBS-SORT-Stil \_**](list-box-styles.md) aufwies, aber nicht den [**LBS \_ HASSTRINGS-Stil,**](list-box-styles.md) sendet das System die [**WM \_ COMPAREITEM-Nachricht**](wm-compareitem.md) ein oder mehrmals an den Besitzer des Listenfelds, um das neue Element ordnungsgemäß im Listenfeld zu platzieren.

Die [**LB \_ INITSTORAGE-Nachricht**](lb-initstorage.md) beschleunigt die Initialisierung von Listenfeldern mit einer großen Anzahl von Elementen (mehr als 100). Sie reserviert die angegebene Arbeitsspeichermenge, sodass nachfolgende **LB \_ ADDSTRING-Nachrichten** die kürzeste Zeit in Anspruch nehmen. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie überbewerten, wird der zusätzliche Arbeitsspeicher belegt. Wenn Sie dies nicht möchten, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Wenn das Listenfeld über den [**WS \_ HSCROLL-Stil**](/windows/desktop/winmsg/window-styles) verfügt und Sie eine Zeichenfolge hinzufügen, die breiter als das Listenfeld ist, senden Sie eine [**LB \_ SETHORIZONTALEXTENT-Nachricht,**](lb-sethorizontalextent.md) um sicherzustellen, dass die horizontale Scrollleiste angezeigt wird.

Bei einer ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mit CP ACP in \_ Unicode. Dies kann Probleme verursachen. Beispielsweise werden romanische Zeichen mit Akzent in einem Nicht-Unicode-Listenfeld in japanischen Windows garniert angezeigt. Kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld, um dieses Problem zu beheben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

