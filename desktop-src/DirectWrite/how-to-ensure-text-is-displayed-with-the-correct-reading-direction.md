---
title: Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.
description: Einige Sprachen, z. b. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730169"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="b9681-103">Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b9681-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="b9681-104">Einige Sprachen, z. b. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="b9681-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="b9681-105">Bei einem Objekt im [DirectWrite](direct-write-portal.md) -Textformat ist die Standard Leserichtung von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="b9681-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="b9681-106">DirectWrite leitet die Leserichtung nicht automatisch aus dem Gebiets Schema ab, sodass Sie dies selbst tun müssen.</span><span class="sxs-lookup"><span data-stu-id="b9681-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="b9681-107">Holen Sie zuerst die erweiterten stilflags für das Fenster, in dem der Text gerendert wird, indem Sie das in WINDOWSX. h definierte getwindowstyleex-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="b9681-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="b9681-108">Das-Makro gibt einen DWORD-Wert zurück, der aus mehreren Flags zusammen mit bitweisen or-Vorgängen besteht.</span><span class="sxs-lookup"><span data-stu-id="b9681-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="b9681-109">Sie müssen bestimmen, ob die spezifischen Flags, die die Leserichtung beeinflussen, vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b9681-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="b9681-110">Es gibt zwei verschiedene Flags, die sich auf die Leserichtung beziehen: WS \_ Ex \_ layoutrtl und WS \_ Ex \_ RtlReading.</span><span class="sxs-lookup"><span data-stu-id="b9681-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="b9681-111">Verwenden Sie den bitweisen AND-Operator (&) mit der dwstyle-Variablen und dem WS \_ Ex \_ layoutrtl-Makro, um einen booleschen Wert zu speichern, der angibt, ob das Layout gespiegelt wird.</span><span class="sxs-lookup"><span data-stu-id="b9681-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="b9681-112">Führen Sie die gleichen Schritte für das WS \_ Ex \_ RtlReading-Flag aus.</span><span class="sxs-lookup"><span data-stu-id="b9681-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="b9681-113">Legen Sie die Leserichtung mithilfe der Methode [**idschreitetextformat:: setreadingdirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) fest.</span><span class="sxs-lookup"><span data-stu-id="b9681-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="b9681-114">Der Standardwert ist von links nach rechts, sodass Sie nur die Leserichtung festlegen müssen, wenn Sie von rechts nach links ist.</span><span class="sxs-lookup"><span data-stu-id="b9681-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="b9681-115">WS \_ Ex \_ layoutrtl spiegelt das gesamte Layout wider und impliziert die Leserichtung von rechts nach links. Legen Sie daher die Leserichtung nur dann fest, wenn eines dieser Flags vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b9681-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="b9681-116">Wenn beide vorhanden sind, brechen Sie einander ab, und die Leserichtung für das Textformat sollte von links nach rechts erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b9681-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
