---
title: CB_GETLBTEXTLEN Meldung (Winuser.h)
description: Ruft die Länge einer Zeichenfolge in Zeichen in der Liste eines Kombinationsfelds ab.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- CB_GETLBTEXTLEN Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: cb226a9012d9573e17bd88a114ebcd2b96e406a38208cc78a925bdca976cd4b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089150"
---
# <a name="cb_getlbtextlen-message"></a>CB \_ GETLBTEXTLEN-Nachricht

Ruft die Länge einer Zeichenfolge in Zeichen in der Liste eines Kombinationsfelds ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der nullbasierte Index der Zeichenfolge.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Länge der Zeichenfolge in **TCHAR** s, mit Ausnahme des abschließenden NULL-Zeichens. Wenn eine ANSI-Zeichenfolge die Anzahl der Bytes ist, und wenn es sich um eine Unicode-Zeichenfolge handelt, ist dies die Anzahl der Zeichen. Unter bestimmten Umständen kann dieser Wert tatsächlich größer als die Länge des Texts sein. Weitere Informationen finden Sie im Abschnitt "Hinweise".

Wenn der *wParam-Parameter* keinen gültigen Index angibt, lautet der Rückgabewert CB \_ ERR.

## <a name="remarks"></a>Hinweise

Unter bestimmten Umständen ist der Rückgabewert größer als die tatsächliche Länge des Texts. Dies tritt bei bestimmten Mischungen von ANSI und Unicode auf und ist darauf zurückzuführen, dass das Betriebssystem das mögliche Vorhandensein von Doppel-Byte-Zeichensatzzeichen (Double-Byte Character Set, DBCS) im Text zulässt. Der Rückgabewert ist jedoch immer mindestens so groß wie die tatsächliche Länge des Texts. damit Sie sie immer verwenden können, um die Pufferzuordnung zu steuern. Dieses Verhalten kann auftreten, wenn eine Anwendung sowohl ANSI-Funktionen als auch allgemeine Dialoge verwendet, die Unicode verwenden.

Um die genaue Länge des Texts abzurufen, verwenden Sie die [**WM \_ GETTEXT-,**](/windows/desktop/winmsg/wm-gettext) [**LB \_ GETTEXT-**](lb-gettext.md)oder [**CB \_ GETLBTEXT-Nachrichten**](cb-getlbtext.md) oder die [**GetWindowText-Funktion.**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ GETLBTEXT**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETTEXT**](lb-gettext.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

