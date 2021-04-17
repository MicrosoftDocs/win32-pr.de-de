---
title: Ipropertyfilter logicoperator-Eigenschaft (wdssharedidl. h)
description: Der zum Anwenden eines Filters zu verwendende Logik Operator.
ms.assetid: 9461c7a3-1c70-41bf-a4fe-8dacd4d2ba49
keywords:
- Logicoperator-Eigenschaft Legacy Funktionen der Windows-Umgebung
- Logicoperator-Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfilter-Schnittstelle
- Ipropertyfilter Interface Legacy Windows-Umgebungs Funktionen, logicoperator (Eigenschaft)
topic_type:
- apiref
api_name:
- IPropertyFilter.LogicOperator
- IPropertyFilter.get_LogicOperator
- IPropertyFilter.put_LogicOperator
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c514ae6231a9d83063b4a294680bdd3949c91102
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479173"
---
# <a name="ipropertyfilterlogicoperator-property"></a><span data-ttu-id="53320-106">Ipropertyfilter:: logicoperator (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="53320-106">IPropertyFilter::LogicOperator property</span></span>

> [!NOTE]
> <span data-ttu-id="53320-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="53320-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="53320-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="53320-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="53320-109">Der zum Anwenden eines Filters zu verwendende Logik Operator.</span><span class="sxs-lookup"><span data-stu-id="53320-109">Logic Operator to use when applying a filter.</span></span>

<span data-ttu-id="53320-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="53320-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="53320-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="53320-111">Syntax</span></span>


```C++
HRESULT put_LogicOperator(
  [in]          FilterLogicOperator op
);

HRESULT get_LogicOperator(
  [out, retval] FilterLogicOperator *op
);
```



## <a name="property-value"></a><span data-ttu-id="53320-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="53320-112">Property value</span></span>

<span data-ttu-id="53320-113">Legt den Typ des Logik Operators fest.</span><span class="sxs-lookup"><span data-stu-id="53320-113">Sets the logic operator type.</span></span>

## <a name="requirements"></a><span data-ttu-id="53320-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53320-114">Requirements</span></span>



| <span data-ttu-id="53320-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53320-115">Requirement</span></span> | <span data-ttu-id="53320-116">Wert</span><span class="sxs-lookup"><span data-stu-id="53320-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="53320-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53320-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53320-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53320-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="53320-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53320-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53320-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53320-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="53320-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="53320-121">Redistributable</span></span><br/>          | <span data-ttu-id="53320-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="53320-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="53320-123">Header</span><span class="sxs-lookup"><span data-stu-id="53320-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53320-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53320-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





