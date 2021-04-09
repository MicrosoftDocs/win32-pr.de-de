---
description: Diese Werte werden mit den Funktionen "immgetdeversionstatus" und "immsetconfiguration" verwendet.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Werte des IME-Konvertierungsmodus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129740"
---
# <a name="ime-conversion-mode-values"></a>Werte des IME-Konvertierungsmodus

Diese Werte werden mit den Funktionen " [**immgetdeversionstatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) " und " [**immsetconfiguration**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) " verwendet.



| bit                      | Bedeutung                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| \_alphanumerischer IME-cmode-Wert \_ | Alphanumerischer Eingabemodus. Dies ist die Standardeinstellung, die als 0x0000 definiert ist.                          |
| IME- \_ cmode- \_ CharCode     | Auf 1 festgelegt, wenn Zeichencode Eingabemodus; 0, wenn nicht.                                          |
| IME- \_ cmode- \_ EUDC         | Auf 1 festgelegt, wenn EUDC-Konvertierungsmodus; 0, wenn nicht.                                               |
| IME- \_ cmode- \_ Fehler        | **Windows Me/98, Windows 2000, Windows XP:** Auf 1 festgelegt, wenn fester Konvertierungsmodus; 0, wenn nicht. |
| IME \_ cmode \_ fullshape    | Auf 1 festgelegt, wenn vollständiger Shape-Modus; 0 (null), wenn Halbform Modus.                                        |
| IME- \_ cmode- \_ hanjaconvert | Auf 1 festgelegt, wenn der Hanja-Konvertierungsmodus. 0, wenn nicht.                                                 |
| IME- \_ cmode- \_ Katakana     | Auf 1 festgelegt, wenn Katakana-Modus; 0, wenn der Hiragana-Modus ist.                                            |
| IME \_ cmode \_ Native       | Auf 1 festgelegt, wenn der einheitliche Modus ist; 0 (null), wenn der alphanumerische Modus ist.                                          |
| IME \_ cmode- \_ noconversion | Auf 1 festgelegt, um die Verarbeitung von Konvertierungen durch IME zu verhindern. 0, wenn nicht.                           |
| IME \_ cmode- \_ Roman        | Auf 1 festgelegt, wenn der römische Eingabemodus; 0, wenn nicht.                                                   |
| IME \_ cmode- \_ Software      | Auf 1 festgelegt, wenn weicher Tastaturmodus 0, wenn nicht.                                                 |
| IME- \_ cmode- \_ Symbol       | Auf 1 festgelegt, wenn der Modus für die Symbol Konvertierung 0, wenn nicht.                                             |



 

Alle anderen Bits sind reserviert.

 

 



