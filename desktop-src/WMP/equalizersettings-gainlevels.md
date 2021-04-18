---
title: Equalizersettings. gainlevels
description: Das Attribut "gainlevels" gibt die Gewinn Ebene des Bands an oder ruft es ab, das dem angegebenen Index entspricht.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Equalizersettings. gainlevels-Fenster Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358304"
---
# <a name="equalizersettingsgainlevels"></a><span data-ttu-id="c9936-104">Equalizersettings. gainlevels</span><span class="sxs-lookup"><span data-stu-id="c9936-104">EQUALIZERSETTINGS.gainLevels</span></span>

<span data-ttu-id="c9936-105">Das Attribut " **gainlevels** " gibt die Gewinn Ebene des Bands an oder ruft es ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="c9936-105">The **gainLevels** attribute specifies or retrieves the gain level of the band corresponding to the index provided.</span></span>

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a><span data-ttu-id="c9936-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c9936-106">Possible Values</span></span>

<span data-ttu-id="c9936-107">Dieses Attribut ist eine Lese-/schreibnummer (**float**) mit einem Wert, der normalerweise zwischen 20 und + 20 liegt. </span><span class="sxs-lookup"><span data-stu-id="c9936-107">This attribute is a read/write **Number** (**float**) with a value normally ranging from  20 to +20.</span></span>

## <a name="parameters"></a><span data-ttu-id="c9936-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9936-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9936-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*das-Band*</span><span class="sxs-lookup"><span data-stu-id="c9936-109"><span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*</span></span>
</dt> <dd>

<span data-ttu-id="c9936-110">**Zahl**(**Long**) zwischen 1 und 10, die den Index des Bands angibt.</span><span class="sxs-lookup"><span data-stu-id="c9936-110">**Number**(**long**) between 1 and 10 indicating the index of the band.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9936-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9936-111">Remarks</span></span>

<span data-ttu-id="c9936-112">Dieses Attribut nimmt einen Parameter an, aber sein Wert wird in Skriptcode auf dieselbe Weise wie andere Attributwerte angegeben.</span><span class="sxs-lookup"><span data-stu-id="c9936-112">This attribute takes a parameter, but its value is specified in script code the same way as other attribute values.</span></span> <span data-ttu-id="c9936-113">Sie kann nicht im Element "equalizersettings" angegeben werden und kann nicht mit dem **wmpprop** -Attribut "lauschen" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9936-113">It cannot be specified in the EQUALIZERSETTINGS element, nor can it be used with the **wmpprop** listening attribute.</span></span> <span data-ttu-id="c9936-114">Stattdessen werden die nummerierten Attribute der Gewinn Ebene für diese Situationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c9936-114">Instead, the numbered gain level attributes are provided for these situations.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9936-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9936-115">Requirements</span></span>



| <span data-ttu-id="c9936-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9936-116">Requirement</span></span> | <span data-ttu-id="c9936-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c9936-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c9936-118">Version</span><span class="sxs-lookup"><span data-stu-id="c9936-118">Version</span></span><br/> | <span data-ttu-id="c9936-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c9936-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9936-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9936-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9936-121">**Equalizersettings-Element**</span><span class="sxs-lookup"><span data-stu-id="c9936-121">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="c9936-122">**Lauschen von Attributen**</span><span class="sxs-lookup"><span data-stu-id="c9936-122">**Listening Attributes**</span></span>](listening-attributes.md)
</dt> </dl>

 

 





