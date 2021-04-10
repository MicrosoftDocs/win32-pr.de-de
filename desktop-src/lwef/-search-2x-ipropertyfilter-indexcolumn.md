---
title: Ipropertyfilter-indexcolumn-Eigenschaft (wdssharedidl. h)
description: Der Name der indizierten Spalte der Eigenschaft, nach der gefiltert werden soll.
ms.assetid: 18ce0c89-bdaa-4f83-bf03-c11b55a842f5
keywords:
- Indexcolumn-Eigenschaft Legacy-Windows-Umgebungs Features
- Indexcolumn-Eigenschaft Legacy-Windows-Umgebungs Features, ipropertyfilter-Schnittstelle
- Ipropertyfilter Interface Legacy Windows-Umgebungs Funktionen, indexcolumn (Eigenschaft)
topic_type:
- apiref
api_name:
- IPropertyFilter.IndexColumn
- IPropertyFilter.get_IndexColumn
- IPropertyFilter.put_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e55a59b4615f4b6c19dcb5f07d16394d2531f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040558"
---
# <a name="ipropertyfilterindexcolumn-property"></a><span data-ttu-id="c2627-106">Ipropertyfilter:: indexcolumn-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2627-106">IPropertyFilter::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="c2627-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="c2627-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c2627-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c2627-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c2627-109">Der Name der indizierten Spalte der Eigenschaft, nach der gefiltert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2627-109">Indexed column name of the property to filter by.</span></span>

<span data-ttu-id="c2627-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c2627-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2627-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2627-111">Syntax</span></span>


```C++
HRESULT put_IndexColumn(
  [in]          BSTR column
);

HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="c2627-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2627-112">Property value</span></span>

<span data-ttu-id="c2627-113">Legt die Spalten Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="c2627-113">Sets the Column property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2627-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2627-114">Requirements</span></span>



| <span data-ttu-id="c2627-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2627-115">Requirement</span></span> | <span data-ttu-id="c2627-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c2627-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2627-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2627-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c2627-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2627-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c2627-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2627-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c2627-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2627-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2627-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c2627-121">Redistributable</span></span><br/>          | <span data-ttu-id="c2627-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c2627-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c2627-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2627-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2627-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2627-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





