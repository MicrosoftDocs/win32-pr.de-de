---
description: Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: MFPKEY_AVGCONSTRAINED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345050"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="1c885-103">Avgeingeschränkter mfpkey- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1c885-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="1c885-104">Gibt an, ob der Encoder eine Average-steuerbare VBR-Codierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c885-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1c885-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1c885-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1c885-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1c885-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1c885-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1c885-107">Data Type</span></span>

<span data-ttu-id="1c885-108">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="1c885-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="1c885-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1c885-109">Default Value</span></span>

<span data-ttu-id="1c885-110">**Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="1c885-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="1c885-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c885-111">Remarks</span></span>

<span data-ttu-id="1c885-112">Wenn diese Eigenschaft und die Eigenschaft [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) beide auf **Variant \_ true** festgelegt sind, verwendet der Encoder die Durchschnitt Bare VBR-Codierung.</span><span class="sxs-lookup"><span data-stu-id="1c885-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="1c885-113">In diesem Fall konfiguriert der Encoder sich entsprechend den Werten von [**mfpkey \_ dyn \_ VBR \_ bavg**](mfpkey-dyn-vbr-bavgproperty.md) und [**mfpkey \_ dyn \_ VBR \_ Ravg**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1c885-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c885-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c885-114">Requirements</span></span>



| <span data-ttu-id="1c885-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c885-115">Requirement</span></span> | <span data-ttu-id="1c885-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1c885-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c885-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c885-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1c885-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c885-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1c885-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c885-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1c885-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c885-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c885-121">Header</span><span class="sxs-lookup"><span data-stu-id="1c885-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c885-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c885-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c885-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c885-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c885-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1c885-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
