---
title: Formatieren von Text in Rich Edit-Steuerelementen
description: Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen.
ms.assetid: 19A4F0D1-88C5-407D-A70F-CB486DAD352E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246c6309dec94538f47ed9ca7e464f1d6d17f240
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724284"
---
# <a name="how-to-format-text-in-rich-edit-controls"></a>Formatieren von Text in Rich Edit-Steuerelementen

Eine Anwendung kann Nachrichten an ein Rich Edit-Steuerelement senden, um Zeichen und Absätze zu formatieren und Formatierungsinformationen abzurufen. Die Attribute für die Absatz Formatierung umfassen Ausrichtung, Tabstopps, Einzüge, Nummerierungen und einfache Tabellen. Für Zeichen können Sie Schriftart Name, Größe, Farbe und Effekte angeben, z. b. Fett, kursiv und geschützt.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="format-text-in-a-rich-edit-control"></a>Formatieren von Text in einem Rich-Edit-Steuerelement

Sie können die Absatz Formatierung mithilfe der [**EM- \_ SetParaFormat**](em-setparaformat.md) -Meldung anwenden. Um die aktuelle Absatz Formatierung für den ausgewählten Text zu ermitteln, verwenden Sie die [**EM \_ GetParaFormat**](em-getparaformat.md) -Nachricht. Die [**paraformat**](/windows/desktop/api/Richedit/ns-richedit-paraformat) -oder [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) -Struktur wird mit beiden Nachrichten verwendet, um Absatz Formatierungs Attribute anzugeben.

Sie können die Zeichen Formatierung mithilfe der [**EM- \_ setcharformat**](em-setcharformat.md) -Meldung anwenden. Zum Bestimmen der aktuellen Zeichen Formatierung für den ausgewählten Text können Sie die [**EM \_ getcharformat**](em-getcharformat.md) -Meldung verwenden. Die [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) -oder [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) -Struktur wird mit beiden Nachrichten zum Angeben von Zeichen Attributen verwendet.

Sie können auch die Nachrichten [**EM \_ setcharformat**](em-setcharformat.md) und [**EM \_ getcharformat**](em-getcharformat.md) verwenden, um die Zeichen Formatierung der Einfügemarke festzulegen und abzurufen. Hierbei handelt es sich um die Formatierung, die auf alle nachträglich eingefügten Zeichen angewendet wird. Wenn eine Anwendung z. b. die Standard Zeichenformatierung auf "Fett" festlegt und der Benutzer dann ein Zeichen eingibt, ist dieses Zeichen fett formatiert.

Die Zeichen Formatierung der Einfügemarke wird nur dann auf den neu eingefügten Text angewendet, wenn die aktuelle Auswahl leer ist (wenn die aktuelle Auswahl eine Einfügemarke ist). Andernfalls geht der neue Text von der Zeichen Formatierung des Texts aus, den er ersetzt. Wenn sich die Auswahl ändert, ändert sich die Standard Zeichen Formatierung so, dass Sie dem ersten Zeichen in der neuen Auswahl entspricht.

Der geschützte Zeichen Effekt ist insofern eindeutig, als er die Darstellung von Text nicht ändert. Wenn der Benutzer versucht, geschützten Text zu ändern, sendet ein Rich Edit-Steuerelement sein übergeordnetes Fenster an den [ \_ geschützten](en-protected.md) Benachrichtigungs Code, sodass das übergeordnete Fenster die Änderung zulassen oder verhindern kann. Zum Empfangen dieses Benachrichtigungs Codes müssen Sie ihn mithilfe der Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) aktivieren.

Die Vordergrundfarbe ist immer ein Zeichen Attribut. In Microsoft Rich Edit 1,0 ist die Hintergrundfarbe nur eine Eigenschaft des Rich Edit-Steuer Elements. Um die Standard Hintergrundfarbe festzulegen, verwenden Sie die Nachricht [**EM \_ setbkgndcolor**](em-setbkgndcolor.md) . Beachten Sie, dass Rich Edit die " [**WM \_ ctlcoloredit**](wm-ctlcoloredit.md) "-Meldung nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




