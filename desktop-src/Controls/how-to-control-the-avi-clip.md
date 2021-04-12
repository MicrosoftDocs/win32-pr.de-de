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
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="6d132-103">Steuern des AVI-Clips</span><span class="sxs-lookup"><span data-stu-id="6d132-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="6d132-104">In diesem Thema wird veranschaulicht, wie Sie mit den Animations Steuerelement-Makros ein zugeordnetes Audio-Video Interleaved (AVI)-Clip abspielen, beenden und schließen.</span><span class="sxs-lookup"><span data-stu-id="6d132-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6d132-105">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="6d132-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6d132-106">Technologien</span><span class="sxs-lookup"><span data-stu-id="6d132-106">Technologies</span></span>

-   [<span data-ttu-id="6d132-107">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="6d132-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6d132-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="6d132-108">Prerequisites</span></span>

-   <span data-ttu-id="6d132-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="6d132-109">C/C++</span></span>
-   <span data-ttu-id="6d132-110">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="6d132-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="6d132-111">AVI-Dateien</span><span class="sxs-lookup"><span data-stu-id="6d132-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="6d132-112">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="6d132-112">Instructions</span></span>


<span data-ttu-id="6d132-113">Erstellen Sie eine Funktion, die als Parameter ein Handle für das Animations Steuerelement und ein Flag annimmt, das die Aktion angibt, die für den zugeordneten AVI-Clip ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6d132-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="6d132-114">Die Funktion im folgenden C++-Beispiel ruft eines von drei Animations Steuerelement-[**Makros \_ auf, basierend**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)auf dem [**Wert \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)des *naction* -Parameters. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)</span><span class="sxs-lookup"><span data-stu-id="6d132-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="6d132-115">Das Handle für das Animations Steuerelement, das dem AVI-Clip zugeordnet ist, wird über den *hwndanim* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="6d132-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6d132-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d132-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d132-117">Informationen zu Animations Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6d132-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="6d132-118">Referenz zum Animations Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d132-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6d132-119">Verwenden von Animations Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="6d132-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="6d132-120">Animations Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d132-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




