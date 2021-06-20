---
description: Überprüfen Sie die Liste der ImE-Konvertierungsmoduswerte (Input Method Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Werte des IME-Konvertierungsmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406753"
---
# <a name="ime-conversion-mode-values"></a>Werte des IME-Konvertierungsmodus

Diese Werte werden mit den [**Funktionen ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.



| bit                      | Bedeutung                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| IME \_ CMODE \_ ALPHANUMERIC | Alphanumerischer Eingabemodus. Dies ist die Standardeinstellung, die als 0x0000.                          |
| IME \_ CMODE \_ CHARCODE     | Legen Sie auf 1 fest, wenn der Zeichencodeeingabemodus ist. 0, wenn nicht.                                          |
| IME \_ CMODE \_ EUDC         | Legen Sie auf 1 fest, wenn der EUDC-Konvertierungsmodus ist. 0, wenn nicht.                                               |
| IME \_ CMODE \_ FIXED        | **Windows Me/98, Windows 2000, Windows XP:** Legen Sie auf 1 fest, wenn der Konvertierungsmodus fest ist. 0, wenn nicht. |
| IME \_ CMODE \_ FULLSHAPE    | Legen Sie auf 1 fest, wenn der Vollformmodus aktiviert ist. 0, wenn halber Formmodus.                                        |
| IME \_ CMODE \_ HANJACONVERT | Legen Sie auf 1 fest, wenn der HANJA-Konvertierungsmodus aktiviert ist. 0, wenn nicht.                                                 |
| IME \_ CMODE \_ KATAKANA     | Legen Sie auf 1 fest, wenn der KATAKANA-Modus ist. 0, wenn HIRAGANA-Modus.                                            |
| IME \_ CMODE \_ NATIVE       | Legen Sie auf 1 fest, wenn der MODUS NATIV ist. 0, wenn der ALPHANUMERIC-Modus.                                          |
| IME \_ CMODE \_ NOCONVERSION | Legen Sie auf 1 fest, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.                           |
| IME \_ CMODE \_ ROMAN        | Legen Sie auf 1 fest, wenn der EINGABEMODUS FÜR ROMAN festgelegt ist. 0, wenn nicht.                                                   |
| IME \_ CMODE \_ SOFTKBD      | Legen Sie auf 1 fest, wenn der Softtastaturmodus aktiviert ist. 0, wenn nicht.                                                 |
| \_IME-CMODE-SYMBOL \_       | Legen Sie auf 1 fest, wenn der SYMBOL-Konvertierungsmodus aktiviert ist. 0, wenn nicht.                                             |



 

Alle anderen Bits sind reserviert.

 

 



