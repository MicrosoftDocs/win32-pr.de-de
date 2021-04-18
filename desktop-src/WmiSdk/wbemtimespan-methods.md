---
description: Die wbemtimespan-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: 7D450EE2-C52F-4B78-B6B1-9FD74394C3DE
ms.tgt_platform: multiple
title: WBEMTimeSpan-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d516f22a7ecd5468d53bda44ce47edbe4504d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352355"
---
# <a name="wbemtimespan-methods"></a><span data-ttu-id="97fd9-103">WBEMTimeSpan-Methoden</span><span class="sxs-lookup"><span data-stu-id="97fd9-103">WBEMTimeSpan Methods</span></span>

<span data-ttu-id="97fd9-104">\[Die [**wbemtimespan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="97fd9-104">\[The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="97fd9-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="97fd9-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="97fd9-106">Die [**wbemtimespan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="97fd9-106">The [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="97fd9-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="97fd9-107">In this section</span></span>

-   <span data-ttu-id="97fd9-108">[**Wbemtimespan-Konstruktoren**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span><span class="sxs-lookup"><span data-stu-id="97fd9-108">[**WbemTimeSpan constructors**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-wbemtimespan(constbstr))</span></span>
-   [<span data-ttu-id="97fd9-109">**Clear-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-109">**Clear method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-clear)
-   [<span data-ttu-id="97fd9-110">**GetBSTR-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-110">**GetBSTR method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-getbstr)
-   [<span data-ttu-id="97fd9-111">**GetTime-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-111">**GetTime method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-gettime)
-   [<span data-ttu-id="97fd9-112">**IsOK-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-112">**IsOk method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtimespan-isok)
-   <span data-ttu-id="97fd9-113">[**Operator =-Methode**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span><span class="sxs-lookup"><span data-stu-id="97fd9-113">[**operator= method**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))</span></span>
-   [<span data-ttu-id="97fd9-114">**Operator +-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-114">**operator+ method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add)
-   [<span data-ttu-id="97fd9-115">**Operator + =-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-115">**operator+= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-add-assign)
-   [<span data-ttu-id="97fd9-116">**Operator-Method**</span><span class="sxs-lookup"><span data-stu-id="97fd9-116">**operator- method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub)
-   [<span data-ttu-id="97fd9-117">**Operator-=-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-117">**operator-= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-sub-assign)
-   [<span data-ttu-id="97fd9-118">**Operator = =-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-118">**operator == method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-equal-equal-to)
-   [<span data-ttu-id="97fd9-119">**Operator! =-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-119">**operator != method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-not-equal-to)
-   [<span data-ttu-id="97fd9-120">**Operator >-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-120">**operator > method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)
-   [<span data-ttu-id="97fd9-121">**Operator >=-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-121">**operator >= method**</span></span>](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)
-   [<span data-ttu-id="97fd9-122">**Operator <-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-122">**operator < method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than)
-   [<span data-ttu-id="97fd9-123">**Operator <=-Methode**</span><span class="sxs-lookup"><span data-stu-id="97fd9-123">**operator <= method**</span></span>](/windows/win32/api/wbemtime/nf-wbemtime-wbemtimespan-operator-less-than-equal-to)

 

 
