---
title: Iresultverb DisplayName-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt einen Zeiger auf den lokalisierten anzeigen Amen für das Verb zurück.
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Features
- Display Name-Eigenschaft Legacy-Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Features, Display Name-Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040461"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="c2f9b-106">Iresultverb::D isplayname-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2f9b-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="c2f9b-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="c2f9b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="c2f9b-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f9b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="c2f9b-109">Diese Eigenschaft gibt einen Zeiger auf den lokalisierten anzeigen Amen für das Verb zurück.</span><span class="sxs-lookup"><span data-stu-id="c2f9b-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="c2f9b-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2f9b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f9b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2f9b-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="c2f9b-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="c2f9b-112">Property value</span></span>

<span data-ttu-id="c2f9b-113">Diese Eigenschaft gibt einen Zeiger auf den lokalisierten anzeigen Amen für das Verb zurück.</span><span class="sxs-lookup"><span data-stu-id="c2f9b-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f9b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2f9b-114">Requirements</span></span>



| <span data-ttu-id="c2f9b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2f9b-115">Requirement</span></span> | <span data-ttu-id="c2f9b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c2f9b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f9b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2f9b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f9b-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2f9b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c2f9b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2f9b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f9b-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2f9b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2f9b-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="c2f9b-121">Redistributable</span></span><br/>          | <span data-ttu-id="c2f9b-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="c2f9b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="c2f9b-123">Header</span><span class="sxs-lookup"><span data-stu-id="c2f9b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2f9b-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2f9b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





