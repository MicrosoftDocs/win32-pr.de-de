---
title: IResultsViewer SortOrderProperty-Eigenschaft (WdsView.h)
description: Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück.
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- Sortoriderproperty-Eigenschaft Legacy-Windows-Umgebungs Features
- Sortor Property-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle Legacy-Windows-Umgebungs Features, sortoriderproperty (Eigenschaft)
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338146"
---
# <a name="iresultsviewersortorderproperty-property"></a><span data-ttu-id="d91a5-106">Iresultviewer:: sortor Name Property (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d91a5-106">IResultsViewer::SortOrderProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="d91a5-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="d91a5-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d91a5-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="d91a5-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d91a5-109">Diese Eigenschaft legt die Reihenfolge der Spalten fest, nach denen die Ergebnisse sortiert werden, oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="d91a5-109">This property will set or return the order of columns to sort results by.</span></span>

<span data-ttu-id="d91a5-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d91a5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91a5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d91a5-111">Syntax</span></span>


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a><span data-ttu-id="d91a5-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d91a5-112">Property value</span></span>

<span data-ttu-id="d91a5-113">Legt die [**columnsortor der**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="d91a5-113">Sets the [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91a5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d91a5-114">Requirements</span></span>



| <span data-ttu-id="d91a5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d91a5-115">Requirement</span></span> | <span data-ttu-id="d91a5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d91a5-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d91a5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d91a5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d91a5-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d91a5-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d91a5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d91a5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d91a5-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d91a5-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="d91a5-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="d91a5-121">Redistributable</span></span><br/>          | <span data-ttu-id="d91a5-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="d91a5-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="d91a5-123">Header</span><span class="sxs-lookup"><span data-stu-id="d91a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d91a5-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="d91a5-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





