---
description: Gibt einen Wert zurück, der die Funktionen der Tablet-Hardware darstellt.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet:: gethardwarecaps-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867723"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="68298-103">ITablet:: gethardwarecaps-Methode</span><span class="sxs-lookup"><span data-stu-id="68298-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="68298-104">Gibt einen Wert zurück, der die Funktionen der Tablet-Hardware darstellt.</span><span class="sxs-lookup"><span data-stu-id="68298-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="68298-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68298-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="68298-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68298-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68298-107">*pdwcaps* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68298-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68298-108">Bitflags, die die Funktionen der Tablet-Hardware darstellen.</span><span class="sxs-lookup"><span data-stu-id="68298-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68298-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68298-109">Return value</span></span>

<span data-ttu-id="68298-110">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68298-110">This method can return one of these values.</span></span>



| <span data-ttu-id="68298-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="68298-111">Return code</span></span>                                                                            | <span data-ttu-id="68298-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68298-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="68298-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68298-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="68298-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="68298-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="68298-115"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="68298-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="68298-116">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="68298-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68298-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68298-117">Remarks</span></span>

<span data-ttu-id="68298-118">Der *pdwcaps* -Parameter ist ein Satz von Bitflags, die Tablet-Hardwarefunktionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="68298-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="68298-119">In der folgenden Tabelle werden diese Flags beschrieben.</span><span class="sxs-lookup"><span data-stu-id="68298-119">The following table describes these flags.</span></span>



| <span data-ttu-id="68298-120">FlagName</span><span class="sxs-lookup"><span data-stu-id="68298-120">Flag Name</span></span>                         | <span data-ttu-id="68298-121">Wert</span><span class="sxs-lookup"><span data-stu-id="68298-121">Value</span></span>                 | <span data-ttu-id="68298-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68298-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68298-123">Integration in thwc \_</span><span class="sxs-lookup"><span data-stu-id="68298-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="68298-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="68298-124">0x00000001</span></span><br/> | <span data-ttu-id="68298-125">Gibt an, dass die Anzeige und der Digitalisierer dieselbe Oberfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="68298-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="68298-126">thwc- \_ CSR \_ muss \_ berühren</span><span class="sxs-lookup"><span data-stu-id="68298-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="68298-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="68298-127">0x00000002</span></span><br/> | <span data-ttu-id="68298-128">Gibt an, dass sich der Cursor in einem physischen Kontakt mit dem Gerät befinden muss, um die Position zu melden.</span><span class="sxs-lookup"><span data-stu-id="68298-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="68298-129">harte thwc- \_ \_ Nähe</span><span class="sxs-lookup"><span data-stu-id="68298-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="68298-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="68298-130">0x00000004</span></span><br/> | <span data-ttu-id="68298-131">Gibt an, dass das Gerät Ereignisse generieren kann, wenn der Cursor in den Bereich physischer Erkennungsbereich wechselt und diesen verlässt.</span><span class="sxs-lookup"><span data-stu-id="68298-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="68298-132">thwc \_ physid \_ csrs</span><span class="sxs-lookup"><span data-stu-id="68298-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="68298-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="68298-133">0x00000008</span></span><br/> | <span data-ttu-id="68298-134">Gibt an, dass das Gerät den aktiven Cursor in der Hardware eindeutig identifizieren kann.</span><span class="sxs-lookup"><span data-stu-id="68298-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="68298-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68298-135">Requirements</span></span>



| <span data-ttu-id="68298-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68298-136">Requirement</span></span> | <span data-ttu-id="68298-137">Wert</span><span class="sxs-lookup"><span data-stu-id="68298-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68298-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68298-138">Minimum supported client</span></span><br/> | <span data-ttu-id="68298-139">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68298-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="68298-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68298-140">Minimum supported server</span></span><br/> | <span data-ttu-id="68298-141">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68298-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="68298-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68298-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="68298-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="68298-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68298-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68298-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68298-145">**ITablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="68298-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




