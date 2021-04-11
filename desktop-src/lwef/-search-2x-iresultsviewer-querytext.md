---
title: Iresultsviewer-querytext-Eigenschaft (wdsview. h)
description: Ruft den aktuellen Abfragetext ab oder legt ihn fest.
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- Querytext-Eigenschaft Legacy-Windows-Umgebungs Features
- Querytext-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Features, querytext-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105782"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="95d26-106">Iresultviewer:: querytext-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95d26-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="95d26-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="95d26-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="95d26-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="95d26-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="95d26-109">Ruft den aktuellen Abfragetext ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="95d26-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="95d26-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="95d26-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d26-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="95d26-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="95d26-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="95d26-112">Property value</span></span>

<span data-ttu-id="95d26-113">Legt den aktuellen Abfragetext fest.</span><span class="sxs-lookup"><span data-stu-id="95d26-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d26-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95d26-114">Requirements</span></span>



| <span data-ttu-id="95d26-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95d26-115">Requirement</span></span> | <span data-ttu-id="95d26-116">Wert</span><span class="sxs-lookup"><span data-stu-id="95d26-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="95d26-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="95d26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="95d26-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d26-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="95d26-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="95d26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="95d26-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="95d26-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="95d26-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="95d26-121">Redistributable</span></span><br/>          | <span data-ttu-id="95d26-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="95d26-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="95d26-123">Header</span><span class="sxs-lookup"><span data-stu-id="95d26-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d26-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d26-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





