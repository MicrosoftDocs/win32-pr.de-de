---
description: Gibt die Leistungs Ebene für den Decoder an.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372868"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="68a68-103">Mfpkey \_ avdecvideoswpowerlevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="68a68-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="68a68-104">Gibt die Leistungs Ebene für den Decoder an.</span><span class="sxs-lookup"><span data-stu-id="68a68-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="68a68-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="68a68-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="68a68-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68a68-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="68a68-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="68a68-107">Data Type</span></span>

<span data-ttu-id="68a68-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="68a68-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="68a68-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="68a68-109">Default Value</span></span>

<span data-ttu-id="68a68-110">**100**</span><span class="sxs-lookup"><span data-stu-id="68a68-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="68a68-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68a68-111">Remarks</span></span>

<span data-ttu-id="68a68-112">Diese Eigenschaft muss auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="68a68-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="68a68-113">Wert</span><span class="sxs-lookup"><span data-stu-id="68a68-113">Value</span></span> | <span data-ttu-id="68a68-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68a68-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="68a68-115">0</span><span class="sxs-lookup"><span data-stu-id="68a68-115">0</span></span>     | <span data-ttu-id="68a68-116">Der Decoder verwendet einen Energiepegel, der für die Akku Lebensdauer optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="68a68-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="68a68-117">50</span><span class="sxs-lookup"><span data-stu-id="68a68-117">50</span></span>    | <span data-ttu-id="68a68-118">Der Decoder verwendet einen ausgeglichenen Energie Stand.</span><span class="sxs-lookup"><span data-stu-id="68a68-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="68a68-119">100</span><span class="sxs-lookup"><span data-stu-id="68a68-119">100</span></span>   | <span data-ttu-id="68a68-120">Der Decoder verwendet einen Energiepegel, der für die Videoqualität optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="68a68-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="68a68-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68a68-121">Requirements</span></span>



| <span data-ttu-id="68a68-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68a68-122">Requirement</span></span> | <span data-ttu-id="68a68-123">Wert</span><span class="sxs-lookup"><span data-stu-id="68a68-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68a68-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68a68-124">Minimum supported client</span></span><br/> | <span data-ttu-id="68a68-125">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68a68-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="68a68-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68a68-126">Minimum supported server</span></span><br/> | <span data-ttu-id="68a68-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68a68-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="68a68-128">Header</span><span class="sxs-lookup"><span data-stu-id="68a68-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a68-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a68-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a68-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68a68-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a68-131">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68a68-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
