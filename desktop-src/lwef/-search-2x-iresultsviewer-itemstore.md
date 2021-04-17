---
title: Iresultsviewer-itemstore-Eigenschaft (wdsview. h)
description: Diese Eigenschaft legt den Namen des Stores fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.
ms.assetid: c2a60485-c8f7-4951-a75e-2e6f6dcc2e4f
keywords:
- Itemstore-Eigenschaft Legacy-Windows-Umgebungs Features
- Itemstore-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Features, itemstore-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.ItemStore
- IResultsViewer.get_ItemStore
- IResultsViewer.put_ItemStore
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99abd4ef7ee36a0c76efa391d98a9fdb1d75f34e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476506"
---
# <a name="iresultsvieweritemstore-property"></a><span data-ttu-id="ddd6c-106">Iresultviewer:: itemstore-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ddd6c-106">IResultsViewer::ItemStore property</span></span>

> [!NOTE]
> <span data-ttu-id="ddd6c-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="ddd6c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ddd6c-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd6c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="ddd6c-109">Diese Eigenschaft legt den Namen des Stores fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="ddd6c-109">This property will set or return the name of the store to filter results by.</span></span>

<span data-ttu-id="ddd6c-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ddd6c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd6c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd6c-111">Syntax</span></span>


```C++
HRESULT put_ItemStore(
  [in]          BSTR name
);

HRESULT get_ItemStore(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="ddd6c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ddd6c-112">Property value</span></span>

<span data-ttu-id="ddd6c-113">Legt die Namen des Stores fest.</span><span class="sxs-lookup"><span data-stu-id="ddd6c-113">Sets the names of the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd6c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddd6c-114">Requirements</span></span>



| <span data-ttu-id="ddd6c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddd6c-115">Requirement</span></span> | <span data-ttu-id="ddd6c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ddd6c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd6c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddd6c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd6c-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd6c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ddd6c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddd6c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd6c-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddd6c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ddd6c-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="ddd6c-121">Redistributable</span></span><br/>          | <span data-ttu-id="ddd6c-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="ddd6c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="ddd6c-123">Header</span><span class="sxs-lookup"><span data-stu-id="ddd6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddd6c-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd6c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





