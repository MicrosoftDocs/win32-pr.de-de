---
title: EM_GETTEXTEX Meldung (RichEdit. h)
description: Ruft den Text aus einem Rich-Edit-Steuerelement ab.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Windows-Steuerelemente für EM_GETTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476479"
---
# <a name="em_gettextex-message"></a>EM \_ gettextex-Nachricht

Ruft den Text aus einem Rich-Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur, die angibt, wie der Text übersetzt werden soll, bevor er in den Ausgabepuffer versetzt wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf den Puffer, in den der Text empfangen werden soll. Die Größe dieses Puffers in Bytes wird vom **CB** -Member der [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur angegeben. Verwenden Sie die Nachricht [**EM \_ gettextverlänex**](em-gettextlengthex.md) , um die erforderliche Größe des Puffers zu erhalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist die Anzahl von **TCHAR**-s, die in den Ausgabepuffer kopiert werden, einschließlich des NULL-Terminator.

## <a name="remarks"></a>Bemerkungen

Wenn die Größe des Ausgabepuffers kleiner ist als die Größe des Texts im-Steuerelement, kopiert das Bearbeitungs Steuerelement Text von seinem Anfang und platziert ihn im Puffer, bis der Puffer voll ist. Ein abschließende Null-Zeichen wird immer noch am Ende des Puffers platziert.

Wenn ANSI-Text angefordert wird, verwendet **EM \_ gettextex** die [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) -Funktion, um die Unicode-Zeichen in ANSI zu übersetzen. Sie können mit einer bestimmten Codepage von Unicode zu ANSI wechseln. Die [**gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex) -Struktur enthält Elemente (**lpdefaultchar** und **lpuseddefchar**), die bei der Übersetzung von Unicode in ANSI verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ settextex**](em-settextex.md)
</dt> <dt>

[**Gettextex**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**WM- \_ SetText**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

