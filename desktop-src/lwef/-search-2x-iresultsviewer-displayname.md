---
title: Iresultsviewer DisplayName-Eigenschaft (wdsview. h)
description: Lokalisierter Anzeige Name des Typs.
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Features
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Features, Display Name-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341380"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="33ad1-106">Iresultviewer::D isplayname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="33ad1-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="33ad1-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="33ad1-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="33ad1-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="33ad1-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="33ad1-109">Lokalisierter Anzeige Name des Typs.</span><span class="sxs-lookup"><span data-stu-id="33ad1-109">Localized display name of the type.</span></span>

<span data-ttu-id="33ad1-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="33ad1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ad1-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="33ad1-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="33ad1-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="33ad1-112">Property value</span></span>

<span data-ttu-id="33ad1-113">Ein Zeiger auf einen Wert, der den lokalisierten anzeigen Amen für den Typ empfängt.</span><span class="sxs-lookup"><span data-stu-id="33ad1-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ad1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33ad1-114">Requirements</span></span>



| <span data-ttu-id="33ad1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33ad1-115">Requirement</span></span> | <span data-ttu-id="33ad1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="33ad1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33ad1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33ad1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33ad1-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="33ad1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33ad1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33ad1-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33ad1-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="33ad1-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="33ad1-121">Redistributable</span></span><br/>          | <span data-ttu-id="33ad1-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="33ad1-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="33ad1-123">Header</span><span class="sxs-lookup"><span data-stu-id="33ad1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="33ad1-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="33ad1-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





