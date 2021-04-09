---
title: CB_GETLBTEXTLEN Meldung (Winuser. h)
description: Ruft die Länge einer Zeichenfolge in der Liste eines Kombinations Felds in Zeichen ab.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Windows-Steuerelemente für CB_GETLBTEXTLEN Meldung
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956453"
---
# <a name="cb_getlbtextlen-message"></a>CB \_ getlbtextlen-Meldung

Ruft die Länge einer Zeichenfolge in der Liste eines Kombinations Felds in Zeichen ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der null basierte Index der Zeichenfolge.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, wobei das abschließende Null-Zeichen ausgeschlossen wird. Wenn eine ANSI-Zeichenfolge die Anzahl von Bytes ist, und wenn es sich um eine Unicode-Zeichenfolge handelt, ist dies die Anzahl der Zeichen. Unter bestimmten Bedingungen ist dieser Wert möglicherweise größer als die Länge des Texts. Weitere Informationen finden Sie im Abschnitt "Hinweise".

Wenn der *wParam* -Parameter keinen gültigen Index angibt, ist der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Unter bestimmten Bedingungen ist der Rückgabewert größer als die tatsächliche Textlänge. Dies tritt bei bestimmten Kombinationen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das Betriebssystem das mögliche vorhanden sein von DBCS-Zeichen (Double-Byte Character Set) im Text zulässt. Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Textlänge. Sie können es also immer verwenden, um die Puffer Zuordnung zu steuern. Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialogfelder verwendet, die Unicode verwenden.

Um die genaue Länge des Texts zu erhalten, verwenden Sie die Nachrichten [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)oder [**CB \_ getlbtext**](cb-getlbtext.md) oder die Funktion [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

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

 

