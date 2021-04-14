---
title: "' Ipropertyfilter '-Eigenschaft ' nestingtiefe ' (wdssharedidl. h)"
description: Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern.
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- Eigenschaften der Legacy-Windows-Umgebung von nestingtiefe
- Nestingtiefe-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfilter-Schnittstelle
- Ipropertyfilter Interface Legacy Windows-Umgebungs Features, nestingtiefe (Eigenschaft)
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391885"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="615d3-106">Ipropertyfilter:: nestingtiefe-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="615d3-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="615d3-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="615d3-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="615d3-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="615d3-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="615d3-109">Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern.</span><span class="sxs-lookup"><span data-stu-id="615d3-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="615d3-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="615d3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="615d3-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="615d3-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="615d3-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="615d3-112">Property value</span></span>

<span data-ttu-id="615d3-113">Legt die Zahl fest, die die Tiefe der geschachtelten Klammern angibt.</span><span class="sxs-lookup"><span data-stu-id="615d3-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="615d3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="615d3-114">Requirements</span></span>



| <span data-ttu-id="615d3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="615d3-115">Requirement</span></span> | <span data-ttu-id="615d3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="615d3-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="615d3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="615d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="615d3-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615d3-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="615d3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="615d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="615d3-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615d3-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="615d3-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="615d3-121">Redistributable</span></span><br/>          | <span data-ttu-id="615d3-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="615d3-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="615d3-123">Header</span><span class="sxs-lookup"><span data-stu-id="615d3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="615d3-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="615d3-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





