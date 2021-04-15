---
title: Iresultverb-Symbol Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt einen Zeiger auf das Handle des optionalen Symbols zurück, das dem Verb zugeordnet ist.
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Symbol Eigenschaft Legacy Windows-Umgebungs Features
- Symbol Eigenschaft Legacy Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Funktionen, Symbol Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477667"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="aff21-106">Iresultverb:: Icon-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="aff21-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="aff21-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="aff21-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="aff21-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="aff21-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="aff21-109">Diese Eigenschaft gibt einen Zeiger auf das Handle des optionalen Symbols zurück, das dem Verb zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="aff21-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="aff21-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="aff21-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff21-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="aff21-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="aff21-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="aff21-112">Property value</span></span>

<span data-ttu-id="aff21-113">HICON ist ein Zeiger auf das Handle des optionalen Symbols mit dem Verb.</span><span class="sxs-lookup"><span data-stu-id="aff21-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff21-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aff21-114">Requirements</span></span>



| <span data-ttu-id="aff21-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aff21-115">Requirement</span></span> | <span data-ttu-id="aff21-116">Wert</span><span class="sxs-lookup"><span data-stu-id="aff21-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff21-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aff21-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aff21-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff21-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="aff21-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aff21-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aff21-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aff21-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aff21-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="aff21-121">Redistributable</span></span><br/>          | <span data-ttu-id="aff21-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="aff21-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="aff21-123">Header</span><span class="sxs-lookup"><span data-stu-id="aff21-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aff21-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aff21-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





