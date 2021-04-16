---
title: Ipropertyfilter-Text Eigenschaft (wdssharedidl. h)
description: Text des Filters.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Text Eigenschaft Legacy Windows-Umgebungs Funktionen
- Text Eigenschaft Legacy Windows-Umgebungs Funktionen, ipropertyfilter-Schnittstelle
- Ipropertyfilter Interface Legacy Windows-Umgebungs Funktionen, Text-Eigenschaft
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518314"
---
# <a name="ipropertyfiltertext-property"></a><span data-ttu-id="8cc3e-106">Ipropertyfilter:: Text-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8cc3e-106">IPropertyFilter::Text property</span></span>

> [!NOTE]
> <span data-ttu-id="8cc3e-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="8cc3e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8cc3e-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="8cc3e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="8cc3e-109">Text des Filters.</span><span class="sxs-lookup"><span data-stu-id="8cc3e-109">Text of the filter.</span></span>

<span data-ttu-id="8cc3e-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8cc3e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc3e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc3e-111">Syntax</span></span>


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="8cc3e-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8cc3e-112">Property value</span></span>

<span data-ttu-id="8cc3e-113">Legt den Filter Text fest.</span><span class="sxs-lookup"><span data-stu-id="8cc3e-113">Sets the filter text.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc3e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8cc3e-114">Requirements</span></span>



| <span data-ttu-id="8cc3e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8cc3e-115">Requirement</span></span> | <span data-ttu-id="8cc3e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8cc3e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc3e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8cc3e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc3e-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cc3e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8cc3e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8cc3e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc3e-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8cc3e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8cc3e-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8cc3e-121">Redistributable</span></span><br/>          | <span data-ttu-id="8cc3e-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="8cc3e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="8cc3e-123">Header</span><span class="sxs-lookup"><span data-stu-id="8cc3e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc3e-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc3e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





