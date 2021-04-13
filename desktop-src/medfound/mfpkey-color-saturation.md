---
description: Passt die Sättigung an.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: MFPKEY_COLOR_SATURATION-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528685"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="8fd74-103">Eigenschaft für mfpkey- \_ Farb \_ Sättigung</span><span class="sxs-lookup"><span data-stu-id="8fd74-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="8fd74-104">Passt die Sättigung an.</span><span class="sxs-lookup"><span data-stu-id="8fd74-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8fd74-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8fd74-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8fd74-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8fd74-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8fd74-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8fd74-107">Data Type</span></span>

<span data-ttu-id="8fd74-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8fd74-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8fd74-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="8fd74-109">Default Value</span></span>

<span data-ttu-id="8fd74-110">0</span><span class="sxs-lookup"><span data-stu-id="8fd74-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="8fd74-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="8fd74-111">Applies To</span></span>

-   [<span data-ttu-id="8fd74-112">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="8fd74-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="8fd74-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fd74-113">Remarks</span></span>

<span data-ttu-id="8fd74-114">Die Sättigungs Anpassung wird durch die Multiplikation der Werte CB und CR durch eine Konstante durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fd74-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="8fd74-115">Diese Eigenschaft hat einen Bereich von-127 bis 127.</span><span class="sxs-lookup"><span data-stu-id="8fd74-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="8fd74-116">NULL gibt an, dass die Sättigung nicht geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fd74-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd74-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fd74-117">Requirements</span></span>



| <span data-ttu-id="8fd74-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fd74-118">Requirement</span></span> | <span data-ttu-id="8fd74-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8fd74-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd74-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fd74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd74-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fd74-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8fd74-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fd74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd74-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fd74-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8fd74-124">Header</span><span class="sxs-lookup"><span data-stu-id="8fd74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fd74-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fd74-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd74-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fd74-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd74-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8fd74-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
