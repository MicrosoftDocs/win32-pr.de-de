---
title: So verwenden Sie Rich-Edit-Zwischenablage Vorgänge
description: Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949163"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>So verwenden Sie Rich-Edit-Zwischenablage Vorgänge

Eine Anwendung kann den Inhalt der Zwischenablage in ein Rich-Edit-Steuerelement einfügen, indem Sie entweder das beste verfügbare Zwischenablage Format oder ein bestimmtes Zwischenablage Format verwendet. Sie können auch bestimmen, ob ein Rich-Edit-Steuerelement in der Lage ist, ein Zwischenablage Format einzufügen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-clipboard-operation"></a>Verwenden eines Rich-Edit-Zwischenablage Vorgangs

Wie bei einem Bearbeitungs Steuerelement können Sie den Inhalt der aktuellen Auswahl mithilfe der [**WM- \_ Kopier**](/windows/desktop/dataxchg/wm-copy) -oder der WM- [**\_ Ausschneide**](/windows/desktop/dataxchg/wm-cut) Nachricht kopieren oder Ausschneiden. Auf ähnliche Weise können Sie den Inhalt der Zwischenablage mithilfe der [**WM- \_ Einfüge**](/windows/desktop/dataxchg/wm-paste) Nachricht in ein Rich-Edit-Steuerelement einfügen. Das Steuerelement fügt das erste verfügbare Format, das es erkennt, ein, das vermutlich das beschreibende Format darstellt.

Wenn Sie ein bestimmtes Zwischenablage Format einfügen möchten, können Sie die " [**EM \_ PasteSpecial**](em-pastespecial.md) "-Meldung verwenden. Diese Meldung ist nützlich für Anwendungen mit einem **speziellen** Befehl zum Einfügen, mit dem Benutzer das Zwischenablage Format auswählen können. Sie können die [**EM \_ CanPaste**](em-canpaste.md) -Nachricht verwenden, um zu bestimmen, ob ein bestimmtes Format vom Steuerelement erkannt wird.

Sie können auch die [**EM \_ CanPaste**](em-canpaste.md) -Nachricht verwenden, um zu bestimmen, ob ein verfügbares Zwischenablage Format von einem Rich Edit-Steuerelement erkannt wird. Diese Meldung ist nützlich, wenn die " [**WM \_ initmenupopup**](/windows/desktop/menurc/wm-initmenupopup) "-Meldung verarbeitet wird. Eine Anwendung kann den **Einfüge** Befehl in Abhängigkeit davon aktivieren oder grauen, ob das Steuerelement ein beliebiges verfügbares Format einfügen kann.

Rich Edit-Steuerelemente registrieren zwei Zwischenablage Formate:

-   Rich Text Format
-   Rich-Text-Format ohne Objekte
-   RichEdit-Text und-Objekte

Eine Anwendung kann diese Formate mithilfe der [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) -Funktion registrieren und die Werte für die Werte "CF \_ RTF", "CF \_ RTF noobjs" und "CF \_ retextobj" angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 