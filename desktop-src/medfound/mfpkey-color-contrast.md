---
description: Passt den Kontrast an.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: MFPKEY_COLOR_CONTRAST-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368254"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="ae276-103">Eigenschaft für den mfpkey- \_ Farb \_ Kontrast</span><span class="sxs-lookup"><span data-stu-id="ae276-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="ae276-104">Passt den Kontrast an.</span><span class="sxs-lookup"><span data-stu-id="ae276-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ae276-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ae276-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ae276-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ae276-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="ae276-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ae276-107">Data Type</span></span>

<span data-ttu-id="ae276-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ae276-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ae276-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ae276-109">Default Value</span></span>

<span data-ttu-id="ae276-110">0</span><span class="sxs-lookup"><span data-stu-id="ae276-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="ae276-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ae276-111">Applies To</span></span>

-   [<span data-ttu-id="ae276-112">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="ae276-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="ae276-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae276-113">Remarks</span></span>

<span data-ttu-id="ae276-114">Die Kontrast Anpassung erfolgt durch Multiplikation der YCbCr-Werte mit einem Skalierungsfaktor.</span><span class="sxs-lookup"><span data-stu-id="ae276-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="ae276-115">Diese Eigenschaft hat einen Bereich von-127 bis 127.</span><span class="sxs-lookup"><span data-stu-id="ae276-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="ae276-116">NULL gibt an, dass keine Änderung im Gegensatz dazu besteht.</span><span class="sxs-lookup"><span data-stu-id="ae276-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae276-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae276-117">Requirements</span></span>



| <span data-ttu-id="ae276-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae276-118">Requirement</span></span> | <span data-ttu-id="ae276-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ae276-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae276-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ae276-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae276-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae276-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ae276-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ae276-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae276-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ae276-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae276-124">Header</span><span class="sxs-lookup"><span data-stu-id="ae276-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae276-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae276-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae276-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae276-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae276-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae276-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
