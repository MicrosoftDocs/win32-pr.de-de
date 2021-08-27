---
title: Verwenden von Rich Edit-Zwischenablagevorgängen
description: Eine Anwendung kann den Inhalt der Zwischenablage mithilfe des besten verfügbaren Zwischenablageformats oder eines bestimmten Zwischenablageformats in ein rich-Edit-Steuerelement einfügen.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdeac2e892716880e4e2971d597c13047dc79cebf2c57888e2fa248c6b0c4beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132090"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Verwenden von Rich Edit-Zwischenablagevorgängen

Eine Anwendung kann den Inhalt der Zwischenablage mithilfe des besten verfügbaren Zwischenablageformats oder eines bestimmten Zwischenablageformats in ein rich-Edit-Steuerelement einfügen. Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement ein Zwischenablageformat eingefügt werden kann.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-clipboard-operation"></a>Verwenden eines Rich-Edit-Zwischenablage-Vorgangs

Wie bei einem Bearbeitungssteuer steuerelement können Sie den Inhalt der aktuellen Auswahl mithilfe der [**WM \_ COPY-**](/windows/desktop/dataxchg/wm-copy) oder [**WM \_ CUT-Meldung kopieren oder ausschneiden.**](/windows/desktop/dataxchg/wm-cut) Auf ähnliche Weise können Sie den Inhalt der Zwischenablage mithilfe der WM-Paste-Meldung in ein [**\_ rich-Edit-Steuerelement**](/windows/desktop/dataxchg/wm-paste) einfügen. Das Steuerelement gibt das erste verfügbare Format ein, das es erkennt, was vermutlich das aussagekräftigste Format ist.

Zum Einfügen eines bestimmten Zwischenablageformats können Sie die [**Meldung EM \_ PASTESPECIAL**](em-pastespecial.md) verwenden. Diese Meldung ist nützlich für Anwendungen mit dem **Befehl "Paste Special",** mit dem der Benutzer das Zwischenablageformat auswählen kann. Sie können die [**EM \_ CANPASTE-Nachricht verwenden,**](em-canpaste.md) um zu bestimmen, ob ein bestimmtes Format vom Steuerelement erkannt wird.

Sie können auch die [**EM \_ CANPASTE-Meldung verwenden,**](em-canpaste.md) um zu bestimmen, ob ein verfügbares Zwischenablageformat von einem Rich-Edit-Steuerelement erkannt wird. Diese Meldung ist nützlich, wenn die [**WM \_ INITMENUPOPUP-Nachricht verarbeitet**](/windows/desktop/menurc/wm-initmenupopup) wird. Eine Anwendung kann den  Befehl Einfügen aktivieren oder grau halten, je nachdem, ob das Steuerelement ein beliebiges verfügbares Format einfügen kann.

Umfangreiche Bearbeitungssteuerelemente registrieren zwei Zwischenablageformate:

-   Rich Text Format
-   Rich-Text-Format ohne Objekte
-   RichEdit-Text und -Objekte

Eine Anwendung kann diese Formate mithilfe der [**RegisterClipboardFormat-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) registrieren und dabei die Werte CF \_ RTF, CF \_ RTFNOOBJS und CF \_ RETEXTOBJ angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 