---
description: Passt die Helligkeit an.
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: MFPKEY_COLOR_BRIGHTNESS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864775"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="9dc6d-103">Eigenschaft "mfpkey \_ Color \_ Helligkeit"</span><span class="sxs-lookup"><span data-stu-id="9dc6d-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="9dc6d-104">Passt die Helligkeit an.</span><span class="sxs-lookup"><span data-stu-id="9dc6d-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9dc6d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9dc6d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9dc6d-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9dc6d-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9dc6d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9dc6d-107">Data Type</span></span>

<span data-ttu-id="9dc6d-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="9dc6d-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="9dc6d-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9dc6d-109">Default Value</span></span>

<span data-ttu-id="9dc6d-110">0</span><span class="sxs-lookup"><span data-stu-id="9dc6d-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="9dc6d-111">Gilt für</span><span class="sxs-lookup"><span data-stu-id="9dc6d-111">Applies To</span></span>

-   [<span data-ttu-id="9dc6d-112">Farb Steuerungs Transformation (DSP)</span><span class="sxs-lookup"><span data-stu-id="9dc6d-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="9dc6d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dc6d-113">Remarks</span></span>

<span data-ttu-id="9dc6d-114">Die Helligkeitsanpassung wird durch Hinzufügen eines Werts zum Luma-Kanal durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9dc6d-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="9dc6d-115">Diese Eigenschaft hat einen Bereich von-127 bis 127.</span><span class="sxs-lookup"><span data-stu-id="9dc6d-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="9dc6d-116">NULL gibt an, dass die Helligkeit nicht geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dc6d-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc6d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dc6d-117">Requirements</span></span>



| <span data-ttu-id="9dc6d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dc6d-118">Requirement</span></span> | <span data-ttu-id="9dc6d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9dc6d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc6d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dc6d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9dc6d-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dc6d-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9dc6d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dc6d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9dc6d-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dc6d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9dc6d-124">Header</span><span class="sxs-lookup"><span data-stu-id="9dc6d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dc6d-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9dc6d-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc6d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dc6d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc6d-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9dc6d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
