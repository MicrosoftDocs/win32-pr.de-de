---
description: Gibt die maximalen vom Encoder unterstützten Verweis Rahmen an.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: CODECAPI_AVEncVideoMaxNumRefFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132161"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="d4ea6-103">Codecapi \_ avencvideomaxnumrefframe (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d4ea6-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="d4ea6-104">Gibt die maximalen vom Encoder unterstützten Verweis Rahmen an.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="d4ea6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d4ea6-105">Data type</span></span>

<span data-ttu-id="d4ea6-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="d4ea6-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="d4ea6-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="d4ea6-107">Property GUID</span></span>

<span data-ttu-id="d4ea6-108">**Codecapi \_ avencvideomaxnumrefframe**</span><span class="sxs-lookup"><span data-stu-id="d4ea6-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="d4ea6-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4ea6-109">Remarks</span></span>

<span data-ttu-id="d4ea6-110">Bei H. 264 wird dies dem Sequenz Parameter Set Variable **Max \_ NUM \_ ref \_ Frames** entsprechend der Angabe in der H. 264-Spezifikation zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="d4ea6-111">**H. 264/AVC-Encoder:**</span><span class="sxs-lookup"><span data-stu-id="d4ea6-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="d4ea6-112">Encoder können weniger Verweis Frames verwenden, um die im Bitstream angegebene Ebene einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="d4ea6-113">Encoder müssen " [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)", " [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)" und " [**getparameterrangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)" unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="d4ea6-114">Dies ist eine statische Eigenschaft, die bedeutet, dass Sie nur festgelegt werden kann, bevor die Codierungs Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="d4ea6-115">Der empfohlene Standardwert ist 2.</span><span class="sxs-lookup"><span data-stu-id="d4ea6-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ea6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4ea6-116">Requirements</span></span>



| <span data-ttu-id="d4ea6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4ea6-117">Requirement</span></span> | <span data-ttu-id="d4ea6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d4ea6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ea6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4ea6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ea6-120">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4ea6-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="d4ea6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4ea6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ea6-122">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d4ea6-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d4ea6-123">Header</span><span class="sxs-lookup"><span data-stu-id="d4ea6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ea6-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ea6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ea6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4ea6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ea6-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d4ea6-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

