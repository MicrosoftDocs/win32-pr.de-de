---
title: PreviewStyle-Eigenschaft von iresultsviewer (wdsview. h)
description: Steuert den Anzeigemodus des Vorschau Bereichs.
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- PreviewStyle-Eigenschaft Legacy-Windows-Umgebungs Features
- PreviewStyle-Eigenschaft Legacy-Windows-Umgebungs Features, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Funktionen, PreviewStyle-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338710"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="19979-106">Iresultviewer::P reviewstyle-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="19979-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="19979-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="19979-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="19979-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="19979-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="19979-109">Steuert den Anzeigemodus des Vorschau Bereichs.</span><span class="sxs-lookup"><span data-stu-id="19979-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="19979-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="19979-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="19979-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="19979-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="19979-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="19979-112">Property value</span></span>

<span data-ttu-id="19979-113">Legt die aktuelle Stil Eigenschaft für den Vorschaubereich fest.</span><span class="sxs-lookup"><span data-stu-id="19979-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="19979-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19979-114">Requirements</span></span>



| <span data-ttu-id="19979-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19979-115">Requirement</span></span> | <span data-ttu-id="19979-116">Wert</span><span class="sxs-lookup"><span data-stu-id="19979-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19979-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19979-117">Minimum supported client</span></span><br/> | <span data-ttu-id="19979-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19979-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19979-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19979-119">Minimum supported server</span></span><br/> | <span data-ttu-id="19979-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19979-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="19979-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="19979-121">Redistributable</span></span><br/>          | <span data-ttu-id="19979-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="19979-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="19979-123">Header</span><span class="sxs-lookup"><span data-stu-id="19979-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19979-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="19979-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





