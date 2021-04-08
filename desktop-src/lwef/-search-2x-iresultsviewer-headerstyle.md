---
title: Iresultsviewer HeaderStyle-Eigenschaft (wdsview. h)
description: Der Header Stil, der in der Ansicht angezeigt wird.
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- HeaderStyle-Eigenschaft, ältere Windows-Umgebungs Features
- HeaderStyle-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle Legacy-Windows-Umgebungs Features, HeaderStyle (Eigenschaft)
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741593"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="8eff0-106">Iresultviewer:: HeaderStyle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8eff0-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="8eff0-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="8eff0-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8eff0-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8eff0-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8eff0-109">Der Header Stil, der in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8eff0-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="8eff0-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8eff0-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff0-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eff0-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="8eff0-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8eff0-112">Property value</span></span>

<span data-ttu-id="8eff0-113">Legt den Stil des angezeigten Headers fest.</span><span class="sxs-lookup"><span data-stu-id="8eff0-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eff0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eff0-114">Requirements</span></span>



| <span data-ttu-id="8eff0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eff0-115">Requirement</span></span> | <span data-ttu-id="8eff0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8eff0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8eff0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8eff0-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eff0-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8eff0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8eff0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8eff0-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8eff0-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="8eff0-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8eff0-121">Redistributable</span></span><br/>          | <span data-ttu-id="8eff0-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8eff0-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="8eff0-123">Header</span><span class="sxs-lookup"><span data-stu-id="8eff0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eff0-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eff0-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





