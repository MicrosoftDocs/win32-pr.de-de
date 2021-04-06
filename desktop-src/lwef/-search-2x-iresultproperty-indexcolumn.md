---
title: Iresultproperty-indexcolumn-Eigenschaft (wdssharedidl. h)
description: Eigenschaften Spaltenname im Index.
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- Indexcolumn-Eigenschaft Legacy-Windows-Umgebungs Features
- Indexcolumn-Eigenschaft Legacy-Windows-Umgebungs Features, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Funktionen, indexcolumn-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858796"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="cd3c6-106">Iresultproperty:: indexcolumn-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cd3c6-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="cd3c6-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cd3c6-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="cd3c6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cd3c6-109">Eigenschaften Spaltenname im Index.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-109">Properties column name in the index.</span></span>

<span data-ttu-id="cd3c6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3c6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd3c6-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="cd3c6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cd3c6-112">Property value</span></span>

<span data-ttu-id="cd3c6-113">Gibt einen Zeiger auf den Spaltennamen im Index zurück.</span><span class="sxs-lookup"><span data-stu-id="cd3c6-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd3c6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd3c6-114">Requirements</span></span>



| <span data-ttu-id="cd3c6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd3c6-115">Requirement</span></span> | <span data-ttu-id="cd3c6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cd3c6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3c6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd3c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3c6-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd3c6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cd3c6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd3c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3c6-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd3c6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd3c6-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cd3c6-121">Redistributable</span></span><br/>          | <span data-ttu-id="cd3c6-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="cd3c6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="cd3c6-123">Header</span><span class="sxs-lookup"><span data-stu-id="cd3c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd3c6-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd3c6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





