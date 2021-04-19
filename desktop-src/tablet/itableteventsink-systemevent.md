---
description: Tritt auf, wenn ein System Ereignis verfügbar ist.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Itableteventsink:: systemevent-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359165"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="eeb6c-103">Itableteventsink:: systemevent-Methode</span><span class="sxs-lookup"><span data-stu-id="eeb6c-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="eeb6c-104">Tritt auf, wenn ein System Ereignis verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb6c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="eeb6c-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="eeb6c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eeb6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb6c-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb6c-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6c-108">Der Bezeichner des Tablets.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6c-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb6c-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6c-110">Der Bezeichner des Tablettstifts.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6c-111">*Ereignis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb6c-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6c-112">Der System Ereignis Code.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="eeb6c-113">*EventData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeb6c-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeb6c-114">Die System Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb6c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eeb6c-115">Return value</span></span>

<span data-ttu-id="eeb6c-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="eeb6c-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="eeb6c-117">Return code</span></span>                                                                            | <span data-ttu-id="eeb6c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eeb6c-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="eeb6c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6c-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="eeb6c-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="eeb6c-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6c-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="eeb6c-122">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eeb6c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eeb6c-123">Remarks</span></span>

<span data-ttu-id="eeb6c-124">Die folgende Liste enthält die gültigen Werte für den Ereignis Parameter.</span><span class="sxs-lookup"><span data-stu-id="eeb6c-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="eeb6c-125">SE \_ tippen</span><span class="sxs-lookup"><span data-stu-id="eeb6c-125">SE\_TAP</span></span>
-   <span data-ttu-id="eeb6c-126">SE \_ DBL \_ Tap</span><span class="sxs-lookup"><span data-stu-id="eeb6c-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="eeb6c-127">SE \_ right \_ Tap</span><span class="sxs-lookup"><span data-stu-id="eeb6c-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="eeb6c-128">SE \_ ziehen</span><span class="sxs-lookup"><span data-stu-id="eeb6c-128">SE\_DRAG</span></span>
-   <span data-ttu-id="eeb6c-129">\_Drag right \_ Drag</span><span class="sxs-lookup"><span data-stu-id="eeb6c-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="eeb6c-130">SE \_ Hold- \_ EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="eeb6c-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="eeb6c-131">SE \_ Hold \_ Leave</span><span class="sxs-lookup"><span data-stu-id="eeb6c-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="eeb6c-132">SE \_ Hover \_ EINGABETASTE</span><span class="sxs-lookup"><span data-stu-id="eeb6c-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="eeb6c-133">SE- \_ Hover \_ verlassen</span><span class="sxs-lookup"><span data-stu-id="eeb6c-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="eeb6c-134">SE \_ mittlere \_ Maustaste</span><span class="sxs-lookup"><span data-stu-id="eeb6c-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="eeb6c-135">SE- \_ Taste</span><span class="sxs-lookup"><span data-stu-id="eeb6c-135">SE\_KEY</span></span>
-   <span data-ttu-id="eeb6c-136">SE- \_ \_ Modifizierertaste</span><span class="sxs-lookup"><span data-stu-id="eeb6c-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="eeb6c-137">SE- \_ Gesten \_ Modus</span><span class="sxs-lookup"><span data-stu-id="eeb6c-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="eeb6c-138">SE- \_ Cursor</span><span class="sxs-lookup"><span data-stu-id="eeb6c-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb6c-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeb6c-139">Requirements</span></span>



| <span data-ttu-id="eeb6c-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeb6c-140">Requirement</span></span> | <span data-ttu-id="eeb6c-141">Wert</span><span class="sxs-lookup"><span data-stu-id="eeb6c-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb6c-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eeb6c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb6c-143">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeb6c-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="eeb6c-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eeb6c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb6c-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="eeb6c-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="eeb6c-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eeb6c-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="eeb6c-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eeb6c-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb6c-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eeb6c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb6c-149">**Itableteventsink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eeb6c-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




