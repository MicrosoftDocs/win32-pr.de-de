---
title: Verarbeiten von Benachrichtigungs Meldungen
description: Ein Eigenschaften Blatt sendet WM \_ -Benachrichtigungs Meldungen, um Informationen von den Seiten abzurufen und die Seiten mit Benutzeraktionen zu benachrichtigen.
ms.assetid: 82768E43-97BA-451A-9373-D5B8FD06ABED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c544910e44e0c865e738427285d7488147b9c1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103724276"
---
# <a name="how-to-process-notification-messages"></a>Verarbeiten von Benachrichtigungs Meldungen

Ein Eigenschaften Blatt sendet [**WM- \_ Benachrichtigungs**](wm-notify.md) Meldungen, um Informationen von den Seiten abzurufen und die Seiten mit Benutzeraktionen zu benachrichtigen.

Der *LPARAM* -Parameter der Nachricht ist die Adresse einer [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur, die das Handle für das Eigenschaften Blatt-Dialogfeld, das Handle für das Dialogfeld der Seite und einen Benachrichtigungs Code enthält. Die Seite muss auf einige Benachrichtigungs Meldungen reagieren, indem der DWL- \_ msgresult-Wert der Seite auf " **true** " oder " **false**" festgelegt wird.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="process-notification-messages"></a>Verarbeiten von Benachrichtigungs Meldungen

Das folgende Beispiel ist ein Code Fragment aus der Dialogfeld Prozedur für eine Seite. Es zeigt, wie der [PSN- \_ Hilfe](psn-help.md) -Benachrichtigungs Code verarbeitet wird.


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

[Verwenden von Eigenschaften Blättern](using-property-sheets.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




