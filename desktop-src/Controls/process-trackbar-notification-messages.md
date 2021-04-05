---
title: Verarbeiten von TrackBar-Benachrichtigungs Meldungen
description: Trackbars Benachrichtigen das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine WM \_ HScroll-oder WM- \_ VScroll-Nachricht sendet.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709006"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Verarbeiten von TrackBar-Benachrichtigungs Meldungen

Trackbars Benachrichtigen das übergeordnete Fenster von Benutzeraktionen, indem das übergeordnete Element eine [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht sendet.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="process-trackbar-notification-messages"></a>Verarbeiten von TrackBar-Benachrichtigungs Meldungen

Das folgende Codebeispiel ist eine Funktion, die aufgerufen wird, wenn das übergeordnete Fenster der TrackBar eine [**WM- \_ HScroll**](wm-hscroll.md) -Nachricht empfängt. Die TrackBar in diesem Beispiel hat den [**TSB-Stil " \_ enableselrange**](trackbar-control-styles.md) ". Die Position des Schiebereglers wird mit dem Auswahlbereich verglichen, und der Schieberegler wird bei Bedarf an die Anfangs-oder Endposition des Auswahl Bereichs verschoben.


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a>Bemerkungen

Ein Dialogfeld, das eine TrackBar im TSB-Format " [**\_ Vert**](trackbar-control-styles.md) " enthält, kann diese Funktion verwenden, wenn Sie eine [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht empfängt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von TrackBar-Steuerelementen](using-trackbar-controls.md)
</dt> </dl>

 

 




