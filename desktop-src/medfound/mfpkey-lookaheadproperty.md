---
description: Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.
ms.assetid: e5cdd066-e25a-4107-9523-5611bd792372
title: MFPKEY_LOOKAHEAD-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a024c4d0be6ef7ab16c4bf51f290b01de3282b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354638"
---
# <a name="mfpkey_lookahead-property"></a><span data-ttu-id="577e7-103">Mfpkey- \_ Lookahead-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="577e7-103">MFPKEY\_LOOKAHEAD Property</span></span>

<span data-ttu-id="577e7-104">Gibt die Anzahl der Frames nach dem aktuellen Frame an, den der Codec vor dem Codieren des aktuellen Frames auswerten soll.</span><span class="sxs-lookup"><span data-stu-id="577e7-104">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="577e7-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="577e7-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="577e7-106">g \_ wszwmvclookahead</span><span class="sxs-lookup"><span data-stu-id="577e7-106">g\_wszWMVCLookAhead</span></span>

## <a name="data-type"></a><span data-ttu-id="577e7-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="577e7-107">Data Type</span></span>

<span data-ttu-id="577e7-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="577e7-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="577e7-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="577e7-109">Default Value</span></span>

<span data-ttu-id="577e7-110">0</span><span class="sxs-lookup"><span data-stu-id="577e7-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="577e7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="577e7-111">Remarks</span></span>

<span data-ttu-id="577e7-112">Wenn der Codec Lookahead verwendet, kann er das Video effizienter codieren.</span><span class="sxs-lookup"><span data-stu-id="577e7-112">When the codec uses lookahead, it can encode the video more efficiently.</span></span>

<span data-ttu-id="577e7-113">Das Writer-Objekt des Windows Media Format SDK erwartet, dass der Codec die einzelnen Stichproben sofort codiert.</span><span class="sxs-lookup"><span data-stu-id="577e7-113">The writer object of the Windows Media Format SDK expects the codec to encode each sample immediately.</span></span> <span data-ttu-id="577e7-114">Dies hat zur Folge, dass diese Funktion in Software, die das Writer-Objekt verwendet (einschließlich Windows Media Encoder und Windows Media Player), nicht ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="577e7-114">As a result, this feature does not work properly in software that uses the writer object (including Windows Media Encoder and Windows Media Player).</span></span> <span data-ttu-id="577e7-115">Alle Dateneinheiten Erweiterungen, die Video Frames zugeordnet sind, werden an den falschen Ausgabe Rahmen angefügt.</span><span class="sxs-lookup"><span data-stu-id="577e7-115">Any data unit extensions associated with video frames will be attached to the wrong output frame.</span></span> <span data-ttu-id="577e7-116">Die Anzahl der Frames, nach denen die Dateneinheiten Erweiterungen falsch platziert werden, entspricht der Anzahl der verwendeten Frames von Lookahead.</span><span class="sxs-lookup"><span data-stu-id="577e7-116">The number of frames by which the data unit extensions are misplaced is equal to the number of frames of lookahead that are used.</span></span>

<span data-ttu-id="577e7-117">Gültige Lookahead-Werte reichen von 0 bis 16 Frames.</span><span class="sxs-lookup"><span data-stu-id="577e7-117">Valid lookahead values range from 0 to 16 frames.</span></span> <span data-ttu-id="577e7-118">Der empfohlene Wert ist 16.</span><span class="sxs-lookup"><span data-stu-id="577e7-118">The recommended value is 16.</span></span>

## <a name="requirements"></a><span data-ttu-id="577e7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="577e7-119">Requirements</span></span>



| <span data-ttu-id="577e7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="577e7-120">Requirement</span></span> | <span data-ttu-id="577e7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="577e7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="577e7-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="577e7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="577e7-123">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="577e7-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="577e7-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="577e7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="577e7-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="577e7-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="577e7-126">Header</span><span class="sxs-lookup"><span data-stu-id="577e7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="577e7-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="577e7-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="577e7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="577e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="577e7-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="577e7-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




