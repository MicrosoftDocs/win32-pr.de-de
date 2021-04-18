---
title: Verwenden von Syslink-Benachrichtigungen
description: Dem Syslink-Steuerelement \ 8212 sind zwei Benachrichtigungs Meldungen zugeordnet, eine für die Maus (nm \_ Click (Syslink)) und eine für die Tastatur (nm \_ Return).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "106338448"
---
# <a name="how-to-use-syslink-notifications"></a>Verwenden von Syslink-Benachrichtigungen

Dem Syslink-Steuerelement sind zwei Benachrichtigungs Meldungen zugeordnet – eine für die Maus ([nm \_ Click (Syslink)](nm-click-syslink.md)) und eine für die Tastatur ([nm \_ Return](nm-return.md)).

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="use-syslink-notifications"></a>Verwenden von Syslink-Benachrichtigungen

Der folgende Beispielcode zeigt, wie die Syslink-Benachrichtigungen verarbeitet werden, die generiert werden, wenn der Benutzer auf einen der beiden Links im [vorherigen Beispiel](create-syslink-controls.md)klickt. Wenn der Benutzer auf die Internet-URL klickt, wird die zugehörige Webseite im Standardbrowser geöffnet. Wenn der Benutzer auf den von der Anwendung definierten Hyperlink klickt, wird ein Meldungs Feld angezeigt.


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Syslink-Steuerelementen](using-syslink-controls.md)
</dt> <dt>

[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




