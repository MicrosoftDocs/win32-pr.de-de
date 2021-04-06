---
title: Iresulttype preceivedtype-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- Preceivedtype-Eigenschaft Legacy-Windows-Umgebungs Features
- Preceivedtype-Eigenschaft Legacy Windows-Umgebungs Features, iresulttype-Schnittstelle
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features, preceivedtype (Eigenschaft)
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858794"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="2b379-106">Iresulttype::P receivedtype-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2b379-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="2b379-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="2b379-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="2b379-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="2b379-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="2b379-109">Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2b379-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="2b379-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2b379-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b379-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b379-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="2b379-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2b379-112">Property value</span></span>

<span data-ttu-id="2b379-113">Gibt die Adresse der Zeichenfolge identifyint des Typs im Index zurück.</span><span class="sxs-lookup"><span data-stu-id="2b379-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b379-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b379-114">Requirements</span></span>



| <span data-ttu-id="2b379-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b379-115">Requirement</span></span> | <span data-ttu-id="2b379-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2b379-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b379-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b379-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b379-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b379-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2b379-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b379-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b379-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b379-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2b379-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="2b379-121">Redistributable</span></span><br/>          | <span data-ttu-id="2b379-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="2b379-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="2b379-123">Header</span><span class="sxs-lookup"><span data-stu-id="2b379-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b379-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b379-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





