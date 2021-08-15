---
title: Flags für den Konvertierungsmodus (Ctffunc.h)
description: Die folgenden Flags werden als Wert für GUID \_ DEPOT \_ KEYBOARD \_ INPUTMODE CONVERSION \_ verwendet. Dies entspricht IME \_ CMODE-Werten für IMM32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Flags für den Konvertierungsmodus Textdienstframework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c8c3a452e3115e66e4f0f6e75999cad9bce7e1eadf14b4cadd24fae640a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879216"
---
# <a name="flags-for-conversion-mode"></a>Flags für den Konvertierungsmodus

Die folgenden Flags werden als Wert von [GUID \_ DEPOT KEYBOARD \_ \_ INPUTMODE \_ CONVERSION](predefined-compartments.md)verwendet. Dies entspricht [IME \_ CMODE-Werten](../intl/ime-conversion-mode-values.md) für IMM32.



| Flag                             | Wert  | BESCHREIBUNG                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONVERSIONMODE \_ ALPHANUMERIC | 0x0000 | Legen Sie auf 1 fest, wenn der ALPHANUMERIC-Modus aktiviert ist.                                  |
| TF \_ CONVERSIONMODE \_ NATIVE       | 0x0001 | Legen Sie auf 1 fest, wenn der NATIVE Modus festgelegt ist. 0, wenn der ALPHANUMERIC-Modus ist.                |
| TF \_ CONVERSIONMODE \_ KATAKANA     | 0x0002 | Legen Sie auf 1 fest, wenn der KATAKANA-Modus aktiviert ist. 0, wenn der HIRAGANA-Modus.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Legen Sie auf 1 fest, wenn der Modus für die vollständige Form aktiviert ist. 0, wenn halber Formmodus.              |
| TF \_ CONVERSIONMODE \_ ROMAN        | 0x0010 | Legen Sie diese Einstellung auf 1 fest, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0 , wenn nicht. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Legen Sie auf 1 fest, wenn der Zeichencodeeingabemodus aktiviert ist. 0 , wenn nicht.                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | Legen Sie auf 1 fest, wenn der Modus für die softe Tastatur aktiviert ist. 0 , wenn nicht.                       |
| TF \_ CONVERSIONMODE \_ NOCONVERSION | 0x0100 | Legen Sie diese Einstellung auf 1 fest, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0 , wenn nicht. |
| TF \_ \_ CONVERSIONMODE-SYMBOL       | 0x0400 | Legen Sie auf 1 fest, wenn der SYMBOL-Konvertierungsmodus aktiviert ist. 0 , wenn nicht.                   |
| TF \_ CONVERSIONMODE \_ FIXED        | 0x0800 | Bei festem Konvertierungsmodus auf 1 festgelegt. 0 , wenn nicht.                    |



 

Die folgenden Werte werden als Wert von [GUID \_ DEPOT KEYBOARD \_ \_ INPUTMODE \_ SENTENCE](predefined-compartments.md)verwendet. Dies entspricht [ \_ IME-SMODE-Werten](../intl/ime-composition-string-values.md) für IMM32.



| Flag                            | Wert  | BESCHREIBUNG                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ NONE          | 0x0000 | Keine Informationen für Satz.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | Die IME verwendet Pluralklauselinformationen, um die Konvertierungsverarbeitung durchzuführen. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | Die IME führt die Konvertierungsverarbeitung im Einzelzeichenmodus durch.        |
| TF \_ SENTENCEMODE \_ AUTOMATIC     | 0x0004 | Die IME führt die Konvertierungsverarbeitung im automatischen Modus durch.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | Die IME verwendet Ausdrucksinformationen, um das nächste Zeichen vorherzusagen.             |
| TF \_ SENTENCEMODE \_ CONVERSATION  | 0x0010 | Die IME verwendet den Konversationsmodus. Dies ist nützlich für Chatanwendungen.      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Verteilbare Komponente<br/>          | TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| Header<br/>                   | <dl> <dt>Ctffunc.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctffunc.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vordefinierte Depots](predefined-compartments.md)
</dt> </dl>

 

