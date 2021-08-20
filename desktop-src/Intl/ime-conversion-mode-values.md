---
description: Überprüfen Sie die Liste der ImE-Konvertierungsmoduswerte (Input Method Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: IME-Konvertierungsmoduswerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aa2f400dbf75346b537df2a0c724ea0a241a6c3b32ef23b2f27a2ce5d075e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810380"
---
# <a name="ime-conversion-mode-values"></a>IME-Konvertierungsmoduswerte

Diese Werte werden mit den Funktionen [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.



| bit                      | Bedeutung                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE \_ ALPHANUMERIC | Alphanumerischer Eingabemodus. Dies ist der Standardwert, der als 0x0000 definiert ist.                          |
| IME \_ CMODE \_ CHARCODE     | Legen Sie auf 1 fest, wenn der Zeichencodeeingabemodus aktiviert ist. 0 , wenn nicht.                                          |
| IME \_ CMODE \_ EUDC         | Legen Sie auf 1 fest, wenn der EUDC-Konvertierungsmodus aktiviert ist. 0 , wenn nicht.                                               |
| IME \_ CMODE \_ FIXED        | **Windows Me/98, Windows 2000, Windows XP:** Bei festem Konvertierungsmodus auf 1 festgelegt. 0 , wenn nicht. |
| IME \_ CMODE \_ FULLSHAPE    | Legen Sie auf 1 fest, wenn der Modus für die vollständige Form aktiviert ist. 0, wenn halber Formmodus.                                        |
| IME \_ CMODE \_ HANJACONVERT | Legen Sie auf 1 fest, wenn der HANJA-Konvertierungsmodus aktiviert ist. 0 , wenn nicht.                                                 |
| IME \_ CMODE \_ KATAKANA     | Legen Sie auf 1 fest, wenn der KATAKANA-Modus aktiviert ist. 0, wenn der HIRAGANA-Modus.                                            |
| IME \_ CMODE \_ NATIVE       | Legen Sie auf 1 fest, wenn der NATIVE Modus festgelegt ist. 0, wenn der ALPHANUMERIC-Modus ist.                                          |
| IME \_ CMODE \_ NOCONVERSION | Legen Sie diese Einstellung auf 1 fest, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0 , wenn nicht.                           |
| IME \_ CMODE \_ ROMAN        | Legen Sie auf 1 fest, wenn der ROMAN-Eingabemodus aktiviert ist. 0 , wenn nicht.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Legen Sie auf 1 fest, wenn der Modus für die softe Tastatur aktiviert ist. 0 , wenn nicht.                                                 |
| IME \_ \_ CMODE-SYMBOL       | Legen Sie auf 1 fest, wenn der SYMBOL-Konvertierungsmodus aktiviert ist. 0 , wenn nicht.                                             |



 

Alle anderen Bits sind reserviert.

 

 



