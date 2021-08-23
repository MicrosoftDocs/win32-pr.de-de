---
title: Verarbeiten von Benachrichtigungsmeldungen
description: Ein Eigenschaftenblatt sendet WM NOTIFY-Meldungen, um Informationen von den Seiten abzurufen und die Seiten über \_ Benutzeraktionen zu benachrichtigen.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baf0c58fdbcbe5378dd46e828a2d29a7c91832174c9564660a82c5ab70997a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575480"
---
# <a name="how-to-process-notification-messages"></a>Verarbeiten von Benachrichtigungsmeldungen

Ein Eigenschaftenblatt sendet [**WM \_ NOTIFY-Meldungen,**](wm-notify.md) um Informationen von den Seiten abzurufen und die Seiten über Benutzeraktionen zu benachrichtigen.

Der *lParam-Parameter* der Nachricht ist die Adresse einer [**NMHDR-Struktur,**](/windows/desktop/api/richedit/ns-richedit-nmhdr) die das Handle für das Eigenschaftenblattdialogfeld, das Handle für das Seitendialogfeld und einen Benachrichtigungscode enthält. Die Seite muss auf einige Benachrichtigungsmeldungen reagieren, indem der DWL MSGRESULT-Wert der Seite entweder auf TRUE oder \_ **FALSE festgelegt wird.** 

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="process-notification-messages"></a>Verarbeiten von Benachrichtigungsmeldungen

Das folgende Beispiel ist ein Codefragment aus der Dialogfeldprozedur für eine Seite. Es wird gezeigt, wie sie den [PSN \_ HELP-Benachrichtigungscode](psn-help.md) verarbeiten.


```C++
case WM_NOTIFY:

    switch (((NMHDR FAR *) lParam)->code) 
    {
    case PSN_HELP:
        {
         
        char szBuf[FILE_LEN]; // Buffer for name of Help file

        // Display Help for the font properties page.
        LoadString(g_hinst, IDS_HELPFILE, &szBuf, sizeof(szBuf)/sizeof(szBuf[0]));
        WinHelp(((NMHDR FAR *)lParam)->hwndFrom, &szBuf, HELP_CONTEXT, IDH_FONT_PROPERTIES);                
        
        break;
        
         }
         
        // Process other property sheet notifications here.
    }
    
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaftenblättern](using-property-sheets.md)
</dt> <dt>

[Windows demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




