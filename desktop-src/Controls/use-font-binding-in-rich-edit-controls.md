---
title: Verwenden der Schriftartbindung in Rich Edit-Steuerelementen
description: Microsoft Rich Edit 3.0 weist Je nach Kontext Nur-Text-Zeichen einen Zeichensatz zu.
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

Microsoft Rich Edit 3.0 weist Je nach Kontext Nur-Text-Zeichen einen Zeichensatz zu. Beispiele:

-   Griechisch-Zeichen wird **GREEK \_ CHARSET zugewiesen.**
-   Hangul-Symbolen wird **HANGUL \_ CHARSET zugewiesen.**
-   Chinesische Zeichen werden **SHIFTJIS \_ CHARSET** zugewiesen, wenn Kanazeichen in der Nähe gefunden werden, oder **GB2312 \_ CHARSET,** wenn in der Nähe kein Kana gefunden wird.
-   Nicht neutralen ANSI-Zeichen werden **in jedem Fall ANSI \_ CHARSET** zugewiesen.

> [!Note]  
> Das Rich-Edit-Steuerelement verwendet Unicode intern, sodass sich diese Verwendung von Zeichensätzen von der ursprünglichen Verwendung in Schriftartspezifikationen unterscheidet. Die [**CHARFORMAT-Struktur**](/windows/win32/api/richedit/ns-richedit-charformata) verfügt jedoch über eine klar definierte Stelle für den Zeichensatz.

 

Neutralen Zeichen wie Leerzeichen und Ziffern wird je nach Kontext ein Zeichensatz zugewiesen. Beispielsweise erhält ein Leerzeichen, das von Zeichen desselben Zeichensets umgeben ist, diesen Zeichensatz. Neutralen und Ziffern, die für bidirektionalen Text verwendet werden, werden Zeichensätze in einer Weise zugewiesen, die auf dem bidirektionalen Unicode-Algorithmus basiert.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-font-binding-in-a-rich-edit-control"></a>Verwenden der Schriftartbindung in einem Rich Edit-Steuerelement

Nachdem Zeichensätze zugewiesen wurden, scannt Rich Edit den Text um die Einfügemarke vorwärts und rückwärts, um die nächstgelegenen Schriftarten zu finden, die für die Zeichensätze verwendet wurden. Wenn für einen Zeichensatz keine Schriftart gefunden wird, verwendet Rich Edit die Schriftart, die vom Client für diesen Zeichensatz ausgewählt wurde. Wenn der Client keine Schriftart für den Zeichensatz angegeben hat, verwendet Rich Edit die Standardschriftart für diesen Zeichensatz. Wenn der Client eine andere Schriftart verwenden möchte, kann der Client sie jederzeit ändern, aber dieser Ansatz funktioniert in den meisten Fällen. Die aktuellen Standardschriftartoptionen basieren auf der folgenden Tabelle. Beachten Sie, dass die Standardschriftarten pro Prozess festgelegt werden, und es gibt separate Listen für die Benutzeroberflächenverwendung und für die Verwendung außerhalb der Benutzeroberfläche.



| Sprache                    | Schriftartname der Benutzeroberfläche  | Schriftgrad der Benutzeroberfläche | Nicht-UI-Schriftartname | Nicht-UI-Schriftgrad |
|-----------------------------|---------------|--------------|------------------|------------------|
| West, CE, ME, Western | Tahoma        | 8            | Arial            | 10               |
| Japanisch                    | MS UI-  | 9            | MS P.      | 10               |
| Koreanisch                      | Gulim         | 9            | Gulim            | 9                |
| Chinesisch (vereinfacht)          | Simsun        | 9            | SimSun           | 10               |
| Chinesisch (traditionell)         | PMingLiU      | 9            | PMingLiU         | 9                |
| Thailändisch                        | MS Sans Serif | 8            | Tahoma           | 14               |
| Symbole                     | Wingdings     | 8            | Wingdings        | 10               |
| Devanagari                  | Mangal        | 8            | Mangal           | 10               |
| Tamilisch                       | Latte         | 8            | Latte            | 10               |
| Geerbisch, Essisch          | Arial Unicode | 8            | Arial Unicode    | 10               |



 

Daher ermöglicht Rich Edit in der Standardtabelle für die Schriftartbindung (Einträge verfügen über einen Zeichensatz, einen Schriftartnamen und eine Größe), dass ANSI CHARSET mit mehreren Zeichensätzen übereinstimmen kann, während der entsprechende Zeichensatz 1:1 mit anderen Schriftarten übereinstimmen \_ kann. Genauer gesagt verwendet rich edit die ANSI \_ CHARSET-Auswahl, wenn keine andere Alternative gefunden wird. Sie können eine genauere Granularität als diese angeben. Weisen Sie z. B. ein bestimmtes ARABISCHES CHARSET für arabische Läufe, eine bestimmte schriftart für Griechisch und \_ so weiter zu. Diese Feingranularität wird auch verwendet, wenn eine Schriftart mit dem gewünschten Zeichensatzstempel an einer Stelle im Dokument vor dem Bereich gefunden wird, der an die Schriftart gebunden wird.

Beachten Sie, dass Rich Edit derzeit kein fehlendes Glyphen in einer Schriftart behandelt, die ansprüche, einen Zeichensatz zu unterstützen, aber unvollständig ist. Zur Anzeigezeit in einem komplexen Skript weiß Rich Edit am Ende, dass ein solches Glyphen fehlt, aber es führt nicht dazu, dass der Hintergrundspeicher eine neue Schriftart verwendet. Normalerweise wird dies durch die zugrunde liegende Schriftartverknüpfung des Betriebssystems erreicht.

## <a name="remarks"></a>Hinweise

**Rich Edit 4.1:** Um die Standardschriftart für ein Skript festzulegen, rufen Sie [**EM \_ SETCHARFORMAT**](em-setcharformat.md) mit [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)auf und geben Werte für die Member **yHeight,** **bCharSet,** **bPitchAndFamily,** **szFaceName** und **lcid** an. Rufen Sie außerdem [**EM \_ GETCHARFORMAT**](em-getcharformat.md) mit **CHARFORMAT2** auf, um die Standardschriftart für eine bestimmte Codepage zu erhalten, und geben Sie Werte für **die Member bCharSet** und **lcid** an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




