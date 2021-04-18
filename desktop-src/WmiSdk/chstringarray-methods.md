---
description: Die chstringarray-Klasse stellt die folgenden Methoden zur Verfügung.
ms.assetid: AFE4306E-6BB1-4F1D-A301-CD5F05385466
ms.tgt_platform: multiple
title: Chstringarray-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bfbe2afa9948e14362d05f5f90a2e375a9cffab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352656"
---
# <a name="chstringarray-methods"></a><span data-ttu-id="b2476-103">Chstringarray-Methoden</span><span class="sxs-lookup"><span data-stu-id="b2476-103">CHStringArray Methods</span></span>

<span data-ttu-id="b2476-104">\[Die [**chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="b2476-104">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b2476-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="b2476-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b2476-106">Die [**chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) -Klasse stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="b2476-106">The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2476-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b2476-107">In this section</span></span>

-   [<span data-ttu-id="b2476-108">**Add-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-108">**Add method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
-   [<span data-ttu-id="b2476-109">**Append-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-109">**Append method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-append)
-   [<span data-ttu-id="b2476-110">**Chstringarray-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-110">**CHStringArray method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-chstringarray)
-   [<span data-ttu-id="b2476-111">**Copy-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-111">**Copy method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-copy)
-   <span data-ttu-id="b2476-112">[**ElementAt-Methode**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span><span class="sxs-lookup"><span data-stu-id="b2476-112">[**ElementAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-elementat(int))</span></span>
-   [<span data-ttu-id="b2476-113">**Methode "freextra"**</span><span class="sxs-lookup"><span data-stu-id="b2476-113">**FreeExtra method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-freeextra)
-   <span data-ttu-id="b2476-114">[**GetAt-Methode**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="b2476-114">[**GetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
-   [<span data-ttu-id="b2476-115">**GetData-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-115">**GetData method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getdata)
-   [<span data-ttu-id="b2476-116">**GetSize-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-116">**GetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getsize)
-   [<span data-ttu-id="b2476-117">**GetUpperBound-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-117">**GetUpperBound method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)
-   <span data-ttu-id="b2476-118">[**InsertAt-Methoden**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span><span class="sxs-lookup"><span data-stu-id="b2476-118">[**InsertAt methods**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-insertat(int_chstringarray))</span></span>
-   <span data-ttu-id="b2476-119">[**Chstringarray::-Operator \[\]**](chstringarray--operator-brackets.md)</span><span class="sxs-lookup"><span data-stu-id="b2476-119">[**CHStringArray::operator \[ \]**](chstringarray--operator-brackets.md)</span></span>
-   [<span data-ttu-id="b2476-120">**RemoveAll-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-120">**RemoveAll method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeall)
-   [<span data-ttu-id="b2476-121">**RemoveAt-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-121">**RemoveAt method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-removeat)
-   <span data-ttu-id="b2476-122">[**Methode "-Methode"**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="b2476-122">[**SetAt method**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
-   [<span data-ttu-id="b2476-123">**Die Methode "antatgrow"**</span><span class="sxs-lookup"><span data-stu-id="b2476-123">**SetAtGrow method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setatgrow)
-   [<span data-ttu-id="b2476-124">**SetSize-Methode**</span><span class="sxs-lookup"><span data-stu-id="b2476-124">**SetSize method**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setsize)

 

 
