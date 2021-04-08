---
description: Gibt das Ende eines Codierungs Durchlaufs an.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864163"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="1f9dd-103">Mfpkey- \_ endofpass (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1f9dd-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="1f9dd-104">Gibt das Ende eines Codierungs Durchlaufs an.</span><span class="sxs-lookup"><span data-stu-id="1f9dd-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="1f9dd-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1f9dd-105">Data Type</span></span>

<span data-ttu-id="1f9dd-106">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1f9dd-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1f9dd-107">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1f9dd-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="1f9dd-108">g \_ wszwmvcendofpass</span><span class="sxs-lookup"><span data-stu-id="1f9dd-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="1f9dd-109">Datentyp für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1f9dd-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="1f9dd-110">Es ist kein Datentyp erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1f9dd-110">No data type is required.</span></span> <span data-ttu-id="1f9dd-111">Um diese Eigenschaft festzulegen, übergeben Sie eine nicht initialisierte **Variante**.</span><span class="sxs-lookup"><span data-stu-id="1f9dd-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9dd-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f9dd-112">Remarks</span></span>

<span data-ttu-id="1f9dd-113">Diese Eigenschaft ist keine normale Eigenschaft, da Sie unabhängig davon, ob der Wert Variant \_ true oder Variant false ist, dieselbe Auswirkung hat \_ .</span><span class="sxs-lookup"><span data-stu-id="1f9dd-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="1f9dd-114">Sie müssen diese Eigenschaft festlegen, nachdem Sie die letzten Eingabe Beispiele für einen Vorverarbeitungs Durchlauf verarbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="1f9dd-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="1f9dd-115">Wenn Sie mehrere Durchgänge ausführen, müssen Sie diese Eigenschaft am Ende jedes Vorverarbeitungs Durchsatzes festlegen (derzeit unterstützt keiner der Codecs mehr als einen).</span><span class="sxs-lookup"><span data-stu-id="1f9dd-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="1f9dd-116">Wenn Sie diese Eigenschaft nicht festlegen, geht der Codec davon aus, dass Sie immer noch Beispiele für die Vorverarbeitung übergeben.</span><span class="sxs-lookup"><span data-stu-id="1f9dd-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9dd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f9dd-117">Requirements</span></span>



| <span data-ttu-id="1f9dd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f9dd-118">Requirement</span></span> | <span data-ttu-id="1f9dd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1f9dd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9dd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f9dd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9dd-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f9dd-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1f9dd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f9dd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9dd-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f9dd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f9dd-124">Header</span><span class="sxs-lookup"><span data-stu-id="1f9dd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9dd-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9dd-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9dd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f9dd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9dd-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f9dd-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




