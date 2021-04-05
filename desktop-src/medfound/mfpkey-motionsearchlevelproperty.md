---
description: Gibt an, wie Farbinformationen in Bewegungs Such Vorgängen verwendet werden.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: MFPKEY_MOTIONSEARCHLEVEL-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042082"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="41f2f-103">Mfpkey- \_ Eigenschaft "mutionsearchlevel"</span><span class="sxs-lookup"><span data-stu-id="41f2f-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="41f2f-104">Gibt an, wie Farbinformationen in Bewegungs Such Vorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f2f-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="41f2f-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="41f2f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="41f2f-106">g \_ wszwmvcmutionsearchlevel</span><span class="sxs-lookup"><span data-stu-id="41f2f-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="41f2f-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="41f2f-107">Data Type</span></span>

<span data-ttu-id="41f2f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="41f2f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="41f2f-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="41f2f-109">Default Value</span></span>

<span data-ttu-id="41f2f-110">0</span><span class="sxs-lookup"><span data-stu-id="41f2f-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="41f2f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41f2f-111">Remarks</span></span>

<span data-ttu-id="41f2f-112">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="41f2f-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="41f2f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="41f2f-113">Value</span></span> | <span data-ttu-id="41f2f-114">Verwendete Video Informationen</span><span class="sxs-lookup"><span data-stu-id="41f2f-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="41f2f-115">0</span><span class="sxs-lookup"><span data-stu-id="41f2f-115">0</span></span>     | <span data-ttu-id="41f2f-116">Nur Luma.</span><span class="sxs-lookup"><span data-stu-id="41f2f-116">Luma only.</span></span>                                       |
| <span data-ttu-id="41f2f-117">1</span><span class="sxs-lookup"><span data-stu-id="41f2f-117">1</span></span>     | <span data-ttu-id="41f2f-118">Luma mit nächster ganzzahligen Chroma.</span><span class="sxs-lookup"><span data-stu-id="41f2f-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="41f2f-119">2</span><span class="sxs-lookup"><span data-stu-id="41f2f-119">2</span></span>     | <span data-ttu-id="41f2f-120">Luma mit echtem Chroma.</span><span class="sxs-lookup"><span data-stu-id="41f2f-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="41f2f-121">-1</span><span class="sxs-lookup"><span data-stu-id="41f2f-121">-1</span></span>    | <span data-ttu-id="41f2f-122">Makroblock-Adaptive mit True Chroma.</span><span class="sxs-lookup"><span data-stu-id="41f2f-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="41f2f-123">-2</span><span class="sxs-lookup"><span data-stu-id="41f2f-123">-2</span></span>    | <span data-ttu-id="41f2f-124">Makroblock-Adaptive mit dem nächstgelegenen ganzzahligen Chroma.</span><span class="sxs-lookup"><span data-stu-id="41f2f-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="41f2f-125">Standardmäßig führt der Codec die Bewegungssuche nur im Luma-Kanal durch.</span><span class="sxs-lookup"><span data-stu-id="41f2f-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="41f2f-126">Das Einschließen von Chroma-Informationen in die Bewegungs Schätzung kann die Qualität codierter Videos erheblich verbessern.</span><span class="sxs-lookup"><span data-stu-id="41f2f-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="41f2f-127">Die Bewegungssuche mit Luma und True Chroma ergibt die beste Videoqualität, aber mit den höchsten Leistungseinbußen.</span><span class="sxs-lookup"><span data-stu-id="41f2f-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="41f2f-128">Die beiden dynamischen Modi (-1 und-2) und die-Eigenschaft mit dem Wert "Luma" mit dem nächstliegenden ganzzahligen Chroma-Modus bietet angemessene Kompromisse zwischen Qualität und Leistung.</span><span class="sxs-lookup"><span data-stu-id="41f2f-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="41f2f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41f2f-129">Requirements</span></span>



| <span data-ttu-id="41f2f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41f2f-130">Requirement</span></span> | <span data-ttu-id="41f2f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="41f2f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41f2f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41f2f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="41f2f-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41f2f-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="41f2f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41f2f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="41f2f-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41f2f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41f2f-136">Header</span><span class="sxs-lookup"><span data-stu-id="41f2f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="41f2f-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41f2f-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41f2f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41f2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41f2f-139">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="41f2f-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




