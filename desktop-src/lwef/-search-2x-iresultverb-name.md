---
title: Iresultverb Name-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. Drucken, öffnen usw.
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- Namenseigenschaft Legacy-Windows-Umgebungs Features
- Namenseigenschaft Legacy-Windows-Umgebungs Features, iresultverb-Schnittstelle
- Iresultverb Interface Legacy Windows-Umgebungs Features, Name-Eigenschaft
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949473"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="cb6df-106">Iresultverb:: Name-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cb6df-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="cb6df-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="cb6df-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="cb6df-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="cb6df-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="cb6df-109">Diese Eigenschaft gibt einen Zeiger auf den Kontonamen für das Verb zurück, z. b. Drucken, öffnen usw.</span><span class="sxs-lookup"><span data-stu-id="cb6df-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="cb6df-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cb6df-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6df-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb6df-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="cb6df-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cb6df-112">Property value</span></span>

<span data-ttu-id="cb6df-113">Name ist ein Zeiger auf den Kontonamen für das Verb.</span><span class="sxs-lookup"><span data-stu-id="cb6df-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6df-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb6df-114">Requirements</span></span>



| <span data-ttu-id="cb6df-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb6df-115">Requirement</span></span> | <span data-ttu-id="cb6df-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cb6df-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6df-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb6df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6df-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cb6df-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb6df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6df-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb6df-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="cb6df-121">Redistributable</span></span><br/>          | <span data-ttu-id="cb6df-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="cb6df-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="cb6df-123">Header</span><span class="sxs-lookup"><span data-stu-id="cb6df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6df-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6df-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





