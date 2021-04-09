---
description: Legt den Sequenz Parametersatz-Bezeichner (SPS) in der SPS-Einheit für die Netzwerk Abstraktionsschicht (NAL) des H. 264-Bit-Streams fest.
ms.assetid: 583DD539-6EE8-4DD4-A0FE-D2BBE1A4302F
title: CODECAPI_AVEncH264SPSID-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e06fb78fc128b2eec5db2c61faf70ee10a5eba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127981"
---
# <a name="codecapi_avench264spsid-property"></a><span data-ttu-id="24858-103">Codecapi \_ AVEncH264SPSID Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24858-103">CODECAPI\_AVEncH264SPSID property</span></span>

<span data-ttu-id="24858-104">Legt den Sequenz Parametersatz-Bezeichner (SPS) in der SPS-Einheit für die Netzwerk Abstraktionsschicht (NAL) des H. 264-Bit-Streams fest.</span><span class="sxs-lookup"><span data-stu-id="24858-104">Sets the sequence parameter set (SPS) identifier in the SPS network abstraction layer (NAL) unit of the H.264 bit stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="24858-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="24858-105">Data type</span></span>

<span data-ttu-id="24858-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="24858-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="24858-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="24858-107">Property GUID</span></span>

<span data-ttu-id="24858-108">**Codecapi \_ AVEncH264SPSID**</span><span class="sxs-lookup"><span data-stu-id="24858-108">**CODECAPI\_AVEncH264SPSID**</span></span>

## <a name="property-value"></a><span data-ttu-id="24858-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="24858-109">Property value</span></span>

<span data-ttu-id="24858-110">Gibt den Wert der **Seq- \_ Parameter \_ Satz- \_ ID** in der SPS-nal-Einheit an.</span><span class="sxs-lookup"><span data-stu-id="24858-110">Specifies the value of **seq\_parameter\_set\_id** in the SPS NAL unit.</span></span> <span data-ttu-id="24858-111">Das **Seq- \_ Parameter \_ Satz- \_ ID** -Syntax Element identifiziert den Satz von Sequenz Parametern.</span><span class="sxs-lookup"><span data-stu-id="24858-111">The **seq\_parameter\_set\_id** syntax element identifies the sequence parameter set.</span></span> <span data-ttu-id="24858-112">Der resultierende Bitstream kann mit anderen Bitstreams verkettet werden, um einen längeren Bitstream zu schaffen, der mehrere Sequenz Parametersätze mit unterschiedlichen SPS-bezeichtern enthält.</span><span class="sxs-lookup"><span data-stu-id="24858-112">The resulting bit stream can be concatenated with other bit streams, to produce a longer bit stream that contains multiple sequence parameter sets with different SPS identifiers.</span></span>

<span data-ttu-id="24858-113">Der gültige Bereich ist 0 31, wie in der H. 264/AVC-Spezifikation angegeben.</span><span class="sxs-lookup"><span data-stu-id="24858-113">The valid range is 0 31, as specified in the H.264/AVC specification.</span></span>

## <a name="requirements"></a><span data-ttu-id="24858-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24858-114">Requirements</span></span>



| <span data-ttu-id="24858-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24858-115">Requirement</span></span> | <span data-ttu-id="24858-116">Wert</span><span class="sxs-lookup"><span data-stu-id="24858-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24858-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24858-117">Minimum supported client</span></span><br/> | <span data-ttu-id="24858-118">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="24858-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="24858-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24858-119">Minimum supported server</span></span><br/> | <span data-ttu-id="24858-120">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="24858-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="24858-121">Header</span><span class="sxs-lookup"><span data-stu-id="24858-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="24858-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="24858-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24858-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24858-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24858-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="24858-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="24858-125">**Icodecapi**</span><span class="sxs-lookup"><span data-stu-id="24858-125">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

