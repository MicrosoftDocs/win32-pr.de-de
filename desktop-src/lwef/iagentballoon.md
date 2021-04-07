---
title: Iagentballoon
description: Iagentballoon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725569"
---
# <a name="iagentballoon"></a>Iagentballoon

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

**Iagentballoon** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Eigenschaften für die Word-Sprechblase von Microsoft-Agent abzufragen. Diese Funktionen sind auch über [**iagentballoonex**](https://www.bing.com/search?q=**IAgentBalloonEx**)verfügbar.

Anfängliche Standardwerte für die Word-Sprechblase eines Zeichens werden im Microsoft-Agent-Zeichen-Editor festgelegt. Nachdem die Anwendung ausgeführt wurde, kann der Benutzer die [**aktivierten**](enabled-property.md) Eigenschaften und die [Schriftart](fontname-property.md) Eigenschaften überschreiben. Wenn ein Benutzer die Eigenschaften der Sprechblase ändert, wirkt sich die Änderung auf alle Zeichen aus. Die Eigenschaften des [**iagentballoon**](/windows/desktop/lwef/iagentballoon) -Objekts gelten auch für die Textausgabe über die " [**Think**](think-method.md) "-Methode.

**Methoden in Vtable-Reihenfolge**



| Iagentballoon-Methoden                                       | BESCHREIBUNG                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | Gibt zurück, ob die Word-Sprechblase aktiviert ist.                                          |
| [Getnumlines](iagentballoon--getnumlines.md)               | Gibt die Anzahl der Zeilen zurück, die in der Wort Sprechblase angezeigt werden.                            |
| [Getnumcharsperline](iagentballoon--getnumcharsperline.md) | Gibt die durchschnittliche Anzahl von Zeichen pro Zeile zurück, die in der Word-Sprechblase angezeigt wird.      |
| [GetFontName](iagentballoon--getfontname.md)               | Gibt den Namen der Schriftart zurück, die in der Word-Sprechblase angezeigt wird.                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | Gibt die Größe der Schriftart zurück, die in der Word-Sprechblase angezeigt wird.                           |
| [Getfontbold](iagentballoon--getfontbold.md)               | Gibt zurück, ob die in der Wort Sprechblase angezeigte Schriftart fett formatiert ist.                       |
| [Getfontitalic](iagentballoon--getfontitalic.md)           | Gibt zurück, ob die in der Wort Sprechblase angezeigte Schriftart kursiv formatiert ist.                     |
| [Getfontstrikethru](iagentballoon--getfontstrikethru.md)   | Gibt zurück, ob die in der Word-Sprechblase angezeigte Schriftart als durchgestrichen angezeigt wird. |
| [GetFont-Unterstreichung](iagentballoon--getfontunderline.md)     | Gibt zurück, ob die in der Wort Sprechblase angezeigte Schriftart unterstrichen ist.                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | Gibt die Vordergrundfarbe zurück, die in der Wort Blase angezeigt wird.                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | Gibt die Hintergrundfarbe zurück, die in der Wort Sprechblase angezeigt wird.                           |
| [GetBorderColor](iagentballoon--getbordercolor.md)         | Gibt die Rahmenfarbe zurück, die in der Wort Sprechblase angezeigt wird.                               |
| [SetVisible](iagentballoon--setvisible.md)                 | Legt fest, dass die Wort Sprechblase sichtbar ist.                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | Gibt die Sichtbarkeits Einstellung für die Word-Sprechblase zurück.                                  |
| [Setfontname](iagentballoon--setfontname.md)               | Legt die in der Wort Sprechblase verwendete Schriftart fest.                                               |
| [SetFontSize](iagentballoon--setfontsize.md)               | Legt den in der Wort Sprechblase verwendeten Schrift Grad fest.                                          |
| [Setfontcharset](iagentballoon--setfontcharset.md)         | Legt den in der Wort Sprechblase verwendeten Zeichensatz fest.                                      |
| [Getfontcharset](iagentballoon--getfontcharset.md)         | Gibt den Zeichensatz zurück, der in der Wort Sprechblase verwendet wird.                                   |



 

 

 