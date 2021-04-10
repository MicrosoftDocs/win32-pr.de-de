---
title: Iresulttype-Uid-Eigenschaft (wdssharedidl. h)
description: Diese Eigenschaft enthält den eindeutigen Bezeichner für den Typ.
ms.assetid: 31c2ef7d-f5a7-441e-80ea-fd7e46fded07
keywords:
- UID-Eigenschafts Funktionen der Legacy-Windows-Umgebung
- UID-Eigenschaft Legacy-Windows-Umgebungs Features, iresulttype-Schnittstelle
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features, UID-Eigenschaft
topic_type:
- apiref
api_name:
- IResultType.UID
- IResultType.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbdd5a9b17da9cde04ac0b371a885b07415d0e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106304"
---
# <a name="iresulttypeuid-property"></a><span data-ttu-id="0ac7c-106">Iresulttype:: UID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0ac7c-106">IResultType::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="0ac7c-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="0ac7c-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="0ac7c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="0ac7c-109">Diese Eigenschaft enthält den eindeutigen Bezeichner für den Typ.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-109">This property contains the unique identifier for the type.</span></span>

<span data-ttu-id="0ac7c-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ac7c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ac7c-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="0ac7c-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0ac7c-112">Property value</span></span>

<span data-ttu-id="0ac7c-113">die Adresse des Speicher Orts, der die UID enthält.</span><span class="sxs-lookup"><span data-stu-id="0ac7c-113">the address of the location containing the uid.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ac7c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ac7c-114">Requirements</span></span>



| <span data-ttu-id="0ac7c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ac7c-115">Requirement</span></span> | <span data-ttu-id="0ac7c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0ac7c-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ac7c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ac7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0ac7c-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ac7c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0ac7c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ac7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0ac7c-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ac7c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ac7c-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="0ac7c-121">Redistributable</span></span><br/>          | <span data-ttu-id="0ac7c-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="0ac7c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="0ac7c-123">Header</span><span class="sxs-lookup"><span data-stu-id="0ac7c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ac7c-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ac7c-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





