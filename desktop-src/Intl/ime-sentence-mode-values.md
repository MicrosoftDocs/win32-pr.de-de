---
description: Überprüfen Sie die Liste der ImE-Satzmoduswerte (Input Method Editor, Eingabemethode-Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME-Satzmoduswerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146129"
---
# <a name="ime-sentence-mode-values"></a>IME-Satzmoduswerte

Diese Werte werden mit den [**Funktionen ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.



| Konstante                  | Definition                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | Der IME führt die Konvertierungsverarbeitung im automatischen Modus aus.               |
| IME \_ SMODE \_ NONE          | Keine Informationen zum Satz.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | Der IME verwendet Ausdrucksinformationen, um das nächste Zeichen vorherzusagen.             |
| IME \_ SMODE \_ PLURALCLAUSE  | Der IME verwendet Pluralklauselinformationen, um die Konvertierungsverarbeitung durchführen zu können. |
| IME \_ SMODE \_ SINGLECONVERT | Der IME führt die Konvertierungsverarbeitung im Einzelzeichenmodus durch.        |
| IME \_ SMODE \_ CONVERSATION  | Der IME verwendet den Konversationsmodus. Dies ist nützlich für Chatanwendungen.      |



 

Bits 16 bis 31 sind für die IME-Verwendung reserviert.

 

 



