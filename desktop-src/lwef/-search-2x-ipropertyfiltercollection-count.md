---
title: Ipropertyfiltercollection Count-Eigenschaft (wdssharedidl. h)
description: Anzahl der Filter in der Auflistung.
ms.assetid: 9d656f06-eb1d-4cc6-9096-252f0fc65ae2
keywords:
- Count-Eigenschaft Legacy-Windows-Umgebungs Features
- Count-Eigenschaft Legacy-Windows-Umgebungs Features, ipropertyfiltercollection-Schnittstelle
- Ipropertyfiltercollection-Schnittstelle Legacy Windows-Umgebungs Features, Count-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.Count
- IPropertyFilterCollection.get_Count
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258a2ca8089cecb8e2e15fbe7e9e92ce1ed3468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741048"
---
# <a name="ipropertyfiltercollectioncount-property"></a><span data-ttu-id="ce610-106">Ipropertyfiltercollection:: Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ce610-106">IPropertyFilterCollection::Count property</span></span>

> [!NOTE]
> <span data-ttu-id="ce610-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="ce610-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ce610-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="ce610-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ce610-109">Anzahl der Filter in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="ce610-109">Number of filters in the collection.</span></span>

<span data-ttu-id="ce610-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ce610-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce610-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce610-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="ce610-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ce610-112">Property value</span></span>

<span data-ttu-id="ce610-113">Gibt einen Zeiger auf die Anzahl der Filter in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="ce610-113">returns a pointer to the number of filters in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce610-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce610-114">Requirements</span></span>



| <span data-ttu-id="ce610-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce610-115">Requirement</span></span> | <span data-ttu-id="ce610-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce610-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce610-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce610-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce610-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce610-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ce610-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce610-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce610-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce610-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ce610-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ce610-121">Redistributable</span></span><br/>          | <span data-ttu-id="ce610-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="ce610-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="ce610-123">Header</span><span class="sxs-lookup"><span data-stu-id="ce610-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce610-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce610-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





