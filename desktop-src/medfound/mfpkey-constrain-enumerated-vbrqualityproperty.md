---
description: Gibt an, ob vom Encoder aufgelistete Modi mit den von mfpkey \_ gewünschten \_ vbrquality übereinstimmen.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370934"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="9b864-103">Mfpkey- \_ Einschränkung für \_ aufgelistete \_ vbrquality-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9b864-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="9b864-104">Gibt an, ob vom Encoder aufgelistete Modi mit den von [**mfpkey \_ gewünschten \_ vbrquality**](mfpkey-desired-vbrqualityproperty.md)übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="9b864-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9b864-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9b864-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9b864-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b864-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9b864-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9b864-107">Data Type</span></span>

<span data-ttu-id="9b864-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="9b864-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="9b864-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="9b864-109">Default Value</span></span>

<span data-ttu-id="9b864-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="9b864-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="9b864-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9b864-111">Remarks</span></span>

<span data-ttu-id="9b864-112">Legen Sie die folgenden Codierungs Eigenschaften fest, um VBR-Modi aufzulisten, die eine bestimmte Qualitätsanforderung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="9b864-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="9b864-113">Legen Sie [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="9b864-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="9b864-114">Legen Sie **mfpkey- \_ \_ Enumeration \_ vbrquality** auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="9b864-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="9b864-115">Legen Sie für [**mfpkey die \_ gewünschte \_ vbrquality**](mfpkey-desired-vbrqualityproperty.md) auf die gewünschte Qualität fest.</span><span class="sxs-lookup"><span data-stu-id="9b864-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="9b864-116">Legen Sie für den Modus ohne Verlust die gewünschte Qualität auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="9b864-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b864-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b864-117">Requirements</span></span>



| <span data-ttu-id="9b864-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b864-118">Requirement</span></span> | <span data-ttu-id="9b864-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9b864-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b864-120">Client</span><span class="sxs-lookup"><span data-stu-id="9b864-120">Client</span></span><br/> | <span data-ttu-id="9b864-121">Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="9b864-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="9b864-122">Header</span><span class="sxs-lookup"><span data-stu-id="9b864-122">Header</span></span><br/> | <dl> <span data-ttu-id="9b864-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b864-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b864-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b864-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b864-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b864-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
