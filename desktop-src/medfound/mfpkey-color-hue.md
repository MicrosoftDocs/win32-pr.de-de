---
description: Passt den Farbton an.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: MFPKEY_COLOR_HUE-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131252"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="ce1b6-103">Mfpkey \_ Color \_ Hue (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ce1b6-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="ce1b6-104">Passt den Farbton an.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ce1b6-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ce1b6-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ce1b6-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ce1b6-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ce1b6-107">Data Type</span></span>

<span data-ttu-id="ce1b6-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ce1b6-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ce1b6-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ce1b6-109">Default Value</span></span>

<span data-ttu-id="ce1b6-110">0</span><span class="sxs-lookup"><span data-stu-id="ce1b6-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce1b6-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ce1b6-111">Applies To</span></span>

-   [<span data-ttu-id="ce1b6-112">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="ce1b6-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="ce1b6-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce1b6-113">Remarks</span></span>

<span data-ttu-id="ce1b6-114">Die Hue-Anpassung wird durch das Mischen der Werte CB und CR durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="ce1b6-115">(Wenn CB und CR in einem zweidimensionalen Raum gezeichnet werden, wird die Hue-Anpassung durch Drehen um den Ursprung durchgeführt.)</span><span class="sxs-lookup"><span data-stu-id="ce1b6-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="ce1b6-116">Diese Eigenschaft hat einen Bereich von-127 bis 127.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="ce1b6-117">NULL bedeutet, dass keine Änderung in Hue angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce1b6-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce1b6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce1b6-118">Requirements</span></span>



| <span data-ttu-id="ce1b6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce1b6-119">Requirement</span></span> | <span data-ttu-id="ce1b6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ce1b6-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce1b6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce1b6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce1b6-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce1b6-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ce1b6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce1b6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce1b6-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce1b6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce1b6-125">Header</span><span class="sxs-lookup"><span data-stu-id="ce1b6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce1b6-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce1b6-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce1b6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce1b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce1b6-128">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce1b6-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
