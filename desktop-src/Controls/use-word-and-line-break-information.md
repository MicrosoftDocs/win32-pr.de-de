---
title: Verwenden von Wort-und Zeilenumbruch Informationen
description: Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wort Umbruch Prozedur bezeichnet wird, um Unterbrechungen zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb90064e455bfeb8ee126e6107d75ef29b3a4f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340287"
---
# <a name="how-to-use-word-and-line-break-information"></a>Verwenden von Wort-und Zeilenumbruch Informationen

Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wort Umbruch Prozedur bezeichnet wird, um Unterbrechungen zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können Das-Steuerelement verwendet diese Informationen beim Ausführen von Zeilenumbruch Vorgängen und bei der Verarbeitung von STRG + nach-links-Pfeiltaste und STRG + nach-rechts-Taste. Eine Anwendung kann Nachrichten an ein Rich-Edit-Steuerelement senden, um die Standardprozedur für das Wort Umbruch zu ersetzen, Informationen zum Wort Umbruch abzurufen und zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-word-and-line-break-information"></a>Verwenden von Wort-und Zeilenumbruch Informationen

Wörter Trennungs Prozeduren für Rich Edit-Steuerelemente ähneln denen für Bearbeitungs Steuerelemente, verfügen jedoch über zusätzliche Funktionen: Wörter Trennungs Prozeduren für beide Arten von Steuerelementen können bestimmen, ob ein Zeichen ein Trennzeichen ist, und das nächste Wörter Umbruch vor oder nach der angegebenen Position finden. Ein Trennzeichen ist ein Zeichen, das das Ende eines Worts markiert, z. b. ein Leerzeichen. In der Regel tritt ein Wort Umbruch in einem Bearbeitungs Steuerelement nur nach Trennzeichen auf. Allerdings gelten für die meisten asiatischen Sprachen unterschiedliche Regeln.

Wörter Trennungs Prozeduren für Rich Edit-Steuerelemente gruppieren auch Zeichen in Zeichenklassen, die jeweils durch einen Wert im Bereich von 0x00 bis 0x0f identifiziert werden. Unterbrechungen treten entweder nach Trennzeichen oder zwischen Zeichen verschiedener Klassen auf. Folglich findet eine Prozedur zum Umbrechen mit unterschiedlichen Klassen für alphanumerische Zeichen und Interpunktions Zeichen zwei Wort Umbrüche in der Zeichenfolge "Win.doc" (vor und nach dem Zeitraum).

Die Klasse eines Zeichens kann mit 0 (null) oder mehreren Flag zum Abbrechen von Wörtern kombiniert werden, um einen 8-Bit-Wert zu bilden. Beim Ausführen von Zeilenumbruch Vorgängen verwendet ein Rich-Edit-Steuerelement Wort Umbruch Flags, um zu bestimmen, wo es Zeilen unterbrechen kann. Rich Edit verwendet die folgenden Flags für die Wort Umbruch.



| Flag            | Beschreibung                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF- \_ BreakAfter | Zeilen können nach dem-Zeichen getrennt werden.                                                                                          |
| WBF-halte \_ Linie  | Das Zeichen ist ein Trennzeichen. Trennzeichen markieren die Enden von Wörtern. Zeilen können nach Trennzeichen getrennt werden.                            |
| WBF \_ iswhite    | Das Zeichen ist ein Leerzeichen. Nachfolgende Leerzeichen sind beim umwickeln nicht in der Länge einer Zeile enthalten. |



 

Der WBF \_ BreakAfter-Wert wird verwendet, um das umschließen nach einem Zeichen zuzulassen, das das Ende eines Worts nicht markiert, z. b. ein Bindestrich.

Sie können die standardmäßige Wort Umbruch Prozedur für ein Rich Edit-Steuerelement durch ihre eigene Prozedur ersetzen, indem Sie die Nachricht " [**EM \_ setwordbreakproc**](em-setwordbreakproc.md) " verwenden. Weitere Informationen zu Word-Break-Prozeduren finden Sie in der Beschreibung der [*editwordbreakproc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) -Funktion.

> [!Note]  
> Diese Ersetzung wird für Microsoft Rich Edit 2,0 und höher aufgrund der Komplexität der mehrsprachigen Wörter Trennung nicht empfohlen.

 

Für Microsoft Rich Edit 1,0 können Sie die EM- [**\_ setwordbreakprocex**](em-setwordbreakprocex.md) -Nachricht verwenden, um die Standardprozedur für erweiterte Wörter Umbrüche durch eine [*editwordbreakprocex*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) -Funktion zu ersetzen. Diese Funktion stellt zusätzliche Informationen über den Text bereit, z. b. den Zeichensatz. Sie können die [**EM \_ getwordbreakprocex**](em-getwordbreakprocex.md) -Nachricht verwenden, um die Adresse des aktuellen erweiterten Wort Umbruch Verfahrens abzurufen. Beachten Sie, dass Microsoft Rich Edit 2,0 und höher " *editwordbreakprocex*", " **EM \_ getwordbreakprocex**" und " **EM \_ setwordbreakprocex**" nicht unterstützt.

Sie können die Nachricht [**EM \_ findwordbreak**](em-findwordbreak.md) verwenden, um Wort Umbrüche zu suchen oder um die Klassen-und Wort Umbruch Flags eines Zeichens zu ermitteln. Das Steuerelement ruft wiederum seine Wort Umbruch Prozedur auf, um die angeforderten Informationen zu erhalten.

Zum Ermitteln der Zeile, auf die ein bestimmtes Zeichen fällt, können Sie die [**EM \_ exlinefromchar**](em-exlinefromchar.md) -Nachricht verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 