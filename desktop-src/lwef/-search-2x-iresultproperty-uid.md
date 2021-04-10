---
title: Iresultproperty Uid-Eigenschaft (wdssharedidl. h)
description: Eindeutiger Bezeichner für die Eigenschaft.
ms.assetid: b5cee5b3-78b4-4d2a-b442-f6624497ef71
keywords:
- UID-Eigenschafts Funktionen der Legacy-Windows-Umgebung
- UID-Eigenschaft Legacy-Windows-Umgebungs Funktionen, iresultproperty-Schnittstelle
- Iresultproperty-Schnittstelle Legacy Windows-Umgebungs Features, UID-Eigenschaft
topic_type:
- apiref
api_name:
- IResultProperty.UID
- IResultProperty.get_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08921e366cca2be40a8a79fe43d7a15cec54f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040463"
---
# <a name="iresultpropertyuid-property"></a><span data-ttu-id="7ad40-106">Iresultproperty:: UID-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7ad40-106">IResultProperty::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="7ad40-107">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="7ad40-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7ad40-108">Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7ad40-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7ad40-109">Eindeutiger Bezeichner für die Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ad40-109">Unique identifier for the property.</span></span>

<span data-ttu-id="7ad40-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7ad40-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad40-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ad40-111">Syntax</span></span>


```C++
HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="7ad40-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7ad40-112">Property value</span></span>

<span data-ttu-id="7ad40-113">Gibt einen Zeiger auf den eindeutigen Bezeichner der Eigenschaft zurück.</span><span class="sxs-lookup"><span data-stu-id="7ad40-113">returns a pointer to the unique property identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ad40-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ad40-114">Requirements</span></span>



| <span data-ttu-id="7ad40-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ad40-115">Requirement</span></span> | <span data-ttu-id="7ad40-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7ad40-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ad40-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ad40-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ad40-118">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ad40-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7ad40-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ad40-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ad40-120">Windows Server 2003 mit SP1 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ad40-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7ad40-121">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="7ad40-121">Redistributable</span></span><br/>          | <span data-ttu-id="7ad40-122">Windows-Desktop Suche (WDS) 2.6.5</span><span class="sxs-lookup"><span data-stu-id="7ad40-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7ad40-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ad40-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ad40-124"><dt>Wdssharedidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ad40-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





