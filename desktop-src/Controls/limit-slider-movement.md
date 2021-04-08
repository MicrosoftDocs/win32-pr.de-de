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
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="83a48-104">Begrenzen der Schieberegler-Bewegung</span><span class="sxs-lookup"><span data-stu-id="83a48-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="83a48-105">Wie in [Informationen zu TrackBar](trackbar-controls.md)-Steuerelementen beschrieben, ist es möglich, einen Teil des TrackBar-Bereichs als Auswahlbereich festzulegen.</span><span class="sxs-lookup"><span data-stu-id="83a48-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="83a48-106">Ein Zweck eines Auswahl Bereichs ist möglicherweise, die Verschiebung des Schiebereglers einzuschränken, sodass einige Teile des vollständigen Bereichs deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="83a48-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="83a48-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="83a48-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="83a48-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="83a48-108">Technologies</span></span>

-   [<span data-ttu-id="83a48-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="83a48-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="83a48-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="83a48-110">Prerequisites</span></span>

-   <span data-ttu-id="83a48-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="83a48-111">C/C++</span></span>
-   <span data-ttu-id="83a48-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="83a48-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="83a48-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="83a48-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="83a48-114">Verschiebungs Bewegung begrenzen</span><span class="sxs-lookup"><span data-stu-id="83a48-114">Limit Slider Movement</span></span>

<span data-ttu-id="83a48-115">Der folgende Beispielcode schränkt die Verschiebung des Schiebereglers ein, indem die Position des Schiebereglers bei jedem Verschieben außerhalb des Auswahl Bereichs zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="83a48-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="83a48-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83a48-116">Remarks</span></span>

<span data-ttu-id="83a48-117">Dieser Code Ausschnitt ist Teil der Fenster Prozedur des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="83a48-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83a48-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="83a48-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83a48-119">Verwenden von TrackBar-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="83a48-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




