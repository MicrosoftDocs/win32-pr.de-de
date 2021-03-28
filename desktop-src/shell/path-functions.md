---
description: Path-Funktionen
ms.assetid: 0105FC65-332B-4F99-9629-F3DFEAD97535
title: Path-Funktionen (Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12265e9b1dd51f8e2ea5bc0cc384bf227b8cd041
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979961"
---
# <a name="path-functions-the-windows-shell"></a><span data-ttu-id="9d390-103">Path-Funktionen (Windows-Shell)</span><span class="sxs-lookup"><span data-stu-id="9d390-103">Path Functions (The Windows Shell)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d390-104">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9d390-104">In this section</span></span>

-   [<span data-ttu-id="9d390-105">**Pathzugeccanonicalize**</span><span class="sxs-lookup"><span data-stu-id="9d390-105">**PathAllocCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccanonicalize)
-   [<span data-ttu-id="9d390-106">**Pathzuweisung**</span><span class="sxs-lookup"><span data-stu-id="9d390-106">**PathAllocCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine)
-   [<span data-ttu-id="9d390-107">**Pathcchaddbackschräg Strich**</span><span class="sxs-lookup"><span data-stu-id="9d390-107">**PathCchAddBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash)
-   [<span data-ttu-id="9d390-108">**Pathcchaddbackslashex**</span><span class="sxs-lookup"><span data-stu-id="9d390-108">**PathCchAddBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex)
-   [<span data-ttu-id="9d390-109">**Pathcchaddextension**</span><span class="sxs-lookup"><span data-stu-id="9d390-109">**PathCchAddExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension)
-   [<span data-ttu-id="9d390-110">**Pathcchappend**</span><span class="sxs-lookup"><span data-stu-id="9d390-110">**PathCchAppend**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappend)
-   [<span data-ttu-id="9d390-111">**Pathcchappdex**</span><span class="sxs-lookup"><span data-stu-id="9d390-111">**PathCchAppendEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex)
-   [<span data-ttu-id="9d390-112">**Pathcchcanonicalize**</span><span class="sxs-lookup"><span data-stu-id="9d390-112">**PathCchCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize)
-   [<span data-ttu-id="9d390-113">**Pathcchcanonicalizeex**</span><span class="sxs-lookup"><span data-stu-id="9d390-113">**PathCchCanonicalizeEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex)
-   [<span data-ttu-id="9d390-114">**Pathcchcombine**</span><span class="sxs-lookup"><span data-stu-id="9d390-114">**PathCchCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine)
-   [<span data-ttu-id="9d390-115">**Pathcchcombineex**</span><span class="sxs-lookup"><span data-stu-id="9d390-115">**PathCchCombineEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex)
-   [<span data-ttu-id="9d390-116">**Pathcchfindextension**</span><span class="sxs-lookup"><span data-stu-id="9d390-116">**PathCchFindExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchfindextension)
-   [<span data-ttu-id="9d390-117">**Pathcchisroot**</span><span class="sxs-lookup"><span data-stu-id="9d390-117">**PathCchIsRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchisroot)
-   [<span data-ttu-id="9d390-118">**Pathcchremovebackschräg Strich**</span><span class="sxs-lookup"><span data-stu-id="9d390-118">**PathCchRemoveBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash)
-   [<span data-ttu-id="9d390-119">**Pathcchremovebackslashex**</span><span class="sxs-lookup"><span data-stu-id="9d390-119">**PathCchRemoveBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex)
-   [<span data-ttu-id="9d390-120">**Pathcchremoveextension**</span><span class="sxs-lookup"><span data-stu-id="9d390-120">**PathCchRemoveExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension)
-   [<span data-ttu-id="9d390-121">**Pathcchremovefilespec**</span><span class="sxs-lookup"><span data-stu-id="9d390-121">**PathCchRemoveFileSpec**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec)
-   [<span data-ttu-id="9d390-122">**Pathcchrenameextension**</span><span class="sxs-lookup"><span data-stu-id="9d390-122">**PathCchRenameExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension)
-   [<span data-ttu-id="9d390-123">**Pathcchskiproot**</span><span class="sxs-lookup"><span data-stu-id="9d390-123">**PathCchSkipRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchskiproot)
-   [<span data-ttu-id="9d390-124">**Pathcchstripprefix**</span><span class="sxs-lookup"><span data-stu-id="9d390-124">**PathCchStripPrefix**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstripprefix)
-   [<span data-ttu-id="9d390-125">**Pathcchstriptor**</span><span class="sxs-lookup"><span data-stu-id="9d390-125">**PathCchStripToRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot)
-   [<span data-ttu-id="9d390-126">**Pathisuncex**</span><span class="sxs-lookup"><span data-stu-id="9d390-126">**PathIsUNCEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathisuncex)

 

 



