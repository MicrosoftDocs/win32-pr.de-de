---
description: Überprüfen Sie die Liste der Ime-Satzmoduswerte (Input Method Editor). Diese Werte werden mit den Funktionen ImmGetConversionStatus und ImmSetConversionStatus verwendet.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: IME-Satzmoduswerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406763"
---
# <a name="ime-sentence-mode-values"></a>IME-Satzmoduswerte

Diese Werte werden mit den Funktionen [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) und [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) verwendet.



| Konstante                  | Definition                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME \_ SMODE \_ AUTOMATIC     | Die IME führt die Konvertierungsverarbeitung im automatischen Modus durch.               |
| IME \_ SMODE \_ NONE          | Keine Informationen für Satz.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | Die IME verwendet Ausdrucksinformationen, um das nächste Zeichen vorherzusagen.             |
| IME \_ SMODE \_ PLURALCLAUSE  | Die IME verwendet Pluralklauselinformationen, um die Konvertierungsverarbeitung durchzuführen. |
| IME \_ SMODE \_ SINGLECONVERT | Die IME führt die Konvertierungsverarbeitung im Einzelzeichenmodus durch.        |
| IME \_ SMODE \_ CONVERSATION  | Die IME verwendet den Konversationsmodus. Dies ist nützlich für Chatanwendungen.      |



 

Die Bits 16 bis 31 sind für die Ime-Verwendung reserviert.

 

 



