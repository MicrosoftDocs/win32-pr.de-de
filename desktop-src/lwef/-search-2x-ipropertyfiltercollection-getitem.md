---
title: Ipropertyfiltercollection GetItem-Eigenschaft (wdssharedidl. h)
description: Gibt einen bestimmten Filter in der Auflistung zurück.
ms.assetid: 72a35d98-b2d8-4dfb-84a7-365a3778fc85
keywords:
- GetItem-Eigenschaft Legacy Windows-Umgebungs Features
- GetItem-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfiltercollection-Schnittstelle
- Ipropertyfiltercollection-Schnittstelle Legacy Windows-Umgebungs Features, GetItem-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilterCollection.GetITem
- IPropertyFilterCollection.get_GetITem
- IPropertyFilterCollection.put_GetITem
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8027bf175efc615c1324f55229c7e307a123c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949727"
---
# <a name="ipropertyfiltercollectiongetitem-property"></a><span data-ttu-id="8877b-106">Ipropertyfiltercollection:: GetItem-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8877b-106">IPropertyFilterCollection::GetITem property</span></span>

> [!NOTE]
> <span data-ttu-id="8877b-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="8877b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8877b-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8877b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8877b-109">Gibt einen bestimmten Filter in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="8877b-109">Returns a specific filter within the collection.</span></span>

<span data-ttu-id="8877b-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8877b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8877b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8877b-111">Syntax</span></span>


```C++
HRESULT put_GetITem(
  [in]          long            index
);

HRESULT get_GetITem(
  [out, retval] IPropertyFilter **filter
);
```



## <a name="property-value"></a><span data-ttu-id="8877b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8877b-112">Property value</span></span>

<span data-ttu-id="8877b-113">Legt die Adresse des Filters fest.</span><span class="sxs-lookup"><span data-stu-id="8877b-113">Sets the address of the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8877b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8877b-114">Requirements</span></span>



| <span data-ttu-id="8877b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8877b-115">Requirement</span></span> | <span data-ttu-id="8877b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8877b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8877b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8877b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8877b-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8877b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8877b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8877b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8877b-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8877b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8877b-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8877b-121">Redistributable</span></span><br/>          | <span data-ttu-id="8877b-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8877b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="8877b-123">Header</span><span class="sxs-lookup"><span data-stu-id="8877b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8877b-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8877b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





