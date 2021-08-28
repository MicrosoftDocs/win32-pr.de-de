---
description: ICE31 überprüft alle vordefinierten Schriftschnitte, die in Steuerelementen verwendet werden, die Text anzeigen. Außerdem wird überprüft, ob die DefaultUIFont-Eigenschaft auf einen gültigen Schriftschnitt verweist.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 783c8b842f80707bbd1ca833fbc7ad1f154a47a0d3aa24377ee58a1c6549bf7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528670"
---
# <a name="ice31"></a>ICE31

ICE31 überprüft alle vordefinierten Schriftschnitte, die in Steuerelementen verwendet [werden,](controls.md) die Text anzeigen. Außerdem wird überprüft, ob die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) auf einen gültigen Schriftschnitt verweist.

Steuerelemente können einen vordefinierten Schriftschnitt haben, wie unter [Hinzufügen von Steuerelementen und Text beschrieben.](adding-controls-and-text.md) Stellen Sie der Zeichenfolge der angezeigten Zeichen { style} oder {&style } voran, um die Schriftart und den \\ Schriftschnitt einer Textzeichenfolge zu setzen. Dabei ist style ein Bezeichner, der in der TextStyle -Spalte der [TextStyle-Tabelle aufgeführt ist.](textstyle-table.md) Wenn keines dieser Eigenschaften vorhanden ist, die [**DefaultUIFont-Eigenschaft**](defaultuifont.md) jedoch als gültiger Textstil definiert ist, wird diese Schriftart verwendet.

ICE31 überprüft die Text -Spalte [](control-table.md) für jedes Steuerelement in der Steuertabelle, um zu überprüfen, ob ein gültiger Eintrag in der [TextStyle-Tabelle vorhanden ist.](textstyle-table.md)

ICE31 ignoriert das [ScrollableText-Steuerelement.](scrollabletext-control.md)

## <a name="results"></a>Ergebnisse

ICE31 veröffentlicht eine Fehlermeldung für nicht definierte Stile, zu lange Formatnamen, eine fehlende TextStyle-Tabelle und Formattags ohne schließende geschweifte Klammer.

ICE31 gibt eine Warnung aus, wenn sich das Formattag nicht am Anfang der Zeile befindet oder wenn ein Steuerelement über mehrere Formattags verfügt.

## <a name="example"></a>Beispiel

ICE31 veröffentlicht die folgenden Fehler für das gezeigte Beispiel:

-   Das Steuerelement DialogB.Control1 verwendet nicht definierten TextStyle BadStyle.
-   Control DialogB.Control2 verwendet nicht definierte TextStyle BadStyle.
-   Das Steuerelement DialogB.Control6 fehlt die schließende geschweifte Klammer im Textformat.
-   Control DialogB.Control3 gibt einen Textstil an, der zu lang ist, um gültig zu sein.

ICE31 gibt die folgende Warnung für das gezeigte Beispiel aus:

-   Das Textformattag in DialogB.Control4 hat keine Auswirkungen. Möchten Sie, dass es als Text angezeigt wird?

[Steuertabelle](control-table.md) (partiell)



| Dialog  | Control  | Text                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialogA | Control0 | { \\ OKStyle}Dies ist der anzuzeigende Text.                                                                                                                             |
| DialogA | Control1 | {&OKStyle} Dies ist der anzuzeigende Text.                                                                                                                              |
| DialogB | Control1 | {&BadStyle} Dies ist der anzuzeigende Text.                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle}Dies ist der anzuzeigende Text.                                                                                                                            |
| DialogB | Control3 | {&Style, der mehr als 72 Zeichen hat und daher auch dann kein Stil sein kann, wenn Sie es auf irgendeine Weise in der TextStyle-Tabelle erhalten haben} Dies ist der anzuzeigende Text. |
| DialogB | Control4 | Warnung { \\ OKStyle}Dies ist der anzuzeigende Text.                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle}{&OKStyle}Dies ist der anzuzeigende Text.                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle Dies ist der anzuzeigende Text.                                                                                                                             |



 

[TextStyle-Tabelle](textstyle-table.md) (partiell)



| TextStyle |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



