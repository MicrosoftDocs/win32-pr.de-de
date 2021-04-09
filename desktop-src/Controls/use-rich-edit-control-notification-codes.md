---
title: Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente
description: Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103948531"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Verwenden von Benachrichtigungs Codes für Rich-Edit-Steuerelemente

Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann Benachrichtigungs Codes verarbeiten, um Ereignisse zu überwachen, die das Steuerelement Rich Edit-Steuerelemente unterstützen alle Benachrichtigungs Codes, die mit Bearbeitungs Steuerelementen verwendet werden, sowie mehrere zusätzliche.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-control-notification-code"></a>Verwenden eines Rich-Edit-Steuerelement-Benachrichtigungs Codes

Sie können bestimmen, welche Benachrichtigungs Codes von einem Rich Edit-Steuerelement durch Festlegen seiner Ereignis Maske an das übergeordnete Fenster gesendet werden. Um die Ereignis Maske für ein Rich-Edit-Steuerelement festzulegen, verwenden Sie die Nachricht [**EM \_ SetEventMask**](em-seteventmask.md) . Sie können die aktuelle Ereignis Maske für ein Rich Edit-Steuerelement mithilfe der [**EM \_ GetEventMask**](em-geteventmask.md) -Nachricht abrufen. Eine Liste der Ereignismasken-Flags finden Sie unter [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).

Das übergeordnete Fenster eines Rich-Edit-Steuer Elements kann alle Tastatur-und Maus Eingaben für das Steuerelement filtern, indem der [en \_ msgfilter](en-msgfilter.md) -Benachrichtigungs Code verarbeitet wird Das übergeordnete Fenster kann die Verarbeitung der Tastatur-oder Maus Meldung verhindern oder die Meldung ändern, indem die angegebene [**msgfilter**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) -Struktur geändert wird.

Eine Anwendung kann den von [en \_ geschützten](en-protected.md) Benachrichtigungs Code verarbeiten, um zu erkennen, wann der Benutzer versucht, geschützten Text zu ändern. Um einen Textbereich als geschützt zu markieren, können Sie den Effekt geschützter Zeichen festlegen.

Sie können es Benutzern ermöglichen, Dateien in einem Rich-Edit-Steuerelement zu löschen, indem Sie den [en \_ dropfiles](en-dropfiles.md) -Benachrichtigungs Code verarbeiten. Die angegebene [**endropfiles**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) -Struktur enthält Informationen zu den Dateien, die gelöscht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




