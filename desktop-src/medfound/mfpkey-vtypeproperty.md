---
description: Gibt die Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.
ms.assetid: 29c7fc1c-2047-4562-ba14-48f9cfbfe68c
title: MFPKEY_VTYPE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e95bab3120e60a2faa1a3be47c6459205f5f34d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863440"
---
# <a name="mfpkey_vtype-property"></a><span data-ttu-id="97d26-103">Mfpkey- \_ VType (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="97d26-103">MFPKEY\_VTYPE Property</span></span>

<span data-ttu-id="97d26-104">Gibt die Logik an, die der Codec zum Erkennen von Zeilen Sprung-Quellvideos verwendet.</span><span class="sxs-lookup"><span data-stu-id="97d26-104">Specifies the logic that the codec will use to detect interlaced source video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="97d26-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="97d26-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="97d26-106">g \_ wszwmvcvtype</span><span class="sxs-lookup"><span data-stu-id="97d26-106">g\_wszWMVCVType</span></span>

## <a name="data-type"></a><span data-ttu-id="97d26-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="97d26-107">Data Type</span></span>

<span data-ttu-id="97d26-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="97d26-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="97d26-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="97d26-109">Default Value</span></span>

<span data-ttu-id="97d26-110">0</span><span class="sxs-lookup"><span data-stu-id="97d26-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="97d26-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97d26-111">Remarks</span></span>

<span data-ttu-id="97d26-112">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="97d26-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="97d26-113">Wert</span><span class="sxs-lookup"><span data-stu-id="97d26-113">Value</span></span> | <span data-ttu-id="97d26-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97d26-114">Description</span></span>                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d26-115">0</span><span class="sxs-lookup"><span data-stu-id="97d26-115">0</span></span>     | <span data-ttu-id="97d26-116">Der Codec verwendet die standardmäßige Erkennungs Logik für Frame Typen.</span><span class="sxs-lookup"><span data-stu-id="97d26-116">The codec will use the standard frame-type detection logic.</span></span>                                                                                 |
| <span data-ttu-id="97d26-117">1</span><span class="sxs-lookup"><span data-stu-id="97d26-117">1</span></span>     | <span data-ttu-id="97d26-118">Der Codec behandelt alle Quellvideo Frames als Zeilen Sprung Rahmen.</span><span class="sxs-lookup"><span data-stu-id="97d26-118">The codec will treat all source video frames as interlaced frames.</span></span>                                                                          |
| <span data-ttu-id="97d26-119">2</span><span class="sxs-lookup"><span data-stu-id="97d26-119">2</span></span>     | <span data-ttu-id="97d26-120">Der Codec behandelt alle Quellvideo Frames als Felder mit Zeilen Sprung Video.</span><span class="sxs-lookup"><span data-stu-id="97d26-120">The codec will treat all source video frames as fields of interlaced video.</span></span>                                                                 |
| <span data-ttu-id="97d26-121">3</span><span class="sxs-lookup"><span data-stu-id="97d26-121">3</span></span>     | <span data-ttu-id="97d26-122">Der Codec ermittelt automatisch, ob Eingabe Videorahmen Zeilen Sprung Rahmen oder Felder mit Zeilen Sprung Video sind.</span><span class="sxs-lookup"><span data-stu-id="97d26-122">The codec will automatically determine whether input video frames are interlaced frames or fields of interlaced video.</span></span>                      |
| <span data-ttu-id="97d26-123">4</span><span class="sxs-lookup"><span data-stu-id="97d26-123">4</span></span>     | <span data-ttu-id="97d26-124">Der Codec ermittelt automatisch, ob eingabevideoframes progressive Frames, Zeilen Sprung Rahmen oder Felder mit Zeilen Sprung Videos sind.</span><span class="sxs-lookup"><span data-stu-id="97d26-124">The codec will automatically determine whether input video frames are progressive frames, interlaced frames, or fields of interlaced video.</span></span> |



 

<span data-ttu-id="97d26-125">Diese Eigenschaft bestimmt die Bild Codierungsmethode, die für die Progressive oder Zeilen Sprung Videocodierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97d26-125">This property determines the picture encoding method used for progressive or interlaced video encoding.</span></span>

<span data-ttu-id="97d26-126">Wenn kein Videotyp angegeben wird, verwendet der Codec die Progressive Frame Codierung für Progressive Codierungs Sitzungen und die Feld Zeilen Sprung-Codierung für Zeilen Sprung-Codierungs Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="97d26-126">If no video type is specified, the codec will use progressive frame encoding for progressive encoding sessions, and field interlaced encoding for interlaced encoding sessions.</span></span> <span data-ttu-id="97d26-127">Der Typ der Video Codierungs Sitzung (progressiv oder Zeilen Sprung) wird mithilfe der [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="97d26-127">The type of video encoding session (progressive or interlaced) is set by using the [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="97d26-128">Die [mfpkey \_ interlacedcodingenabled](mfpkey-interlacedcodingenabledproperty.md) -Eigenschaft muss auf Variant true festgelegt werden, um eine Zeilen Sprung \_ Ausgabe zu erzielen. andernfalls hat das Festlegen der "mpfkey"- \_ Eigenschaft "VType" keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="97d26-128">The [MFPKEY\_INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md) property must be set to VARIANT\_TRUE in order to produce interlaced output; otherwise, setting the MPFKEY\_VTYPE property will have no effect.</span></span>

 

<span data-ttu-id="97d26-129">Wenn das Zeilen Sprung Video codiert wird, können mehrere Bild Codierungs Methoden angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="97d26-129">When interlaced video is being encoded, it is possible to specify several picture encoding methods.</span></span> <span data-ttu-id="97d26-130">In der Regel die effizienteste Methode zum Codieren von Zeilen Sprung Videos ist die Verwendung der Methode "Field interschnür" (2).</span><span class="sxs-lookup"><span data-stu-id="97d26-130">Typically the most efficient way to encode interlaced video is to use the field interlaced method (2).</span></span> <span data-ttu-id="97d26-131">Wenn das Quellvideo sehr wenig Bewegung enthält, kann die Frame-interschnür Methode (1) oder die automatische Frame-/Feldmethode (2) besser geeignet sein.</span><span class="sxs-lookup"><span data-stu-id="97d26-131">If the source video contains very little motion, the frame interlaced method (1) or the auto frame/field method (2) might be more suitable.</span></span>

<span data-ttu-id="97d26-132">Beim Codieren gemischter Inhalte (die sowohl Progressive als auch Zeilen Sprung Rahmen enthalten) ist es am besten, den Wert Auto-Frame/Feld/Progressive-Methode (4) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="97d26-132">When encoding mixed content (containing both progressive and interlaced frames), it's best to use the value auto frame/field/progressive method (4).</span></span>

## <a name="requirements"></a><span data-ttu-id="97d26-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97d26-133">Requirements</span></span>



| <span data-ttu-id="97d26-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97d26-134">Requirement</span></span> | <span data-ttu-id="97d26-135">Wert</span><span class="sxs-lookup"><span data-stu-id="97d26-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d26-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97d26-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97d26-137">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97d26-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="97d26-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97d26-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97d26-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97d26-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97d26-140">Header</span><span class="sxs-lookup"><span data-stu-id="97d26-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="97d26-141"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d26-141"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97d26-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97d26-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d26-143">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97d26-143">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




