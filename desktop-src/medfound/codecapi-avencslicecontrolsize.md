---
description: Gibt die Größe des Slice in Einheiten von Megabyte (MB), Bits oder MB an.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: CODECAPI_AVEncSliceControlSize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127977"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="e4c2b-103">Codecapi \_ avencslicecontrolsize (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e4c2b-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="e4c2b-104">Gibt die Größe des Slice in Einheiten von Megabyte (MB), Bits oder MB an.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="e4c2b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e4c2b-105">Data type</span></span>

<span data-ttu-id="e4c2b-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="e4c2b-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e4c2b-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="e4c2b-107">Property GUID</span></span>

<span data-ttu-id="e4c2b-108">**Codecapi \_ avencslicecontrolsize**</span><span class="sxs-lookup"><span data-stu-id="e4c2b-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="e4c2b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4c2b-109">Remarks</span></span>

<span data-ttu-id="e4c2b-110">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="e4c2b-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="e4c2b-111">Die Bedeutung des Werts von codecapi \_ avencslicecontrolsize wird von der [codecapi-Eigenschaft " \_ avencslicecontrolmode](codecapi-avencslicecontrolmode.md) " gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="e4c2b-112">In der folgenden Tabelle wird veranschaulicht, wie die Eigenschaften codecapi \_ avencslicecontrolsize und codecapi \_ avencslicecontrolmode die Größe und die Anzahl der Slices in einem Frame steuern.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="e4c2b-113">Codecapi \_ avencslicecontrolmode-Einstellung</span><span class="sxs-lookup"><span data-stu-id="e4c2b-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="e4c2b-114">Bedeutung des Werts</span><span class="sxs-lookup"><span data-stu-id="e4c2b-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c2b-115">0</span><span class="sxs-lookup"><span data-stu-id="e4c2b-115">0</span></span>                                       | <span data-ttu-id="e4c2b-116">Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Makroblocks angibt.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="e4c2b-117">Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblöcke im Frame ist.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="e4c2b-118">1</span><span class="sxs-lookup"><span data-stu-id="e4c2b-118">1</span></span>                                       | <span data-ttu-id="e4c2b-119">Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Bits angibt.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="e4c2b-120">Der Encoder sollte einen neuen Slice im Makroblock starten, der bewirkt, dass die Anzahl der Bits im Slice diesen Wert überschreitet (sodass die Größe jedes Slice immer kleiner als oder gleich diesem Wert ist).</span><span class="sxs-lookup"><span data-stu-id="e4c2b-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="e4c2b-121">Dies bedeutet, dass die letzte Slice-Größe erheblich kleiner als dieser Wert sein könnte.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="e4c2b-122">2</span><span class="sxs-lookup"><span data-stu-id="e4c2b-122">2</span></span>                                       | <span data-ttu-id="e4c2b-123">Dies ist eine ganze Zahl, die die Größe jedes Slice im Frame in Einheiten von Makroblock Zeilen angibt.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="e4c2b-124">Der Encoder sollte die Einstellung ablehnen, wenn der Wert größer als die Anzahl der Makroblock Zeilen im Frame ist.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="e4c2b-125">Wenn die Anwendung keinen Wert für [codecapi \_ avencslicecontrolmode](codecapi-avencslicecontrolmode.md)festgelegt, sollte der Encoder einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="e4c2b-126">Der empfohlene Standardwert ist, dass ein einzelner Slice für den gesamten Frame vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="e4c2b-127">Einige Encoder können Slices parallel codieren, sodass die Leistung abhängig von den Slice-Steuerelement Einstellungen beeinträchtigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="e4c2b-128">Beispielsweise kann das Codieren eines Frames als einzelner Slice langsamer sein, als wenn der Frame als mehrere Slices codiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="e4c2b-129">Die Slice-Steuerelement Einstellungen sind dynamisch und können während der Codierungs Sitzung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="e4c2b-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4c2b-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4c2b-130">Requirements</span></span>



| <span data-ttu-id="e4c2b-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4c2b-131">Requirement</span></span> | <span data-ttu-id="e4c2b-132">Wert</span><span class="sxs-lookup"><span data-stu-id="e4c2b-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4c2b-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e4c2b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e4c2b-134">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e4c2b-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="e4c2b-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e4c2b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e4c2b-136">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e4c2b-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e4c2b-137">Header</span><span class="sxs-lookup"><span data-stu-id="e4c2b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4c2b-138"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4c2b-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4c2b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e4c2b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4c2b-140">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e4c2b-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




