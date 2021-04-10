---
description: Stellt ein Histogramm einer Textur dar.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixenginehistogram-Struktur
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124682"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="72747-103"><span id="vspixengine.pixenginehistogram"></span>Pixenginehistogram-Struktur</span><span class="sxs-lookup"><span data-stu-id="72747-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="72747-104">Stellt ein Histogramm einer Textur dar.</span><span class="sxs-lookup"><span data-stu-id="72747-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="72747-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72747-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="72747-106">Member</span><span class="sxs-lookup"><span data-stu-id="72747-106">Members</span></span>

<span data-ttu-id="72747-107">**horizontalmin**</span><span class="sxs-lookup"><span data-stu-id="72747-107">**horizontalMin**</span></span>  
<span data-ttu-id="72747-108">Die minimalen Werte für jede der X-, Y-, Z-und W-Komponenten in der horizontalen Achse (Domäne) des Histogramms.</span><span class="sxs-lookup"><span data-stu-id="72747-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="72747-109">**horizontalmax**</span><span class="sxs-lookup"><span data-stu-id="72747-109">**horizontalMax**</span></span>  
<span data-ttu-id="72747-110">Die maximalen Werte für jede der X-, Y-, Z-und W-Komponenten in der horizontalen Achse (Domäne) des Histogramms.</span><span class="sxs-lookup"><span data-stu-id="72747-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="72747-111">**verticalmin**</span><span class="sxs-lookup"><span data-stu-id="72747-111">**verticalMin**</span></span>  
<span data-ttu-id="72747-112">Die minimalen Werte für jede der X-, Y-, Z-und W-Komponenten auf der vertikalen Achse (Bereich) des Histogramms.</span><span class="sxs-lookup"><span data-stu-id="72747-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="72747-113">**verticalmax**</span><span class="sxs-lookup"><span data-stu-id="72747-113">**verticalMax**</span></span>  
<span data-ttu-id="72747-114">Die maximalen Werte für jede der X-, Y-, Z-und W-Komponenten auf der vertikalen Achse (Bereich) des Histogramms.</span><span class="sxs-lookup"><span data-stu-id="72747-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="72747-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="72747-115">**dataLength**</span></span>  
<span data-ttu-id="72747-116">Die Anzahl der im Histogramm berücksichtigten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="72747-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="72747-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72747-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="72747-118">Header</span><span class="sxs-lookup"><span data-stu-id="72747-118">Header</span></span></p></td><td><span data-ttu-id="72747-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="72747-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



