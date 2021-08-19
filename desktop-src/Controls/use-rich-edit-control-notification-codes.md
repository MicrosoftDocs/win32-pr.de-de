---
title: Verwenden von Rich Edit-Steuerelement-Benachrichtigungscodes
description: Das übergeordnete Fenster eines Rich-Edit-Steuerelements kann Benachrichtigungscodes verarbeiten, um Ereignisse zu überwachen, die sich auf das Steuerelement auswirken. Umfangreiche Bearbeitungssteuerelemente unterstützen alle Benachrichtigungscodes, die mit Bearbeitungssteuerelementen verwendet werden, sowie mehrere zusätzliche.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6bc730c648e76137db480f14895d540a9142ae6a80ffa58533e38ef513653ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828633"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Verwenden von Rich Edit-Steuerelement-Benachrichtigungscodes

Das übergeordnete Fenster eines Rich-Edit-Steuerelements kann Benachrichtigungscodes verarbeiten, um Ereignisse zu überwachen, die sich auf das Steuerelement auswirken. Umfangreiche Bearbeitungssteuerelemente unterstützen alle Benachrichtigungscodes, die mit Bearbeitungssteuerelementen verwendet werden, sowie mehrere zusätzliche.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="use-a-rich-edit-control-notification-code"></a>Verwenden eines Rich Edit-Steuerelementbenachrichtigungscodes

Sie können bestimmen, welche Benachrichtigungscodes ein Rich-Edit-Steuerelement an das übergeordnete Fenster sendet, indem Sie dessen Ereignismaske festlegen. Verwenden Sie die EM [**\_ SETEVENTMASK-Meldung,**](em-seteventmask.md) um die Ereignismaske für ein umfassendes Bearbeitungssteuer steuerelement fest zu legen. Sie können die aktuelle Ereignismaske für ein rich edit-Steuerelement mithilfe der [**EM \_ GETEVENTMASK-Nachricht**](em-geteventmask.md) abrufen. Eine Liste der Ereignismaskenflags finden Sie unter [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).

Das übergeordnete Fenster eines Rich-Edit-Steuerelements kann alle Tastatur- und Mauseingaben für das Steuerelement filtern, indem der [EN \_ MSGFILTER-Benachrichtigungscode](en-msgfilter.md) verarbeitet wird. Das übergeordnete Fenster kann die Verarbeitung der Tastatur- oder Mausnachricht verhindern oder die Nachricht ändern, indem die angegebene [**MSGFILTER-Struktur geändert**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) wird.

Eine Anwendung kann den [EN \_ PROTECTED-Benachrichtigungscode](en-protected.md) verarbeiten, um zu erkennen, wann der Benutzer versucht, geschützten Text zu ändern. Um einen Textbereich als geschützt zu markieren, können Sie den Effekt für geschützte Zeichen festlegen.

Sie können es dem Benutzer ermöglichen, Dateien in einem Rich-Edit-Steuerelement zu löschen, indem Sie den [EN \_ DROPFILES-Benachrichtigungscode](en-dropfiles.md) verarbeiten. Die angegebene [**ENDROPFILES-Struktur**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) enthält Informationen zu den Dateien, die gelöscht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Rich Edit-Steuerelementen](using-rich-edit-controls.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




