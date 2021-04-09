---
title: Anzeigen von Quick Infos für Schaltflächen
description: Wenn Sie den tbstyle- \_ Tooltips-Stil angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement. Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleisten Schaltfläche bewegen und diese für ungefähr eine Sekunde belassen.
ms.assetid: 0383DB63-A10E-4235-A974-AB21551E086B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb37de7c21c904673a1f656533497130d50bd8f7
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "103858103"
---
# <a name="how-to-display-tooltips-for-buttons"></a>Anzeigen von Quick Infos für Schaltflächen

Wenn Sie den [**tbstyle- \_ Tooltips**](toolbar-control-and-button-styles.md) -Stil angeben, erstellt und verwaltet die Symbolleiste ein QuickInfo-Steuerelement. Das QuickInfo-Steuerelement ist ausgeblendet und wird nur angezeigt, wenn Benutzer den Mauszeiger über eine Symbolleisten Schaltfläche bewegen und diese für ungefähr eine Sekunde belassen.

Die Anwendung kann Text für das QuickInfo-Steuerelement mit einer der folgenden Methoden bereitstellen:

-   Legen Sie den QuickInfo-Text für jede Schaltfläche als **IString** -Member der [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) -Struktur fest. Außerdem müssen Sie eine [**TB- \_ setmaxtextrows**](tb-setmaxtextrows.md) -Nachricht senden und die maximalen Textzeilen auf 0 festlegen, sodass der Text nicht als Schaltflächen Bezeichnung und nicht als QuickInfo angezeigt wird.
-   Erstellen Sie die Symbolleiste mit dem [**tbstyle- \_ Listen**](toolbar-control-and-button-styles.md) Stil, und legen Sie dann den erweiterten Stil [**tbstyle \_ Ex \_ mixedbuttons**](toolbar-extended-styles.md) fest. Bezeichnungen werden nur für Schaltflächen mit dem [**btns- \_ ShowText**](toolbar-control-and-button-styles.md) -Stil angezeigt. Für Schaltflächen, die nicht über diesen Stil verfügen, wird eine QuickInfo angezeigt, die den Schaltflächen Text enthält.
-   Reagieren Sie auf den [TTN \_ getdispinfo](ttn-getdispinfo.md) -Benachrichtigungs Code.
-   Reagieren Sie auf den [TBN- \_ getinfotip](tbn-getinfotip.md) -Benachrichtigungs Code.

Eine Anwendung, die Nachrichten direkt an das ToolTip-Steuerelement senden muss, kann das Handle für das Steuerelement abrufen, indem die [**TB \_ gettooltips**](tb-gettooltips.md) -Nachricht verwendet wird. Eine Anwendung kann das ToolTip-Steuerelement einer Symbolleiste durch ein anderes QuickInfo-Steuerelement ersetzen, indem die [**TB- \_ SetToolTips**](tb-settooltips.md) -Nachricht verwendet wird

Die flexibelste Möglichkeit zum Bereitstellen von QuickInfo-Text ist die Reaktion auf den [TTN \_ getdispinfo](ttn-getdispinfo.md) -oder [TBN \_ getinfotip](tbn-getinfotip.md) -Benachrichtigungs Code, der vom Symbolleisten-Steuerelement in Form einer WM-Benachrichtigungs Meldung gesendet wird. [**\_**](wm-notify.md) Für [TTN \_ getdispinfo](ttn-getdispinfo.md)enthält der *LPARAM* -Parameter einen Zeiger auf eine [**nmttdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) -Struktur (auch als **lptooltiptext** definiert), die den Befehls Bezeichner der Schaltfläche angibt, für die Hilfetext benötigt wird. Dieser Bezeichner befindet sich im Member **nmttdispinfo. HDR. idfrom** . Eine Anwendung kann den Hilfetext in die Struktur kopieren, die Adresse einer Zeichenfolge angeben, die den Hilfetext enthält, oder den Instanzhandle und den Ressourcen Bezeichner einer Zeichen folgen Ressource angeben.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="display-a-tooltip-for-a-button"></a>Anzeigen einer QuickInfo für eine Schaltfläche

Der folgende Beispielcode behandelt den [TTN \_ getdispinfo-QuickInfo](ttn-getdispinfo.md) -Benachrichtigungs Code durch Bereitstellen von Text von Ressourcen bezeichtern.


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

[Verwenden von Symbolleisten](using-toolbar-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




