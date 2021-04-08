---
title: Iresultverb-HelpText-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt einen Zeiger auf die lokalisierte Hilfe Zeichenfolge für das Verb zurück.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- HelpText-Eigenschaft Legacy-Windows-Umgebungs Features
- HelpText-Eigenschaft Legacy-Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Features, HelpText-Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741033"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="dfce8-106">Iresultverb:: HelpText-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="dfce8-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="dfce8-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="dfce8-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="dfce8-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="dfce8-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="dfce8-109">Diese Eigenschaft gibt einen Zeiger auf die lokalisierte Hilfe Zeichenfolge für das Verb zurück.</span><span class="sxs-lookup"><span data-stu-id="dfce8-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="dfce8-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dfce8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfce8-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfce8-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="dfce8-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dfce8-112">Property value</span></span>

<span data-ttu-id="dfce8-113">Der Wert dieser Eigenschaft ist ein Zeiger auf die lokalisierte Hilfe Zeichenfolge für dieses Verb.</span><span class="sxs-lookup"><span data-stu-id="dfce8-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfce8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfce8-114">Requirements</span></span>



| <span data-ttu-id="dfce8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfce8-115">Requirement</span></span> | <span data-ttu-id="dfce8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dfce8-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfce8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dfce8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dfce8-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfce8-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dfce8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dfce8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dfce8-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dfce8-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dfce8-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="dfce8-121">Redistributable</span></span><br/>          | <span data-ttu-id="dfce8-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="dfce8-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="dfce8-123">Header</span><span class="sxs-lookup"><span data-stu-id="dfce8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfce8-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfce8-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





