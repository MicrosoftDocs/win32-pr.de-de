---
title: Eigenschaft ' ipropertyfilter UID ' (wdssharedidl. h)
description: UID für die Eigenschaft, nach der gefiltert werden soll.
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- UID-Eigenschafts Funktionen der Legacy-Windows-Umgebung
- UID-Eigenschaft Legacy-Windows-Umgebungs Features, ipropertyfilter-Schnittstelle
- Ipropertyfilter-Schnittstelle ältere Windows-Umgebungs Features, UID-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340898"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="4a422-106">Ipropertyfilter:: UID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4a422-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="4a422-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="4a422-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4a422-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4a422-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4a422-109">UID für die Eigenschaft, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a422-109">UID for the property to filter by.</span></span>

<span data-ttu-id="4a422-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4a422-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a422-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a422-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="4a422-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4a422-112">Property value</span></span>

<span data-ttu-id="4a422-113">Legt die UID-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="4a422-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a422-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a422-114">Requirements</span></span>



| <span data-ttu-id="4a422-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a422-115">Requirement</span></span> | <span data-ttu-id="4a422-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4a422-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a422-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a422-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a422-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a422-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a422-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a422-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a422-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a422-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4a422-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4a422-121">Redistributable</span></span><br/>          | <span data-ttu-id="4a422-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="4a422-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="4a422-123">Header</span><span class="sxs-lookup"><span data-stu-id="4a422-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a422-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a422-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





