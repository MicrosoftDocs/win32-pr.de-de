---
title: Begrenzen der Schieberegler-Bewegung
description: Wie in Informationen zu TrackBar-Steuerelementen beschrieben, ist es möglich, einen Teil des TrackBar-Bereichs als Auswahlbereich festzulegen. Ein Zweck eines Auswahl Bereichs ist möglicherweise, die Verschiebung des Schiebereglers einzuschränken, sodass einige Teile des vollständigen Bereichs deaktiviert werden.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855707"
---
# <a name="how-to-limit-slider-movement"></a>Begrenzen der Schieberegler-Bewegung

Wie in [Informationen zu TrackBar](trackbar-controls.md)-Steuerelementen beschrieben, ist es möglich, einen Teil des TrackBar-Bereichs als Auswahlbereich festzulegen. Ein Zweck eines Auswahl Bereichs ist möglicherweise, die Verschiebung des Schiebereglers einzuschränken, sodass einige Teile des vollständigen Bereichs deaktiviert werden.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="limit-slider-movement"></a>Verschiebungs Bewegung begrenzen

Der folgende Beispielcode schränkt die Verschiebung des Schiebereglers ein, indem die Position des Schiebereglers bei jedem Verschieben außerhalb des Auswahl Bereichs zurückgesetzt wird.


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a>Bemerkungen

Dieser Code Ausschnitt ist Teil der Fenster Prozedur des Dialog Felds.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von TrackBar-Steuerelementen](using-trackbar-controls.md)
</dt> </dl>

 

 




