---
title: Verarbeiten von Trackbar-Benachrichtigungsmeldungen
description: Trackleisten benachrichtigen das übergeordnete Fenster über Benutzeraktionen, indem sie dem übergeordneten Element eine WM \_ HSCROLL- oder WM \_ VSCROLL-Nachricht senden.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211a468c5c107a96fc6b28d12feed219799450828db07be87cd8887b5816bd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540320"
---
# <a name="how-to-process-trackbar-notification-messages"></a>Verarbeiten von Trackbar-Benachrichtigungsmeldungen

Trackleisten benachrichtigen das übergeordnete Fenster über Benutzeraktionen, indem sie dem übergeordneten Element eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) senden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen

### <a name="process-trackbar-notification-messages"></a>Verarbeiten von Trackbar-Benachrichtigungsmeldungen

Das folgende Codebeispiel ist eine Funktion, die aufgerufen wird, wenn das übergeordnete Fenster der Trackleiste eine [**WM \_ HSCROLL-Nachricht**](wm-hscroll.md) empfängt. Die Trackleiste in diesem Beispiel hat den [**TBS \_ ENABLESELRANGE-Stil.**](trackbar-control-styles.md) Die Position des Schiebereglers wird mit dem Auswahlbereich verglichen, und der Schieberegler wird bei Bedarf an die Anfangs- oder Endposition des Auswahlbereichs verschoben.


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



## <a name="remarks"></a>Hinweise

Ein Dialogfeld, das eine [**TBS \_ VERT-Trackleiste**](trackbar-control-styles.md) enthält, kann diese Funktion verwenden, wenn es eine [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) empfängt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Trackbar-Steuerelementen](using-trackbar-controls.md)
</dt> </dl>

 

 




