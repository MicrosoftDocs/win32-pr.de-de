---
description: Tritt auf, wenn dem System ein neuer Tablettstift hinzugefügt wird.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'Itableteventsink:: Cursor New-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218369"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="00e2f-103">Itableteventsink:: Cursor New-Methode</span><span class="sxs-lookup"><span data-stu-id="00e2f-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="00e2f-104">Tritt auf, wenn dem System ein neuer Tablettstift hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="00e2f-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e2f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="00e2f-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="00e2f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00e2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e2f-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00e2f-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00e2f-108">Der Bezeichner des Tablet-Kontexts, in dem der neue Tablettstift hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="00e2f-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="00e2f-109">*zid*</span><span class="sxs-lookup"><span data-stu-id="00e2f-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="00e2f-110">Der Bezeichner des neuen tablettstiftobjekts.</span><span class="sxs-lookup"><span data-stu-id="00e2f-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e2f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00e2f-111">Return value</span></span>

<span data-ttu-id="00e2f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="00e2f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="00e2f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="00e2f-113">Return code</span></span>                                                                            | <span data-ttu-id="00e2f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="00e2f-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="00e2f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00e2f-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="00e2f-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="00e2f-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="00e2f-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="00e2f-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="00e2f-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="00e2f-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="00e2f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00e2f-119">Requirements</span></span>



| <span data-ttu-id="00e2f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00e2f-120">Requirement</span></span> | <span data-ttu-id="00e2f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="00e2f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00e2f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00e2f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00e2f-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00e2f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00e2f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00e2f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00e2f-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00e2f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="00e2f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="00e2f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="00e2f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00e2f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e2f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00e2f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e2f-129">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="00e2f-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




