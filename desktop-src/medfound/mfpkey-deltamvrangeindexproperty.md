---
description: Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.
ms.assetid: 22ffdb77-9266-42e5-be41-fc7457141bba
title: MFPKEY_DELTAMVRANGEINDEX-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d923659e64c9a0dcab40811e31d7752924700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528676"
---
# <a name="mfpkey_deltamvrangeindex-property"></a><span data-ttu-id="ac601-103">Mfpkey- \_ Eigenschaft "Delta-vrangeindex"</span><span class="sxs-lookup"><span data-stu-id="ac601-103">MFPKEY\_DELTAMVRANGEINDEX Property</span></span>

<span data-ttu-id="ac601-104">Gibt die Methode an, die zum Codieren der Bewegungsvektor Informationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ac601-104">Specifies the method used to encode the motion vector information.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ac601-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ac601-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ac601-106">g \_ wszwmvcdelta tamvrangeindex</span><span class="sxs-lookup"><span data-stu-id="ac601-106">g\_wszWMVCDeltaMVRangeIndex</span></span>

## <a name="data-type"></a><span data-ttu-id="ac601-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ac601-107">Data Type</span></span>

<span data-ttu-id="ac601-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ac601-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="ac601-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="ac601-109">Default Value</span></span>

<span data-ttu-id="ac601-110">0</span><span class="sxs-lookup"><span data-stu-id="ac601-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="ac601-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac601-111">Remarks</span></span>

<span data-ttu-id="ac601-112">Wenn diese Eigenschaft festgelegt ist, vergrößert der Encoder den Delta Bewegungsvektor Bereich in Feldern.</span><span class="sxs-lookup"><span data-stu-id="ac601-112">If this property is set, the encoder increases the delta motion vector range in fields.</span></span> <span data-ttu-id="ac601-113">Bewegungsvektor Informationen sind nur für Zeilen Sprung Felder gültig.</span><span class="sxs-lookup"><span data-stu-id="ac601-113">Motion vector information is valid only for interlaced fields.</span></span>

<span data-ttu-id="ac601-114">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ac601-114">This property may be set to one of the following values:</span></span>



| <span data-ttu-id="ac601-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ac601-115">Value</span></span> | <span data-ttu-id="ac601-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac601-116">Description</span></span>                                                                          |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac601-117">0</span><span class="sxs-lookup"><span data-stu-id="ac601-117">0</span></span>     | <span data-ttu-id="ac601-118">Verwenden Sie den vorhandenen Delta Bewegungsvektor Bereich.</span><span class="sxs-lookup"><span data-stu-id="ac601-118">Use the existing delta motion vector range.</span></span>                                          |
| <span data-ttu-id="ac601-119">1</span><span class="sxs-lookup"><span data-stu-id="ac601-119">1</span></span>     | <span data-ttu-id="ac601-120">Verdoppelt den Delta Bewegungsvektor Bereich in horizontaler Richtung.</span><span class="sxs-lookup"><span data-stu-id="ac601-120">Double the delta motion vector range in the horizontal direction.</span></span>                    |
| <span data-ttu-id="ac601-121">2</span><span class="sxs-lookup"><span data-stu-id="ac601-121">2</span></span>     | <span data-ttu-id="ac601-122">Verdoppelt den Delta Bewegungsvektor Bereich in vertikaler Richtung.</span><span class="sxs-lookup"><span data-stu-id="ac601-122">Double the delta motion vector range in the vertical direction.</span></span>                      |
| <span data-ttu-id="ac601-123">3</span><span class="sxs-lookup"><span data-stu-id="ac601-123">3</span></span>     | <span data-ttu-id="ac601-124">Verdoppeln Sie den Vektor Bereich der Delta Bewegung sowohl in horizontaler als auch in vertikaler Richtung.</span><span class="sxs-lookup"><span data-stu-id="ac601-124">Double the delta motion vector range in both the horizontal and vertical directions.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="ac601-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ac601-125">Requirements</span></span>



| <span data-ttu-id="ac601-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac601-126">Requirement</span></span> | <span data-ttu-id="ac601-127">Wert</span><span class="sxs-lookup"><span data-stu-id="ac601-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac601-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac601-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ac601-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac601-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ac601-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac601-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ac601-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac601-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ac601-132">Header</span><span class="sxs-lookup"><span data-stu-id="ac601-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac601-133"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac601-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac601-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ac601-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac601-135">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac601-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




