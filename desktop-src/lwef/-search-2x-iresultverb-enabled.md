---
title: Iresultverb-aktivierte Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt true zurück, wenn das Verb aktiviert ist.
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- Aktivierte Eigenschaften Legacy-Windows-Umgebungs Features
- Aktivierte Eigenschaft ältere Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Features, aktivierte Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956740"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="406c6-106">Iresultverb:: aktivierte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="406c6-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="406c6-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="406c6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="406c6-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="406c6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="406c6-109">Diese Eigenschaft gibt true zurück, wenn das Verb aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="406c6-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="406c6-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="406c6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="406c6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="406c6-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="406c6-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="406c6-112">Property value</span></span>

<span data-ttu-id="406c6-113">Diese Eigenschaft gibt true zurück, wenn das Verb aktiviert ist, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="406c6-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="406c6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="406c6-114">Requirements</span></span>



| <span data-ttu-id="406c6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="406c6-115">Requirement</span></span> | <span data-ttu-id="406c6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="406c6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="406c6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="406c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="406c6-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="406c6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="406c6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="406c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="406c6-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="406c6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="406c6-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="406c6-121">Redistributable</span></span><br/>          | <span data-ttu-id="406c6-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="406c6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="406c6-123">Header</span><span class="sxs-lookup"><span data-stu-id="406c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="406c6-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="406c6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





