---
title: Iresultproperty-Hinweis Eigenschaft (wdssharedidl. h)
description: Spezieller Wert, der für das Abrufen von Daten verwendet wird.
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- Hinweis Eigenschaft Legacy-Windows-Umgebungs Features
- Hinweis Eigenschaft Legacy-Windows-Umgebungs Features, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, Hint-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339956"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="4033e-106">Iresultproperty:: Hint-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4033e-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="4033e-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="4033e-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4033e-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4033e-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4033e-109">Spezieller Wert, der für das Abrufen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4033e-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="4033e-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="4033e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4033e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="4033e-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="4033e-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="4033e-112">Property value</span></span>

<span data-ttu-id="4033e-113">Gibt einen Zeiger auf den Hinweis zurück.</span><span class="sxs-lookup"><span data-stu-id="4033e-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="4033e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4033e-114">Requirements</span></span>



| <span data-ttu-id="4033e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4033e-115">Requirement</span></span> | <span data-ttu-id="4033e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4033e-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4033e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4033e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4033e-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4033e-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4033e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4033e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4033e-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4033e-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="4033e-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4033e-121">Redistributable</span></span><br/>          | <span data-ttu-id="4033e-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="4033e-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="4033e-123">Header</span><span class="sxs-lookup"><span data-stu-id="4033e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4033e-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4033e-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





