---
title: Strauchsichere Funktionen
description: .
ms.assetid: 3590dd8d-3a88-4dde-a5fe-f10e12354919
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b31824788b68a7ec789c6d274b2a368eda1cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337427"
---
# <a name="strsafe-functions"></a><span data-ttu-id="70b1e-103">Strauchsichere Funktionen</span><span class="sxs-lookup"><span data-stu-id="70b1e-103">Strsafe Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70b1e-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="70b1e-104">In this section</span></span>

-   [<span data-ttu-id="70b1e-105">**Stringcbcat**</span><span class="sxs-lookup"><span data-stu-id="70b1e-105">**StringCbCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)
-   [<span data-ttu-id="70b1e-106">**Stringcb-Ex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-106">**StringCbCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)
-   [<span data-ttu-id="70b1e-107">**Stringcb-n**</span><span class="sxs-lookup"><span data-stu-id="70b1e-107">**StringCbCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)
-   [<span data-ttu-id="70b1e-108">**Stringcbcr-x**</span><span class="sxs-lookup"><span data-stu-id="70b1e-108">**StringCbCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)
-   [<span data-ttu-id="70b1e-109">**Stringcbcopy**</span><span class="sxs-lookup"><span data-stu-id="70b1e-109">**StringCbCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)
-   [<span data-ttu-id="70b1e-110">**Stringcbcopyex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-110">**StringCbCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)
-   [<span data-ttu-id="70b1e-111">**Stringcbcopyn**</span><span class="sxs-lookup"><span data-stu-id="70b1e-111">**StringCbCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)
-   [<span data-ttu-id="70b1e-112">**Stringcbcopynetx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-112">**StringCbCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)
-   [<span data-ttu-id="70b1e-113">**Stringcbgets**</span><span class="sxs-lookup"><span data-stu-id="70b1e-113">**StringCbGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)
-   [<span data-ttu-id="70b1e-114">**Stringcbgetsex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-114">**StringCbGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)
-   [<span data-ttu-id="70b1e-115">**Stringcblength**</span><span class="sxs-lookup"><span data-stu-id="70b1e-115">**StringCbLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)
-   [<span data-ttu-id="70b1e-116">**Stringcbprintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="70b1e-116">**StringCbPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_la)
-   [<span data-ttu-id="70b1e-117">**Stringcbprintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-117">**StringCbPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_lexa)
-   [<span data-ttu-id="70b1e-118">**Stringcbprintf**</span><span class="sxs-lookup"><span data-stu-id="70b1e-118">**StringCbPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)
-   [<span data-ttu-id="70b1e-119">**Stringcbprintfex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-119">**StringCbPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)
-   [<span data-ttu-id="70b1e-120">**Stringcbvprintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="70b1e-120">**StringCbVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_la)
-   [<span data-ttu-id="70b1e-121">**Stringcbvprintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-121">**StringCbVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_lexa)
-   [<span data-ttu-id="70b1e-122">**Stringcbvprintf**</span><span class="sxs-lookup"><span data-stu-id="70b1e-122">**StringCbVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)
-   [<span data-ttu-id="70b1e-123">**Stringcbvprintfex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-123">**StringCbVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)
-   [<span data-ttu-id="70b1e-124">**StringCchCat**</span><span class="sxs-lookup"><span data-stu-id="70b1e-124">**StringCchCat**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)
-   [<span data-ttu-id="70b1e-125">**Stringcch| Ex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-125">**StringCchCatEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)
-   [<span data-ttu-id="70b1e-126">**Stringcch.**</span><span class="sxs-lookup"><span data-stu-id="70b1e-126">**StringCchCatN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)
-   [<span data-ttu-id="70b1e-127">**Stringcchcatcher**</span><span class="sxs-lookup"><span data-stu-id="70b1e-127">**StringCchCatNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)
-   [<span data-ttu-id="70b1e-128">**StringCchCopy**</span><span class="sxs-lookup"><span data-stu-id="70b1e-128">**StringCchCopy**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)
-   [<span data-ttu-id="70b1e-129">**Stringcchcopyex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-129">**StringCchCopyEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)
-   [<span data-ttu-id="70b1e-130">**Stringcchcopyn**</span><span class="sxs-lookup"><span data-stu-id="70b1e-130">**StringCchCopyN**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)
-   [<span data-ttu-id="70b1e-131">**Stringcchcopynetx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-131">**StringCchCopyNEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)
-   [<span data-ttu-id="70b1e-132">**Stringcchgets**</span><span class="sxs-lookup"><span data-stu-id="70b1e-132">**StringCchGets**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)
-   [<span data-ttu-id="70b1e-133">**Stringcchgetsex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-133">**StringCchGetsEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)
-   [<span data-ttu-id="70b1e-134">**Stringcchlength**</span><span class="sxs-lookup"><span data-stu-id="70b1e-134">**StringCchLength**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)
-   [<span data-ttu-id="70b1e-135">**StringCchPrintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="70b1e-135">**StringCchPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_la)
-   [<span data-ttu-id="70b1e-136">**StringCchPrintf \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-136">**StringCchPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_lexa)
-   [<span data-ttu-id="70b1e-137">**StringCchPrintf**</span><span class="sxs-lookup"><span data-stu-id="70b1e-137">**StringCchPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)
-   [<span data-ttu-id="70b1e-138">**Stringcchprintfex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-138">**StringCchPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)
-   [<span data-ttu-id="70b1e-139">**Stringcchvprintf \_ l**</span><span class="sxs-lookup"><span data-stu-id="70b1e-139">**StringCchVPrintf\_l**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_la)
-   [<span data-ttu-id="70b1e-140">**Stringcchvprintf- \_ lEx**</span><span class="sxs-lookup"><span data-stu-id="70b1e-140">**StringCchVPrintf\_lEx**</span></span>](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_lexa)
-   [<span data-ttu-id="70b1e-141">**Stringcchvprintf**</span><span class="sxs-lookup"><span data-stu-id="70b1e-141">**StringCchVPrintf**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)
-   [<span data-ttu-id="70b1e-142">**Stringcchvprintfex**</span><span class="sxs-lookup"><span data-stu-id="70b1e-142">**StringCchVPrintfEx**</span></span>](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)
-   <span data-ttu-id="70b1e-143">[**Unalignedstringcblength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70b1e-143">[**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))</span></span>
-   <span data-ttu-id="70b1e-144">[**Unalignedstringcchlength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="70b1e-144">[**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))</span></span>

 

 