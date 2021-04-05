---
title: Definieren des Wiedergabe Bereichs
description: Definieren des Wiedergabe Bereichs
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Mciwndplayfrom-Makro
- Mciwndplayto-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947689"
---
# <a name="defining-playback-scope"></a><span data-ttu-id="2bb71-105">Definieren des Wiedergabe Bereichs</span><span class="sxs-lookup"><span data-stu-id="2bb71-105">Defining Playback Scope</span></span>

<span data-ttu-id="2bb71-106">Mciwnd stellt Makros bereit, mit denen Sie den Wiedergabe *Bereich* definieren können.</span><span class="sxs-lookup"><span data-stu-id="2bb71-106">MCIWnd provides macros that allow you to define the playback *scope*.</span></span> <span data-ttu-id="2bb71-107">Der Bereich ist der Teil der Wiedergabe, den Sie wiedergeben möchten.</span><span class="sxs-lookup"><span data-stu-id="2bb71-107">The scope is the portion of the playback you want to play.</span></span> <span data-ttu-id="2bb71-108">Beispielsweise können Sie den Inhalt an einer anderen Position als der Anfangsposition wiedergeben, indem Sie das [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bb71-108">For example, you can play the content from a position other than the beginning position by using the [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) macro.</span></span> <span data-ttu-id="2bb71-109">Dieses Makro wechselt an die angegebene Position, beginnt mit der Wiedergabe und wird bis zum Ende des Inhalts fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2bb71-109">This macro moves to the specified position, begins playback, and continues to the end of the content.</span></span> <span data-ttu-id="2bb71-110">Entsprechend können Sie den Inhalt für einen angegebenen Endpunkt wiedergeben, indem Sie das [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bb71-110">Similarly, you can play the content to a specified end point by using the [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) macro.</span></span> <span data-ttu-id="2bb71-111">Dieses Makro beginnt an der aktuellen Wiedergabe Position und wird wiedergegeben, bis die angegebene Position erreicht oder das Ende des Inhalts erreicht ist, je nachdem, was zuerst eintritt.</span><span class="sxs-lookup"><span data-stu-id="2bb71-111">This macro starts at the current playback position and plays until it reaches the specified position or the end of the content is reached, whichever comes first.</span></span>

<span data-ttu-id="2bb71-112">Außerdem können Sie die Anfangs-und Endpositionen definieren, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="2bb71-112">Also, you can define both the beginning and ending positions by using the [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) macro.</span></span> <span data-ttu-id="2bb71-113">Dieses Makro wechselt an die angegebene Anfangsposition und wird wiedergegeben, bis die angegebene Endposition oder das Ende des Inhalts erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="2bb71-113">This macro moves to the specified starting position and plays until the specified ending position or the end of the content is reached.</span></span>

 

 




