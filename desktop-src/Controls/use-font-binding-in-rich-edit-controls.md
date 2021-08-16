---
title: Verwenden der Schriftartbindung in Rich Edit-Steuerelementen
description: Microsoft Rich Edit 3.0 weist nur Textzeichen je nach Kontext einen Zeichensatz zu.
ms.assetid: 975B9C33-6766-4FF1-A93E-2169C140CEE9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3086f9f74469bc535700f28b6eeb45c204024beb34c21663139fd3d63746d4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829024"
---
# <a name="how-to-use-font-binding-in-rich-edit-controls"></a>Verwenden der Schriftartbindung in Rich Edit-Steuerelementen

Microsoft Rich Edit 3.0 weist nur Textzeichen je nach Kontext einen Zeichensatz zu. Beispiele:

-   Griechisch-Zeichen wird **GREEK \_ CHARSET** zugewiesen.
-   Hangul-Symbolen wird **HANGUL \_ CHARSET** zugewiesen.
-   Chinesische Zeichen werden **SHIFTJIS \_ CHARSET** zugewiesen, wenn Kanazeichen in der Nähe gefunden werden, oder **GB2312 \_ CHARSET,** wenn kein Kana in der Nähe gefunden wird.
-   Nicht neutrale ANSI-Zeichen werden in jedem Fall **ANSI \_ CHARSET** zugewiesen.

> [!Note]  
> Das Rich Edit-Steuerelement verwendet intern Unicode, sodass sich diese Verwendung von Zeichensätzen von der ursprünglichen Verwendung in Schriftartspezifikationen unterscheidet. Die [**CHARFORMAT-Struktur**](/windows/win32/api/richedit/ns-richedit-charformata) verfügt jedoch über einen klar definierten Ort für den Zeichensatz.

 

Neutralen Zeichen wie Leerzeichen und Ziffern wird je nach Kontext ein Zeichensatz zugewiesen. Beispielsweise ruft ein Leerzeichen, das von Zeichen des gleichen Zeichensatzes umgeben ist, diesen Zeichensatz ab. Neutralen und Ziffern, die für bidirektionalen Text verwendet werden, werden Zeichensätze auf eine Weise zugewiesen, die auf dem bidirektionalen Unicode-Algorithmus basiert.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-font-binding-in-a-rich-edit-control"></a>Verwenden der Schriftartbindung in einem Rich Edit-Steuerelement

Nachdem Zeichensätze zugewiesen wurden, scannt Rich Edit den Text um die Einfügemarke vorwärts und rückwärts, um die nächstgelegenen Schriftarten zu finden, die für die Zeichensätze verwendet wurden. Wenn für einen Zeichensatz keine Schriftart gefunden wird, verwendet Rich Edit die Schriftart, die vom Client für diesen Zeichensatz ausgewählt wurde. Wenn der Client keine Schriftart für den Zeichensatz angegeben hat, verwendet Rich Edit die Standardschriftart für diesen Zeichensatz. Wenn der Client eine andere Schriftart wünscht, kann der Client diese immer ändern, aber dieser Ansatz funktioniert meistens. Die aktuellen Standardschriftarten basieren auf der folgenden Tabelle. Beachten Sie, dass die Standardschriftarten pro Prozess festgelegt werden, und es gibt separate Listen für die Benutzeroberflächenverwendung und für die Verwendung außerhalb der Benutzeroberfläche.



| Sprache                    | Schriftartname der Benutzeroberfläche  | Schriftgrad der Benutzeroberfläche | Schriftartname, der nicht auf der Benutzeroberfläche enthalten ist | Schriftgrad ohne Benutzeroberfläche |
|-----------------------------|---------------|--------------|------------------|------------------|
| West, CE, ME, Westeuropa | Tahoma        | 8            | Arial            | 10               |
| Japanisch                    | MS UI-Nutzeroberfläche  | 9            | MS P(      | 10               |
| Koreanisch                      | Gulim         | 9            | Gulim            | 9                |
| Chinesisch (vereinfacht)          | Simsun        | 9            | SimSun           | 10               |
| Chinesisch (traditionell)         | PMingLiU      | 9            | PMingLiU         | 9                |
| Thailändisch                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Symbole                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamilisch                       | Laota         | 8            | Laota            | 10               |
| Libyisch, Libyisch          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Aus diesem Grund ermöglicht Rich Edit in der Standardtabelle für die Schriftartbindung (Einträge haben einen Zeichensatz, einen Schriftartnamen und eine Größe) an ANSI CHARSET die \_ Übereinstimmung mit mehreren Zeichensätzen, während der entsprechende Zeichensatz 1:1 mit anderen Schriftarten übereinstimmt. Genauer gesagt verwendet rich edit immer dann die \_ ANSI CHARSET-Auswahl, wenn keine andere Alternative gefunden wird. Sie können eine höhere Granularität als diese angeben. Weisen Sie z. B. ein bestimmtes ARABISCHES \_ CHARSET für arabische Ausführungen, eine bestimmte griechisch-Schriftart für griechisch-Läufe usw. zu. Diese präzisere Granularität wird auch verwendet, wenn sich eine Schriftart mit dem gewünschten Zeichensatzstempel an einer beliebigen Stelle im Dokument vor dem Bereich befindet, der an die Schriftart gebunden wird.

Beachten Sie, dass Rich Edit derzeit kein fehlendes Glyphen in einer Schriftart behandelt, die angibt, einen Zeichensatz zu unterstützen, aber unvollständig ist. Zum Zeitpunkt der Anzeige in einem komplexen Skript weiß Rich Edit, dass ein solches Glyph fehlt, führt jedoch nicht dazu, dass der Sicherungsspeicher eine neue Schriftart verwendet. Normalerweise wird dies durch die zugrunde liegende Schriftartverknüpfung des Betriebssystems erreicht.

## <a name="remarks"></a>Hinweise

**Rich Edit 4.1:** Um die Standardschriftart für ein Skript festzulegen, rufen [**Sie EM \_ SETCHARFORMAT**](em-setcharformat.md) mit [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)auf und geben Werte für die Member **yHeight,** **bCharSet,** **bPitchAndFamily,** **szFaceName** und **lcid** an. Um die Standardschriftart für eine bestimmte Codepage abzurufen, rufen [**Sie EM \_ GETCHARFORMAT**](em-getcharformat.md) mit **CHARFORMAT2** auf und geben Werte für die Member **bCharSet** und **lcid** an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




