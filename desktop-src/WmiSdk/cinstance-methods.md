---
description: Die CInstance-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: B9846350-405D-440E-AC35-16446D3F03F5
ms.tgt_platform: multiple
title: CInstance-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e088f4604263d3fd1673982e22e2f6c88f991b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866900"
---
# <a name="cinstance-methods"></a><span data-ttu-id="c0857-103">CInstance-Methoden</span><span class="sxs-lookup"><span data-stu-id="c0857-103">CInstance Methods</span></span>

<span data-ttu-id="c0857-104">\[Die [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="c0857-104">\[The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="c0857-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="c0857-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="c0857-106">Die [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c0857-106">The [**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c0857-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c0857-107">In this section</span></span>

-   [<span data-ttu-id="c0857-108">**Commit-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-108">**Commit method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-commit)
-   [<span data-ttu-id="c0857-109">**GetBool-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-109">**Getbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbool)
-   [<span data-ttu-id="c0857-110">**GetByte-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-110">**GetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getbyte)
-   [<span data-ttu-id="c0857-111">**Getchstring-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-111">**GetCHString method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getchstring)
-   [<span data-ttu-id="c0857-112">**Getclassobjectinterface-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-112">**GetClassObjectInterface method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getclassobjectinterface)
-   [<span data-ttu-id="c0857-113">**GetDateTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-113">**GetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdatetime)
-   [<span data-ttu-id="c0857-114">**GetDouble-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-114">**GetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdouble)
-   [<span data-ttu-id="c0857-115">**Getdword-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-115">**GetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getdword)
-   [<span data-ttu-id="c0857-116">**Getembeddedobject-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-116">**GetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getembeddedobject)
-   [<span data-ttu-id="c0857-117">**Getmethodcontext-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-117">**GetMethodContext method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getmethodcontext)
-   [<span data-ttu-id="c0857-118">**GetStatus-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-118">**GetStatus method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstatus)
-   [<span data-ttu-id="c0857-119">**GetStringArray-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-119">**GetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getstringarray)
-   [<span data-ttu-id="c0857-120">**GetTimeSpan-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-120">**GetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-gettimespan)
-   [<span data-ttu-id="c0857-121">**Getvariant-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-121">**GetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getvariant)
-   [<span data-ttu-id="c0857-122">**GetWBEMINT16-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-122">**GetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwbemint16)
-   [<span data-ttu-id="c0857-123">**GetWBEMINT64-Methoden**</span><span class="sxs-lookup"><span data-stu-id="c0857-123">**GetWBEMINT64 methods**</span></span>](cinstance-getwbemint64.md)
-   [<span data-ttu-id="c0857-124">**Getwchar-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-124">**GetWCHAR method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getwchar)
-   [<span data-ttu-id="c0857-125">**GetWord-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-125">**GetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-getword)
-   [<span data-ttu-id="c0857-126">**IsNull-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-126">**IsNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-isnull)
-   [<span data-ttu-id="c0857-127">**SetBool-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-127">**Setbool method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbool)
-   [<span data-ttu-id="c0857-128">**SetByte-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-128">**SetByte method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setbyte)
-   [<span data-ttu-id="c0857-129">**Setcharsplat-Methoden**</span><span class="sxs-lookup"><span data-stu-id="c0857-129">**SetCharSplat methods**</span></span>](cinstance-setcharsplat.md)
-   [<span data-ttu-id="c0857-130">**Setchstring-Methoden**</span><span class="sxs-lookup"><span data-stu-id="c0857-130">**SetCHString methods**</span></span>](cinstance-setchstring.md)
-   [<span data-ttu-id="c0857-131">**SetDateTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-131">**SetDateTime method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdatetime)
-   [<span data-ttu-id="c0857-132">**SetDouble-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-132">**SetDOUBLE method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdouble)
-   [<span data-ttu-id="c0857-133">**Setdword-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-133">**SetDWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setdword)
-   [<span data-ttu-id="c0857-134">\*\*\* Tembeddedobject-Methode\*\*</span><span class="sxs-lookup"><span data-stu-id="c0857-134">**SetEmbeddedObject method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setembeddedobject)
-   [<span data-ttu-id="c0857-135">**SetNull-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-135">**SetNull method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setnull)
-   [<span data-ttu-id="c0857-136">**Setstringarray-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-136">**SetStringArray method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setstringarray)
-   [<span data-ttu-id="c0857-137">**SetTimeSpan-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-137">**SetTimeSpan method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-settimespan)
-   [<span data-ttu-id="c0857-138">**Setvariant-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-138">**SetVariant method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setvariant)
-   [<span data-ttu-id="c0857-139">**SetWBEMINT16-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-139">**SetWBEMINT16 method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwbemint16)
-   [<span data-ttu-id="c0857-140">**""-Methode ""**</span><span class="sxs-lookup"><span data-stu-id="c0857-140">**SetWCHARSplat method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setwcharsplat)
-   <span data-ttu-id="c0857-141">[**SetWBEMINT64-Methoden**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c0857-141">[**SetWBEMINT64 methods**](/previous-versions/windows/desktop/legacy/aa389221(v=vs.85))</span></span>
-   [<span data-ttu-id="c0857-142">**Setword-Methode**</span><span class="sxs-lookup"><span data-stu-id="c0857-142">**SetWORD method**</span></span>](/windows/desktop/api/Instance/nf-instance-cinstance-setword)

 

 
