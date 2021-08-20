---
title: Steuern des AVI-Clips
description: In diesem Thema wird veranschaulicht, wie sie die Animationssteuersteuermakros verwenden, um einen zugeordneten zwischengespeicherten Clip (AVI) Audio-Video, zu beenden und zu schließen.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbabd3ea6e0694448e4bd8c01e53161333b2df3904cf1578252bdbe150d3d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170761"
---
# <a name="how-to-control-the-avi-clip"></a>Steuern des AVI-Clips

In diesem Thema wird veranschaulicht, wie sie die Animationssteuersteuermakros verwenden, um einen zugeordneten zwischengespeicherten Clip (AVI) Audio-Video, zu beenden und zu schließen.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung
-   AVI-Dateien

## <a name="instructions"></a>Anweisungen


Erstellen Sie eine Funktion, die als Parameter ein Handle für das Animationssteuerzeichen und ein Flag angibt, das die Aktion angibt, die für den zugeordneten AVI-Clip ausgeführt werden soll.

Die Funktion im folgenden C++-Beispiel ruft basierend auf dem Wert des *nAction-Parameters* eines von drei Animationssteuersteuermakros auf ([**\_ Animieren**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)der Wiedergabe , [**Animieren \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)beenden , [**Schließen animieren). \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) Das Handle für das animations-Steuerelement, das dem AVI-Clip zugeordnet ist, wird über den *hwndAnim-Parameter* übergeben.


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Animationssteuerelementen](animation-control-overview.md)
</dt> <dt>

[Referenz zum Animationssteuersteuersystem](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Verwenden von Animationssteuerelementen](using-animation-control.md)
</dt> <dt>

[Animation-Steuerelement](animation-control-reference.md)
</dt> </dl>

 

 




