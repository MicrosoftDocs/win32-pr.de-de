---
title: Iresulttype GetProperty-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft enthält angegebene Eigenschafts Informationen.
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- GetProperty-Eigenschaft Legacy-Windows-Umgebungs Features
- GetProperty-Eigenschaft Legacy Windows-Umgebungs Features, iresulttype-Schnittstelle
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Funktionen, GetProperty-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858795"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="708b2-106">Iresulttype:: GetProperty-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="708b2-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="708b2-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="708b2-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="708b2-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="708b2-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="708b2-109">Diese Eigenschaft enthält angegebene Eigenschafts Informationen.</span><span class="sxs-lookup"><span data-stu-id="708b2-109">This property contains specified property information.</span></span>

<span data-ttu-id="708b2-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="708b2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="708b2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="708b2-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="708b2-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="708b2-112">Property value</span></span>

<span data-ttu-id="708b2-113">Legt die Adresse der angegebenen Eigenschaften Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="708b2-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="708b2-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="708b2-114">Requirements</span></span>



| <span data-ttu-id="708b2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="708b2-115">Requirement</span></span> | <span data-ttu-id="708b2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="708b2-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="708b2-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="708b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="708b2-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="708b2-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="708b2-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="708b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="708b2-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="708b2-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="708b2-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="708b2-121">Redistributable</span></span><br/>          | <span data-ttu-id="708b2-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="708b2-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="708b2-123">Header</span><span class="sxs-lookup"><span data-stu-id="708b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="708b2-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="708b2-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





