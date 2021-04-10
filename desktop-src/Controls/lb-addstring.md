---
title: LB_ADDSTRING Meldung (Winuser. h)
description: Fügt einem Listenfeld eine Zeichenfolge hinzu. Wenn das Listenfeld nicht den lbs- \_ Sortier Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt und die Liste sortiert.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Windows-Steuerelemente für LB_ADDSTRING Meldung
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
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040541"
---
# <a name="lb_addstring-message"></a>LB- \_ AddString-Nachricht

Fügt einem Listenfeld eine Zeichenfolge hinzu. Wenn das Listenfeld nicht den lbs- [**\_ Sortier**](list-box-styles.md) Stil hat, wird die Zeichenfolge am Ende der Liste hinzugefügt. Andernfalls wird die Zeichenfolge in die Liste eingefügt und die Liste sortiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die NULL-terminierte Zeichenfolge, die hinzugefügt werden soll.

Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, wird dieser Parameter nicht als Zeichenfolge, sondern als Elementdaten gespeichert. Sie können die **lb- \_ GetItemData** -und **lb- \_ ltitemdata** -Nachrichten senden, um die Elementdaten abzurufen oder zu ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist der null basierte Index der Zeichenfolge im Listenfeld. Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err. Wenn nicht genügend Speicherplatz vorhanden ist, um die neue Zeichenfolge zu speichern, ist der Rückgabewert "lb \_ errspace".

## <a name="remarks"></a>Bemerkungen

Wenn im Listenfeld ein vom Besitzer gezeichneter Stil und der [**lbs- \_ Sortier**](list-box-styles.md) Stil, jedoch nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil vorhanden ist, sendet das System die [**WM- \_ compareitem**](wm-compareitem.md) -Nachricht einmal oder mehrmals an den Besitzer des Listen Felds, um das neue Element ordnungsgemäß im Listenfeld zu platzieren.

Die " [**lb- \_ InitStorage**](lb-initstorage.md) "-Nachricht beschleunigt die Initialisierung von Listenfeldern, die über eine große Anzahl von Elementen (mehr als 100) verfügen. Sie reserviert die angegebene Menge an Arbeitsspeicher, sodass nachfolgende **lb- \_ AddString** -Nachrichten die kürzeste Zeit in Anspruch nehmen. Sie können Schätzwerte für den *wParam* -Parameter und den *LPARAM* -Parameter verwenden. Wenn Sie den Wert überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie unterschätzen, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Wenn das Listenfeld den [**WS- \_ HScroll**](/windows/desktop/winmsg/window-styles) -Stil aufweist und Sie eine Zeichenfolge hinzufügen, die breiter als das Listenfeld ist, senden Sie eine [**lb- \_ lthorizontalblock**](lb-sethorizontalextent.md) -Nachricht, um sicherzustellen, dass die horizontale Schiebe Leiste

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

[**LB- \_ deletestring**](lb-deletestring.md)
</dt> <dt>

[**LB- \_ InsertString**](lb-insertstring.md)
</dt> <dt>

[**LB- \_ SelectString**](lb-selectstring.md)
</dt> <dt>

[**LB-Abbild \_ Umfang**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM- \_ compareitem**](wm-compareitem.md)
</dt> </dl>

 

