---
description: Tritt auf, wenn der Tablettstift den physischen Erkennungsbereich (Nähe) des Tablets verlässt.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'Itableteventsink:: Cursor-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868679"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="79cf7-103">Itableteventsink:: Cursor-Methode</span><span class="sxs-lookup"><span data-stu-id="79cf7-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="79cf7-104">Tritt auf, wenn der Tablettstift den physischen Erkennungsbereich (Nähe) des Tablets verlässt.</span><span class="sxs-lookup"><span data-stu-id="79cf7-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="79cf7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79cf7-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="79cf7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79cf7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79cf7-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79cf7-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79cf7-108">Der Bezeichner des Tablets.</span><span class="sxs-lookup"><span data-stu-id="79cf7-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="79cf7-109">*zid*</span><span class="sxs-lookup"><span data-stu-id="79cf7-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="79cf7-110">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="79cf7-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79cf7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79cf7-111">Return value</span></span>

<span data-ttu-id="79cf7-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="79cf7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="79cf7-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="79cf7-113">Return code</span></span>                                                                            | <span data-ttu-id="79cf7-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79cf7-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="79cf7-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79cf7-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="79cf7-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="79cf7-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="79cf7-117"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="79cf7-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="79cf7-118">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="79cf7-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79cf7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79cf7-119">Requirements</span></span>



| <span data-ttu-id="79cf7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79cf7-120">Requirement</span></span> | <span data-ttu-id="79cf7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="79cf7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79cf7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79cf7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="79cf7-123">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79cf7-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="79cf7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79cf7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="79cf7-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="79cf7-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="79cf7-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79cf7-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="79cf7-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79cf7-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79cf7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79cf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79cf7-129">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="79cf7-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




