---
description: ICE31 überprüft alle vordefinierten Schriftart Stile, die in Steuerelementen verwendet werden, die Text anzeigen. Außerdem wird überprüft, ob die defaultuifont-Eigenschaft auf einen gültigen Schrift Schnitt verweist.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216742"
---
# <a name="ice31"></a>ICE31

ICE31 überprüft alle vordefinierten Schriftart Stile, die in Steuer [Elementen](controls.md) verwendet werden, die Text anzeigen. Außerdem wird überprüft, ob die [**defaultuifont**](defaultuifont.md) -Eigenschaft auf einen gültigen Schrift Schnitt verweist.

Steuerelemente können ein vordefiniertes Schriftformat aufweisen, wie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md)beschrieben. Um die Schriftart und den Schrift Schnitt einer Text Zeichenfolge festzulegen, stellen Sie die Zeichenfolge der angezeigten Zeichen mit "{ \\ Style}" oder "{&*Style*}" vor. Dabei ist Style ein Bezeichner, der in der TextStyle-Spalte der [TextStyle-Tabelle](textstyle-table.md)aufgeführt ist. Wenn keines dieser beiden vorhanden ist, die [**defaultuifont**](defaultuifont.md) -Eigenschaft jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.

ICE31 überprüft die Text Spalte für jedes Steuerelement in der [Steuerelement Tabelle](control-table.md) , um zu überprüfen, ob ein gültiger Eintrag in der [TextStyle-Tabelle](textstyle-table.md)vorhanden ist.

ICE31 ignoriert das [scrollabletext-Steuer](scrollabletext-control.md)Element.

## <a name="results"></a>Ergebnisse

ICE31 gibt eine Fehlermeldung für nicht definierte Stile, Formatvorlagen Namen, die zu lang sind, eine fehlende TextStyle-Tabelle und stiltags ohne schließende geschweifte Klammer an.

ICE31 gibt eine Warnung aus, wenn sich das Stiltag nicht am Anfang der Zeile befindet, oder wenn ein Steuerelement über mehrere Style-Tags verfügt.

## <a name="example"></a>Beispiel

ICE31 gibt die folgenden Fehler für das gezeigte Beispiel aus:

-   Steuerelement dialogb. Control1 verwendet nicht definierte TextStyle-badstyle-Elemente.
-   Steuerelement dialogb. Control2 verwendet nicht definierte TextStyle-badstyle-Elemente.
-   Im Steuerelement dialogb. Control6 fehlt die schließende geschweifte Klammer im Textstil.
-   Steuerelement dialogb. Control3 gibt einen Text Stil an, der zu lang ist, um gültig zu sein.

ICE31 gibt die folgende Warnung für das folgende Beispiel aus:

-   Das textstiltag in dialogb. Control4 hat keine Auswirkung. Möchten Sie, dass Sie als Text angezeigt werden?

[Control-Tabelle](control-table.md) (partiell)



| Dialog  | Control  | Text                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dialoga | Control0 | { \\ Okstyle} Dies ist der anzuzeigende Text.                                                                                                                             |
| Dialoga | Control1 | {&okstyle} Dies ist der anzuzeigende Text.                                                                                                                              |
| Dialog GB | Control1 | {&badstyle} Dies ist der anzuzeigende Text.                                                                                                                             |
| Dialog GB | Control2 | { \\ Badstyle} Dies ist der anzuzeigende Text.                                                                                                                            |
| Dialog GB | Control3 | {&Stil, der mehr als 72 Zeichen hat und daher nicht möglicherweise ein Stil ist, auch wenn Sie es irgendwie geschafft haben, ihn in der TextStyle-Tabelle zu erhalten} Dies ist der anzuzeigende Text. |
| Dialog GB | Control4 | Warnung { \\ okstyle} Dies ist der anzuzeigende Text.                                                                                                                     |
| Dialog GB | Control5 | { \\ Okstyle} {&okstyle}. Dies ist der anzuzeigende Text.                                                                                                                   |
| Dialog GB | Control6 | { \\ Okstyle Dies ist der anzuzeigende Text.                                                                                                                             |



 

[TextStyle-Tabelle](textstyle-table.md) (partiell)



| Textart |
|-----------|
| Okstyle   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



