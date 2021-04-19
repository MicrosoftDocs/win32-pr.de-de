---
description: Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (VBR) von Audiostreams an.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: MFPKEY_DESIRED_VBRQUALITY-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349152"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="2ac32-103">Mfpkey \_ gewünschte \_ vbrquality-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2ac32-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="2ac32-104">Gibt die gewünschte Qualitätsstufe für die Qualitäts basierte (1-Pass-) VBR-Codierung (VBR) von Audiostreams an.</span><span class="sxs-lookup"><span data-stu-id="2ac32-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2ac32-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2ac32-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2ac32-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ac32-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2ac32-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2ac32-107">Data Type</span></span>

<span data-ttu-id="2ac32-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2ac32-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="2ac32-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="2ac32-109">Default Value</span></span>

<span data-ttu-id="2ac32-110">0</span><span class="sxs-lookup"><span data-stu-id="2ac32-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="2ac32-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ac32-111">Remarks</span></span>

<span data-ttu-id="2ac32-112">Dieser Wert kann zwischen 0 und 100 liegen, wobei 100 eine maximale Qualität ist.</span><span class="sxs-lookup"><span data-stu-id="2ac32-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="2ac32-113">Der Wert 0 gibt an, dass die Qualitäts basierte VBR-Codierungsmethode nicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ac32-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="2ac32-114">Legen Sie die folgenden Codierungs Eigenschaften fest, um VBR-Modi aufzulisten, die eine bestimmte Qualitätsanforderung erfüllen.</span><span class="sxs-lookup"><span data-stu-id="2ac32-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="2ac32-115">Legen Sie [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="2ac32-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="2ac32-116">Legen Sie [**mfpkey- \_ \_ Enumeration \_ vbrquality**](mfpkey-constrain-enumerated-vbrqualityproperty.md) auf **Variant \_ true** fest.</span><span class="sxs-lookup"><span data-stu-id="2ac32-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="2ac32-117">Legen Sie für **mfpkey die \_ gewünschte \_ vbrquality** auf die gewünschte Qualität fest.</span><span class="sxs-lookup"><span data-stu-id="2ac32-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="2ac32-118">Legen Sie für den Modus ohne Verlust die gewünschte Qualität auf 100 fest.</span><span class="sxs-lookup"><span data-stu-id="2ac32-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ac32-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac32-119">Requirements</span></span>



| <span data-ttu-id="2ac32-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ac32-120">Requirement</span></span> | <span data-ttu-id="2ac32-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac32-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac32-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ac32-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac32-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ac32-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2ac32-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ac32-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac32-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ac32-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ac32-126">Header</span><span class="sxs-lookup"><span data-stu-id="2ac32-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac32-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac32-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ac32-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ac32-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac32-129">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ac32-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
