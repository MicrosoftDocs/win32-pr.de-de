---
title: LB_GETTEXTLEN Meldung (Winuser. h)
description: Ruft die Länge einer Zeichenfolge in einem Listenfeld ab.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Windows-Steuerelemente für LB_GETTEXTLEN Meldung
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103483"
---
# <a name="lb_gettextlen-message"></a>LB- \_ gettextlen-Nachricht

Ruft die Länge einer Zeichenfolge in einem Listenfeld ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Zeichenfolge.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der *wParam* -Parameter ist auf 16-Bit-Werte beschränkt. Dies bedeutet, dass Listenfelder nicht mehr als 32.767 Elemente enthalten dürfen. Obwohl die Anzahl der Elemente eingeschränkt ist, wird die Gesamtgröße der Elemente in einem Listenfeld in Bytes nur durch den verfügbaren Arbeitsspeicher beschränkt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird. Unter bestimmten Bedingungen ist dieser Wert möglicherweise größer als die Länge des Texts. Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".

Wenn vom *wParam* -Parameter kein gültiger Index angegeben wird, ist der Rückgabewert lb \_ Err.

## <a name="remarks"></a>Bemerkungen

Unter bestimmten Bedingungen ist der Rückgabewert größer als die tatsächliche Textlänge. Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das Betriebssystem das mögliche vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt. Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können Sie daher immer verwenden, um die Puffer Zuordnung zu steuern. Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.

Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)oder [**CB \_ getlbtext**](cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

Wenn im Listenfeld ein vom Besitzer gezeichneter Stil, aber nicht der [**lbs \_ hasstrings**](list-box-styles.md) -Stil enthalten ist, ist der Rückgabewert immer die Größe eines **DWORD**(in Bytes).

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

[**CB \_ getlbtext**](cb-getlbtext.md)
</dt> <dt>

[**LB- \_ gettext**](lb-gettext.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

