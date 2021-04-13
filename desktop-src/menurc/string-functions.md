---
title: Zeichenfolgenfunktionen
description: .
ms.assetid: 0249ea7a-84f1-4e25-9e80-0be5eb6c04ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b2f6c3f75e98de2f951f56aa2891eab72401a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388555"
---
# <a name="string-functions"></a><span data-ttu-id="1e65d-103">Zeichenfolgenfunktionen</span><span class="sxs-lookup"><span data-stu-id="1e65d-103">String Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1e65d-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1e65d-104">In This Section</span></span>

-   [<span data-ttu-id="1e65d-105">**Charlower**</span><span class="sxs-lookup"><span data-stu-id="1e65d-105">**CharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowera)
-   [<span data-ttu-id="1e65d-106">**Charlowerbuff**</span><span class="sxs-lookup"><span data-stu-id="1e65d-106">**CharLowerBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa)
-   [<span data-ttu-id="1e65d-107">**Charnext**</span><span class="sxs-lookup"><span data-stu-id="1e65d-107">**CharNext**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnexta)
-   [<span data-ttu-id="1e65d-108">**Charnextexa**</span><span class="sxs-lookup"><span data-stu-id="1e65d-108">**CharNextExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnextexa)
-   [<span data-ttu-id="1e65d-109">**Charprev**</span><span class="sxs-lookup"><span data-stu-id="1e65d-109">**CharPrev**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charpreva)
-   [<span data-ttu-id="1e65d-110">**Charprevexa**</span><span class="sxs-lookup"><span data-stu-id="1e65d-110">**CharPrevExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charprevexa)
-   [<span data-ttu-id="1e65d-111">**Charper OEM**</span><span class="sxs-lookup"><span data-stu-id="1e65d-111">**CharToOem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooema)
-   [<span data-ttu-id="1e65d-112">**Chartoken**</span><span class="sxs-lookup"><span data-stu-id="1e65d-112">**CharToOemBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooembuffa)
-   [<span data-ttu-id="1e65d-113">**Charupper**</span><span class="sxs-lookup"><span data-stu-id="1e65d-113">**CharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charuppera)
-   [<span data-ttu-id="1e65d-114">**Charupperbuff**</span><span class="sxs-lookup"><span data-stu-id="1e65d-114">**CharUpperBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa)
-   [<span data-ttu-id="1e65d-115">**Ischaralpha**</span><span class="sxs-lookup"><span data-stu-id="1e65d-115">**IsCharAlpha**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)
-   [<span data-ttu-id="1e65d-116">**Ischaralpha numerisch**</span><span class="sxs-lookup"><span data-stu-id="1e65d-116">**IsCharAlphaNumeric**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica)
-   [<span data-ttu-id="1e65d-117">**Ischarlower**</span><span class="sxs-lookup"><span data-stu-id="1e65d-117">**IsCharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)
-   [<span data-ttu-id="1e65d-118">**Ischarupper**</span><span class="sxs-lookup"><span data-stu-id="1e65d-118">**IsCharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)
-   [<span data-ttu-id="1e65d-119">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="1e65d-119">**LoadString**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadstringa)
-   [<span data-ttu-id="1e65d-120">**lstrincat**</span><span class="sxs-lookup"><span data-stu-id="1e65d-120">**lstrcat**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcata)
-   [<span data-ttu-id="1e65d-121">**lstraucmp**</span><span class="sxs-lookup"><span data-stu-id="1e65d-121">**lstrcmp**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa)
-   [<span data-ttu-id="1e65d-122">**lstraucmpi**</span><span class="sxs-lookup"><span data-stu-id="1e65d-122">**lstrcmpi**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpia)
-   [<span data-ttu-id="1e65d-123">**lstrincpy**</span><span class="sxs-lookup"><span data-stu-id="1e65d-123">**lstrcpy**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)
-   [<span data-ttu-id="1e65d-124">**lstrincpyn**</span><span class="sxs-lookup"><span data-stu-id="1e65d-124">**lstrcpyn**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpyna)
-   [<span data-ttu-id="1e65d-125">**lstrlen**</span><span class="sxs-lookup"><span data-stu-id="1e65d-125">**lstrlen**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrlena)
-   [<span data-ttu-id="1e65d-126">**Oemto Char**</span><span class="sxs-lookup"><span data-stu-id="1e65d-126">**OemToChar**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtochara)
-   [<span data-ttu-id="1e65d-127">**Oemzu charbuff**</span><span class="sxs-lookup"><span data-stu-id="1e65d-127">**OemToCharBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa)
-   [<span data-ttu-id="1e65d-128">**wsprintf**</span><span class="sxs-lookup"><span data-stu-id="1e65d-128">**wsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)
-   [<span data-ttu-id="1e65d-129">**Wvsprintf**</span><span class="sxs-lookup"><span data-stu-id="1e65d-129">**wvsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)

 

 




