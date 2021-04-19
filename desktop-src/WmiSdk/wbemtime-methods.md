---
description: Die wbemtime-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: 56B21156-8FD2-4FF8-805E-DDA63C897F80
ms.tgt_platform: multiple
title: WBEMTime-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e77c338f3d1d0657e20bfe6b819c9976d00d45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362978"
---
# <a name="wbemtime-methods"></a><span data-ttu-id="ba0ca-103">WBEMTime-Methoden</span><span class="sxs-lookup"><span data-stu-id="ba0ca-103">WBEMTime Methods</span></span>

<span data-ttu-id="ba0ca-104">\[Die [**wbemtime**](wbemtime.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates für nicht sicherheitsrelevante Probleme verfügbar sind, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="ba0ca-104">\[The [**WBEMTime**](wbemtime.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="ba0ca-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="ba0ca-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="ba0ca-106">Die [**wbemtime**](wbemtime.md) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ba0ca-106">The [**WBEMTime**](wbemtime.md) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ba0ca-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ba0ca-107">In this section</span></span>

-   [<span data-ttu-id="ba0ca-108">**Clear-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-108">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)
-   [<span data-ttu-id="ba0ca-109">**GetBSTR-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-109">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)
-   [<span data-ttu-id="ba0ca-110">**Getdmtf-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-110">**GetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)
-   [<span data-ttu-id="ba0ca-111">**Getdmtf nonntfs-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-111">**GetDMTFNonNtfs method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)
-   [<span data-ttu-id="ba0ca-112">**GetFileTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-112">**GetFILETIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)
-   <span data-ttu-id="ba0ca-113">[**Getlocaloffsetfordate-Methoden**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba0ca-113">[**GetLocalOffsetForDate methods**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85))</span></span>
-   [<span data-ttu-id="ba0ca-114">**Getstructtm-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-114">**GetStructtm method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)
-   [<span data-ttu-id="ba0ca-115">**GetSystemTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-115">**GetSYSTEMTIME method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)
-   [<span data-ttu-id="ba0ca-116">**GetTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-116">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)
-   [<span data-ttu-id="ba0ca-117">**GetTime \_ t-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-117">**Gettime\_t method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)
-   [<span data-ttu-id="ba0ca-118">**IsOK-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-118">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)
-   <span data-ttu-id="ba0ca-119">[**Operator-Operatoren**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba0ca-119">[**operator- operators**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))</span></span>
-   [<span data-ttu-id="ba0ca-120">**Wbemtime:: Operator! =-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-120">**WBEMTime::operator != method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)
-   [<span data-ttu-id="ba0ca-121">**Wbemtime:: Operator <-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-121">**WBEMTime::operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)
-   [<span data-ttu-id="ba0ca-122">**Wbemtime:: Operator <=-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-122">**WBEMTime::operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)
-   [<span data-ttu-id="ba0ca-123">**Wbemtime:: Operator = =-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-123">**WBEMTime::operator == method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)
-   [<span data-ttu-id="ba0ca-124">**Wbemtime:: Operator >-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-124">**WBEMTime::operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="ba0ca-125">**Wbemtime:: Operator >=-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-125">**WBEMTime::operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="ba0ca-126">**Operator +-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-126">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="ba0ca-127">**Operator + =-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-127">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   <span data-ttu-id="ba0ca-128">[**Operator = Operatoren**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba0ca-128">[**operator= operators**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))</span></span>
-   [<span data-ttu-id="ba0ca-129">**Operator-=-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-129">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="ba0ca-130">**Setdmtf-Methode**</span><span class="sxs-lookup"><span data-stu-id="ba0ca-130">**SetDMTF method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)
-   <span data-ttu-id="ba0ca-131">[**Wbemtime-Konstruktoren**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span><span class="sxs-lookup"><span data-stu-id="ba0ca-131">[**WBEMTime constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr))</span></span>

 

 
