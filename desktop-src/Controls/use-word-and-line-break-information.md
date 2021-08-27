---
title: Verwenden von Word- und Zeilenunterbrechungsinformationen
description: Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wörterumbruchprozedur bezeichnet wird, um Brüche zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können.
ms.assetid: DDCE9814-0D39-494C-953A-FB6A98100EEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178770ce4a7206c18f6fbbc197d92e23ff0139ae637bd5f7ceb4159aee3270ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059690"
---
# <a name="how-to-use-word-and-line-break-information"></a>Verwenden von Word- und Zeilenunterbrechungsinformationen

Ein Rich-Edit-Steuerelement ruft eine Funktion auf, die als Wörterumbruchprozedur bezeichnet wird, um Brüche zwischen Wörtern zu finden und zu bestimmen, wo Zeilen unterbrochen werden können. Das Steuerelement verwendet diese Informationen beim Ausführen von Zeilenumbruchvorgängen und bei der Verarbeitung von TASTENKOMBINATIONEN MIT STRG+NACH-LINKS-TASTE und STRG+NACH-RECHTS-TASTE. Eine Anwendung kann Nachrichten an ein Rich-Edit-Steuerelement senden, um die Standardprozedur für die Wörterunterbrechung zu ersetzen, Informationen zur Wortunterbrechung abzurufen und zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-word-and-line-break-information"></a>Verwenden von Word- und Zeilenunterbrechungsinformationen

Wörterbruchproz amp;#160;B. -Prozeduren für Rich-Edit-Steuerelemente ähneln denen für Bearbeitungssteuerelemente, verfügen aber über zusätzliche Funktionen: Wörterbruchproz amp;#160;-Prozeduren für beide Arten von Steuerelementen können bestimmen, ob ein Zeichen ein Trennzeichen ist und die nächste Wortunterbrechung vor oder nach der angegebenen Position finden kann. Ein Trennzeichen ist ein Zeichen, das das Ende eines Worts markiert, z. B. ein Leerzeichen. In der Regel tritt in einem Bearbeitungssteuerelement ein Wörterbruch nur nach Trennzeichen auf. Für die meisten sprachen asienisch gelten jedoch unterschiedliche Regeln.

Wordbreak-Prozeduren für Rich-Edit-Steuerelemente gruppieren Zeichen auch in Zeichenklassen, die jeweils durch einen Wert im Bereich identifiziert werden, der über 0x0F 0x00. Unterbrechungen treten entweder nach Trennzeichen oder zwischen Zeichen verschiedener Klassen auf. Daher würde eine Wörterumbruchprozedur mit verschiedenen Klassen für alphanumerische Zeichen und Interpunktionszeichen zwei Wortumbrüche in der Zeichenfolge "Win.doc" (vor und nach dem Punkt) finden.

Die Klasse eines Zeichens kann mit null oder mehr Wörterbruchflags kombiniert werden, um einen 8-Bit-Wert zu bilden. Beim Ausführen von Zeilenumbruchvorgängen verwendet ein Rich-Edit-Steuerelement Wörterumbruchflags, um zu bestimmen, wo Zeilen umbrochen werden können. Rich Edit verwendet die folgenden Wörterbruchflags.



| Flag            | Beschreibung                                                                                                                       |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| WBF \_ BREAKAFTER | Zeilen können nach dem Zeichen unterbrochen werden.                                                                                          |
| WBF \_ BREAKLINE  | Das Zeichen ist ein Trennzeichen. Trennzeichen markieren die Enden von Wörtern. Zeilen können nach Trennzeichen unterbrochen werden.                            |
| WBF \_ ISWHITE    | Das Zeichen ist ein Leerzeichen. Nachfolgende Leerzeichen sind beim Umschließen nicht in der Länge einer Zeile enthalten. |



 

Der WBF \_ BREAKAFTER-Wert wird verwendet, um das Umschließen nach einem Zeichen zu ermöglichen, das das Ende eines Worts nicht markiert, z. B. einen Bindestrich.

Mithilfe der [**EM \_ SETWORDBREAKPROC-Meldung**](em-setwordbreakproc.md) können Sie die Standardprozedur zur Wörterunterbrechung für ein Rich-Edit-Steuerelement durch Ihre eigene Prozedur ersetzen. Weitere Informationen zu Wörterunterbrechungsverfahren finden Sie in der Beschreibung der [*EditWordBreakProc-Funktion.*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)

> [!Note]  
> Diese Ersetzung wird für Microsoft Rich Edit 2.0 und höher aufgrund der Komplexität des Mehrsprachigen Wortbruchs nicht empfohlen.

 

Für Microsoft Rich Edit 1.0 können Sie die [**EM \_ SETWORDBREAKPROCEX-Meldung**](em-setwordbreakprocex.md) verwenden, um die erweiterte Standardprozedur zur Wörterunterbrechung durch eine [*EditWordBreakProcEx-Funktion*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) zu ersetzen. Diese Funktion stellt zusätzliche Informationen zum Text bereit, z. B. den Zeichensatz. Sie können die [**EM \_ GETWORDBREAKPROCEX-Nachricht**](em-getwordbreakprocex.md) verwenden, um die Adresse der aktuellen erweiterten Wörterpausenprozedur abzurufen. Beachten Sie, dass Microsoft Rich Edit 2.0 und höher *EditWordBreakProcEx,* **EM \_ GETWORDBREAKPROCEX** und **EM \_ SETWORDBREAKPROCEX** nicht unterstützen.

Sie können die [**EM \_ FINDWORDBREAK-Nachricht**](em-findwordbreak.md) verwenden, um Wörterumbrüche zu finden oder die Klassen- und Wörterumbruchflags eines Zeichens zu bestimmen. Im Gegenzug ruft das Steuerelement seine Wörterumbruchprozedur auf, um die angeforderten Informationen abzurufen.

Um zu bestimmen, auf welche Zeile ein bestimmtes Zeichen fällt, können Sie die [**EM \_ EXLINEFROMCHAR-Nachricht**](em-exlinefromchar.md) verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 