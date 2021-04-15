---
title: EM_SETTEXTEX Meldung (RichEdit. h)
description: Kombiniert die Funktionalität der WM- \_ Meldungen "SetText" und "em \_ replacesel" und bietet die Möglichkeit, Text mithilfe einer Codepage festzulegen und entweder Rich-Text oder nur-Text zu verwenden.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Windows-Steuerelemente für EM_SETTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477310"
---
# <a name="em_settextex-message"></a>EM \_ settextex-Nachricht

Kombiniert die Funktionalität der WM-Meldungen " [**\_ SetText**](/windows/desktop/winmsg/wm-settext) " und " [**EM \_ replacesel**](em-replacesel.md) " und bietet die Möglichkeit, Text mithilfe einer Codepage festzulegen und entweder Rich-Text oder nur-Text zu verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein Zeiger auf eine [**settextex**](/windows/desktop/api/Richedit/ns-richedit-settextex) -Struktur, die Flags und eine optionale Codepage angibt, die bei der Übersetzung in Unicode verwendet werden soll.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf den einzufügenden null-terminierten Text. Dieser Text ist eine ANSI-Zeichenfolge, es sei denn, die Codepage ist 1200 (Unicode). Wenn *LPARAM* mit einer gültigen RTF-ASCII-Sequenz beginnt, z. b. "{ \\ RTF" oder "{urtf", wird der Text mit dem RTF-Reader gelesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang den gesamten Text festlegt und erfolgreich ist, lautet der Rückgabewert 1.

Wenn der Vorgang die Auswahl festlegt und erfolgreich ist, ist der Rückgabewert die Anzahl der kopierten Bytes oder Zeichen.

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ gettextex**](em-gettextex.md)
</dt> <dt>

[**Settextex**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

