---
title: Ipropertyfiltercollection-RemoveItem-Eigenschaft (wdssharedidl. h)
description: Entfernt einen bestimmten Filter für die Auflistung.
ms.assetid: a8b8a1f7-d47a-45dc-81c9-f01ecf6c1560
keywords:
- RemoveItem-Eigenschaft Legacy Windows-Umgebungs Features
- RemoveItem-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfiltercollection-Schnittstelle
- Ipropertyfiltercollection-Schnittstelle Legacy Windows-Umgebungs Features, RemoveItem-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.RemoveItem
- IPropertyFilterCollection.put_RemoveItem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2994b636a7b8483d4b3f219648f137166b75790d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742328"
---
# <a name="ipropertyfiltercollectionremoveitem-property"></a><span data-ttu-id="14d4b-106">Ipropertyfiltercollection:: RemoveItem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="14d4b-106">IPropertyFilterCollection::RemoveItem property</span></span>

> [!NOTE]
> <span data-ttu-id="14d4b-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="14d4b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="14d4b-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="14d4b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="14d4b-109">Entfernt einen bestimmten Filter für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="14d4b-109">Removes a specific filter to the collection.</span></span>

<span data-ttu-id="14d4b-110">Diese Eigenschaft ist lesegeschützt.</span><span class="sxs-lookup"><span data-stu-id="14d4b-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d4b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="14d4b-111">Syntax</span></span>


```C++
HRESULT put_RemoveItem(
  [in] long index
);
```



## <a name="property-value"></a><span data-ttu-id="14d4b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="14d4b-112">Property value</span></span>

<span data-ttu-id="14d4b-113">Akzeptiert einen Zeiger auf den Index für den zu entfernenden Filter.</span><span class="sxs-lookup"><span data-stu-id="14d4b-113">Accepts a pointer to the index for the filter to be removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d4b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14d4b-114">Requirements</span></span>



| <span data-ttu-id="14d4b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14d4b-115">Requirement</span></span> | <span data-ttu-id="14d4b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="14d4b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d4b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14d4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14d4b-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="14d4b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14d4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14d4b-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="14d4b-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="14d4b-121">Redistributable</span></span><br/>          | <span data-ttu-id="14d4b-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="14d4b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="14d4b-123">Header</span><span class="sxs-lookup"><span data-stu-id="14d4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d4b-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14d4b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





