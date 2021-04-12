---
title: Steuern des AVI-Clips
description: In diesem Thema wird veranschaulicht, wie Sie mit den Animations Steuerelement-Makros ein zugeordnetes Audio-Video Interleaved (AVI)-Clip abspielen, beenden und schließen.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474704"
---
# <a name="how-to-control-the-avi-clip"></a>Steuern des AVI-Clips

In diesem Thema wird veranschaulicht, wie Sie mit den Animations Steuerelement-Makros ein zugeordnetes Audio-Video Interleaved (AVI)-Clip abspielen, beenden und schließen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche
-   AVI-Dateien

## <a name="instructions"></a>Anweisungen


Erstellen Sie eine Funktion, die als Parameter ein Handle für das Animations Steuerelement und ein Flag annimmt, das die Aktion angibt, die für den zugeordneten AVI-Clip ausgeführt werden soll.

Die Funktion im folgenden C++-Beispiel ruft eines von drei Animations Steuerelement-[**Makros \_ auf, basierend**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)auf dem [**Wert \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)des *naction* -Parameters. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) Das Handle für das Animations Steuerelement, das dem AVI-Clip zugeordnet ist, wird über den *hwndanim* -Parameter übergeben.


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

[Informationen zu Animations Steuerelementen](animation-control-overview.md)
</dt> <dt>

[Referenz zum Animations Steuerelement](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Verwenden von Animations Steuerelementen](using-animation-control.md)
</dt> <dt>

[Animations Steuerelement](animation-control-reference.md)
</dt> </dl>

 

 




