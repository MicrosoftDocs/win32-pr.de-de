---
title: Iresulttype PropertyCount-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom-Typ verfügbar gemacht werden.
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- PropertyCount-Eigenschaft Legacy Funktionen der Windows-Umgebung
- PropertyCount-Eigenschaft Legacy-Windows-Umgebungs Features, iresulttype-Schnittstelle
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Funktionen, PropertyCount-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517390"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="af72b-106">Iresulttype::P ropertycount-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af72b-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="af72b-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="af72b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="af72b-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="af72b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="af72b-109">Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom-Typ verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="af72b-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="af72b-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="af72b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af72b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="af72b-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="af72b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="af72b-112">Property value</span></span>

<span data-ttu-id="af72b-113">Gibt die Adresse der Anzahl der verfügbar gemachten Eigenschaften zurück.</span><span class="sxs-lookup"><span data-stu-id="af72b-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="af72b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af72b-114">Requirements</span></span>



| <span data-ttu-id="af72b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af72b-115">Requirement</span></span> | <span data-ttu-id="af72b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="af72b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af72b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af72b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af72b-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af72b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="af72b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af72b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af72b-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af72b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af72b-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="af72b-121">Redistributable</span></span><br/>          | <span data-ttu-id="af72b-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="af72b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="af72b-123">Header</span><span class="sxs-lookup"><span data-stu-id="af72b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af72b-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af72b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





