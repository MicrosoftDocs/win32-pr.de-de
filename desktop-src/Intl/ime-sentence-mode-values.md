---
description: Diese Werte werden mit den Funktionen "immgetdeversionstatus" und "immsetconfiguration" verwendet.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Werte für den IME-Satzmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216237"
---
# <a name="ime-sentence-mode-values"></a>Werte für den IME-Satzmodus

Diese Werte werden mit den Funktionen " [**immgetdeversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) " und " [**immsetconfiguration**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) " verwendet.



| Konstante                  | Definition                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| IME- \_ smode \_ automatisch     | Der IME führt die Konvertierungs Verarbeitung im automatischen Modus aus.               |
| IME \_ smode \_ None          | Keine Informationen für einen Satz.                                               |
| IME \_ smode \_ phravervorhersage | Der IME verwendet Ausdrucks Informationen, um das nächste Zeichen vorherzusagen.             |
| IME \_ smode \_ pluralclause  | Der IME verwendet die Plural-klauselinformationen, um die Konvertierungs Verarbeitung auszuführen. |
| IME \_ smode \_ singleconvert | Der IME führt die Konvertierungs Verarbeitung im Einzelzeichen Modus aus.        |
| IME- \_ smode- \_ Konversation  | Der IME verwendet den Konversationsmodus. Dies ist nützlich für Chat Anwendungen.      |



 

Bits 16 bis 31 sind für die IME-Verwendung reserviert.

 

 



