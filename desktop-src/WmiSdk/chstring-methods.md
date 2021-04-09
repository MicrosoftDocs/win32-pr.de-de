---
description: Die chstring-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: C064D6DE-14C4-4143-8164-B367C10CBF8E
ms.tgt_platform: multiple
title: Chstring-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15a26bf2b5945990f8cd37ee67c2953395ca98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042476"
---
# <a name="chstring-methods"></a><span data-ttu-id="0bc81-103">Chstring-Methoden</span><span class="sxs-lookup"><span data-stu-id="0bc81-103">CHString Methods</span></span>

<span data-ttu-id="0bc81-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="0bc81-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0bc81-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="0bc81-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0bc81-106">Die [**chstring**](chstring.md) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0bc81-106">The [**CHString**](chstring.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0bc81-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0bc81-107">In this section</span></span>

-   [<span data-ttu-id="0bc81-108">**Methode ' zugeordcsysstring '**</span><span class="sxs-lookup"><span data-stu-id="0bc81-108">**AllocSysString method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)
-   <span data-ttu-id="0bc81-109">[**Chstring-Konstruktoren**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span><span class="sxs-lookup"><span data-stu-id="0bc81-109">[**CHString constructors**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_))</span></span>
-   [<span data-ttu-id="0bc81-110">**COLLATE-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-110">**Collate method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-collate)
-   [<span data-ttu-id="0bc81-111">**Compare-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-111">**Compare method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-compare)
-   [<span data-ttu-id="0bc81-112">**Comparumocase-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-112">**CompareNoCase method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)
-   [<span data-ttu-id="0bc81-113">**Empty-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-113">**Empty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-empty)
-   <span data-ttu-id="0bc81-114">[**Methoden suchen**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span><span class="sxs-lookup"><span data-stu-id="0bc81-114">[**Find methods**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))</span></span>
-   [<span data-ttu-id="0bc81-115">**Findoneof-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-115">**FindOneOf method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)
-   <span data-ttu-id="0bc81-116">[**Formatieren von Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span><span class="sxs-lookup"><span data-stu-id="0bc81-116">[**Format methods**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))</span></span>
-   <span data-ttu-id="0bc81-117">[**Formatmessagew-Methoden**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span><span class="sxs-lookup"><span data-stu-id="0bc81-117">[**FormatMessageW methods**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))</span></span>
-   [<span data-ttu-id="0bc81-118">**Formatv-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-118">**FormatV method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)
-   [<span data-ttu-id="0bc81-119">**Methode "freextra"**</span><span class="sxs-lookup"><span data-stu-id="0bc81-119">**FreeExtra method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)
-   [<span data-ttu-id="0bc81-120">**Getalloclength-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-120">**GetAllocLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)
-   <span data-ttu-id="0bc81-121">[**GetAt-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span><span class="sxs-lookup"><span data-stu-id="0bc81-121">[**GetAt method**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))</span></span>
-   [<span data-ttu-id="0bc81-122">**GetBuffer-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-122">**GetBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)
-   [<span data-ttu-id="0bc81-123">**Getbuffersetlength-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-123">**GetBufferSetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength)
-   [<span data-ttu-id="0bc81-124">**GetData-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-124">**GetData method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)
-   [<span data-ttu-id="0bc81-125">**GetLength-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-125">**GetLength method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)
-   [<span data-ttu-id="0bc81-126">**IsEmpty-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-126">**IsEmpty method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)
-   [<span data-ttu-id="0bc81-127">**Left-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-127">**Left method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-left)
-   <span data-ttu-id="0bc81-128">[**Loadstringw-Methode**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span><span class="sxs-lookup"><span data-stu-id="0bc81-128">[**LoadStringW method**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))</span></span>
-   [<span data-ttu-id="0bc81-129">**LockBuffer-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-129">**LockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)
-   [<span data-ttu-id="0bc81-130">**Makelower-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-130">**MakeLower method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)
-   [<span data-ttu-id="0bc81-131">**Makereverse-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-131">**MakeReverse method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)
-   [<span data-ttu-id="0bc81-132">**Makeuppermethode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-132">**MakeUpper method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)
-   <span data-ttu-id="0bc81-133">[**Mid-Methoden**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span><span class="sxs-lookup"><span data-stu-id="0bc81-133">[**Mid methods**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))</span></span>
-   <span data-ttu-id="0bc81-134">[**Operator- \[ \] Methode**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-134">[**operator\[\] method**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))</span></span>
-   [<span data-ttu-id="0bc81-135">**Chstring:: Operator +**</span><span class="sxs-lookup"><span data-stu-id="0bc81-135">**CHString::operator+**</span></span>](chstring--operator-plus.md)
-   [<span data-ttu-id="0bc81-136">**Chstring:: Operator + =**</span><span class="sxs-lookup"><span data-stu-id="0bc81-136">**CHString::operator+=**</span></span>](chstring--operator-plus-equal.md)
-   [<span data-ttu-id="0bc81-137">**Chstring:: Operator =**</span><span class="sxs-lookup"><span data-stu-id="0bc81-137">**CHString::operator=**</span></span>](chstring--operator-equal.md)
-   <span data-ttu-id="0bc81-138">[**Operator = = (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-138">[**operator==(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-139">[**Operator = = (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-139">[**operator==(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-140">[**Operator> (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-140">[**operator>(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-141">[**Operator> (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-141">[**operator>(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-142">[**Operator>= (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-142">[**operator>=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-143">[**Operator>= (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-143">[**operator>=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-144">[**Operator< (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-144">[**operator<(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-145">[**Operator< (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-145">[**operator<(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-146">[**Operator<= (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-146">[**operator<=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-147">[**Operator<= (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-147">[**operator<=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-148">[**Operator! = (constchstring&, constchstring&)-Methode**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-148">[**operator!=(constCHString&, constCHString&) method**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))</span></span>
-   <span data-ttu-id="0bc81-149">[**Operator! = (constchstring&, constlpcwstr&)-Methode**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bc81-149">[**operator!=(constCHString&, constLPCWSTR&) method**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))</span></span>
-   [<span data-ttu-id="0bc81-150">**Operator LPCWSTR-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-150">**operator LPCWSTR method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)
-   [<span data-ttu-id="0bc81-151">**ReleaseBuffer-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-151">**ReleaseBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)
-   [<span data-ttu-id="0bc81-152">**Reverdie Find-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-152">**ReverseFind method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)
-   [<span data-ttu-id="0bc81-153">**Right-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-153">**Right method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-right)
-   [<span data-ttu-id="0bc81-154">**Methode "-Methode"**</span><span class="sxs-lookup"><span data-stu-id="0bc81-154">**SetAt method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-setat)
-   [<span data-ttu-id="0bc81-155">**Span Ausschluss-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-155">**SpanExcluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)
-   [<span data-ttu-id="0bc81-156">**Span-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-156">**SpanIncluding method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)
-   [<span data-ttu-id="0bc81-157">**TrimLeft-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-157">**TrimLeft method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)
-   [<span data-ttu-id="0bc81-158">**TrimRight-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-158">**TrimRight method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)
-   [<span data-ttu-id="0bc81-159">**UnlockBuffer-Methode**</span><span class="sxs-lookup"><span data-stu-id="0bc81-159">**UnlockBuffer method**</span></span>](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)

 

 
