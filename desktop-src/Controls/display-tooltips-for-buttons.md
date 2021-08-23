---
title: Anzeigen von QuickInfos für Schaltflächen
description: Wenn Sie den TBSTYLE \_ TOOLTIPS-Stil angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement. Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleistenschaltfläche bewegen und dort etwa eine Sekunde lang belassen.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f169c6cc9324c98ed085b38f14802fcaa3c5cfbc8bd7ee9aa29af62ef41a6adc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320000"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Anzeigen von QuickInfos für Schaltflächen

Wenn Sie den [**TBSTYLE \_ TOOLTIPS-Stil**](toolbar-control-and-button-styles.md) angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement. Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleistenschaltfläche bewegen und dort etwa eine Sekunde lang belassen.

Ihre Anwendung kann text für das QuickInfo-Steuerelement auf eine der folgenden Arten bereitstellen:

-   Legen Sie den QuickInfo-Text als **iString-Member** der [**TBBUTTON-Struktur**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) für jede Schaltfläche fest. Sie müssen auch eine [**\_ TB SETMAXTEXTROWS-Nachricht**](tb-setmaxtextrows.md) senden und die maximale Textzeilen auf 0 festlegen, damit der Text nicht als Schaltflächenbezeichnung und nicht als QuickInfo angezeigt wird.
-   Erstellen Sie die Symbolleiste mit dem [**TBSTYLE \_ LIST-Stil,**](toolbar-control-and-button-styles.md) und legen Sie dann den erweiterten [**TBSTYLE EX \_ \_ MIXEDBUTTONS-Stil**](toolbar-extended-styles.md) fest. Bezeichnungen werden nur für Schaltflächen mit dem [**BTNS \_ SHOWTEXT-Stil**](toolbar-control-and-button-styles.md) angezeigt. Für Schaltflächen ohne diesen Stil wird eine QuickInfo angezeigt, die den Schaltflächentext enthält.
-   Reagieren Sie auf den [TTN \_ GETDISPINFO-Benachrichtigungscode.](ttn-getdispinfo.md)
-   Reagieren Sie auf den [ \_ TBN-GETINFOTIP-Benachrichtigungscode.](tbn-getinfotip.md)

Eine Anwendung, die Nachrichten direkt an das QuickInfo-Steuerelement senden muss, kann das Handle mithilfe der [**TB \_ GETTOOLTIPS-Nachricht**](tb-gettooltips.md) an das Steuerelement abrufen. Eine Anwendung kann das QuickInfo-Steuerelement einer Symbolleiste mithilfe der [**TB \_ SETTOOLTIPS-Nachricht**](tb-settooltips.md) durch ein anderes QuickInfo-Steuerelement ersetzen.

Die flexibelste Möglichkeit zum Bereitstellen von QuickInfo-Text besteht darin, auf den [TTN \_ GETDISPINFO-](ttn-getdispinfo.md) oder [TBN \_ GETINFOTIP-Benachrichtigungscode](tbn-getinfotip.md) zu reagieren, der vom Symbolleistensteuerelement in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) an das übergeordnete Element gesendet wird. Für [TTN \_ GETDISPINFO](ttn-getdispinfo.md)enthält der *lParam-Parameter* einen Zeiger auf eine [**NMTTDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) (auch als **LPTOOLTIPTEXT** definiert), die den Befehlsbezeichner der Schaltfläche angibt, für die Hilfetext erforderlich ist. Dieser Bezeichner befindet sich im **Element NMTTDISPINFO.hdr.idFrom.** Eine Anwendung kann den Hilfetext in die Struktur kopieren, die Adresse einer Zeichenfolge angeben, die den Hilfetext enthält, oder das Instanzhandle und den Ressourcenbezeichner einer Zeichenfolgenressource angeben.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="display-a-tooltip-for-a-button"></a>Anzeigen einer QuickInfo für eine Schaltfläche

Im folgenden Beispielcode wird der [TTN GETDISPINFO-QuickInfo-Benachrichtigungscode \_ ](ttn-getdispinfo.md) verarbeitet, indem Text aus Ressourcenbezeichnern angegeben wird.


```C++
case WM_NOTIFY: 
            
    switch (((LPNMHDR) lParam)->code) 
    {
    
    case TTN_GETDISPINFO: 
        { 
            LPTOOLTIPTEXT lpttt = (LPTOOLTIPTEXT)lParam; 
            
            // Set the instance of the module that contains the resource.
            lpttt->hinst = g_hInst; 
            
            UINT_PTR idButton = lpttt->hdr.idFrom;
            
            switch (idButton) 
            { 
            case IDM_NEW: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_NEW); 
                break; 
                
            case IDM_OPEN: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_OPEN); 
                break; 
                
            case IDM_SAVE: 
                lpttt->lpszText = MAKEINTRESOURCE(IDS_TIPS_SAVE); 
                break; 
            } 
            
            break; 
        } 
    }
    return TRUE;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Symbolleistensteuerelementen](using-toolbar-controls.md)
</dt> <dt>

[Demo zu Windows allgemeinen Steuerelementen (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




