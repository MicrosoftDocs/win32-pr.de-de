---
title: Iresultsviewer-FilterType-Eigenschaft (wdsview. h)
description: Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- FilterType-Eigenschaft Legacy-Windows-Umgebungs Features
- FilterType-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultviewer-Schnittstelle
- Iresultviewer-Schnittstelle ältere Windows-Umgebungs Features, FilterType-Eigenschaft
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345337"
---
# <a name="iresultsviewerfiltertype-property"></a><span data-ttu-id="81d0d-106">Iresultviewer:: FilterType (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81d0d-106">IResultsViewer::FilterType property</span></span>

> [!NOTE]
> <span data-ttu-id="81d0d-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="81d0d-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="81d0d-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="81d0d-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="81d0d-109">Diese Eigenschaft legt den Namen des vorab bereitgestellten Typs fest, nach dem die Ergebnisse gefiltert werden, oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="81d0d-109">This property will set or return the name of the preceived type to filter results by.</span></span>

<span data-ttu-id="81d0d-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="81d0d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d0d-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="81d0d-111">Syntax</span></span>


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="81d0d-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="81d0d-112">Property value</span></span>

<span data-ttu-id="81d0d-113">Legt den wahrgenommenen Typ fest, mit dem die Ergebnisse gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="81d0d-113">Sets the perceived type used to filter results.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d0d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81d0d-114">Requirements</span></span>



| <span data-ttu-id="81d0d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81d0d-115">Requirement</span></span> | <span data-ttu-id="81d0d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="81d0d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81d0d-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81d0d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81d0d-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81d0d-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81d0d-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81d0d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81d0d-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81d0d-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="81d0d-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="81d0d-121">Redistributable</span></span><br/>          | <span data-ttu-id="81d0d-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="81d0d-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="81d0d-123">Header</span><span class="sxs-lookup"><span data-stu-id="81d0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d0d-124"><dt>Wdsview. h</dt></span><span class="sxs-lookup"><span data-stu-id="81d0d-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





