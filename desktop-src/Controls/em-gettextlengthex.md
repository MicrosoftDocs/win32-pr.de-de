---
title: EM_GETTEXTLENGTHEX-Nachricht (Richedit.h)
description: Berechnet die Textlänge auf verschiedene Weise. Sie wird normalerweise aufgerufen, bevor ein Puffer erstellt wird, um den Text vom Steuerelement zu empfangen.
ms.assetid: 42c89b7b-e48d-4517-9993-ce58ff9e4e40
keywords:
- EM_GETTEXTLENGTHEX Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETTEXTLENGTHEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba6cf0a094edc2288dbeae6f735e8c10fb72f943f99f9a41b15fc1ef3136168d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540939"
---
# <a name="em_gettextlengthex-message"></a>EM \_ GETTEXTLENGTHEX-Nachricht

Berechnet die Textlänge auf verschiedene Weise. Sie wird normalerweise aufgerufen, bevor ein Puffer erstellt wird, um den Text vom Steuerelement zu empfangen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Zeiger auf eine [**GETTEXTLENGTHEX-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) die die Textlängeninformationen empfängt.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Nachricht gibt die Anzahl der **TCHAR-s** im Bearbeitungssteuerelement zurück, abhängig von der Einstellung der Flags in der [**GETTEXTLENGTHEX-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex) Wenn im Flagmember inkompatible **Flags** festgelegt wurden, gibt die Meldung E \_ INVALIDARG zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung ist eine schnelle und einfache Möglichkeit, die Anzahl der Zeichen in der Unicode-Version des Rich Edit-Steuerelements zu bestimmen. Für eine Nicht-Unicode-Zielcodepage konvertieren Sie jedoch möglicherweise in eine Kombination aus Einzel-Byte- und Doppel-Byte-Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GETTEXTLENGTHEX**](/windows/desktop/api/Richedit/ns-richedit-gettextlengthex)
</dt> </dl>

 

 





