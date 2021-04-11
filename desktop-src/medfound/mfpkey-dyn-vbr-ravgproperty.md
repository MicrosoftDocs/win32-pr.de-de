---
description: Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: MFPKEY_DYN_VBR_RAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959420"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="9a593-103">Eigenschaft "mfpkey \_ dyn \_ VBR \_ Ravg"</span><span class="sxs-lookup"><span data-stu-id="9a593-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="9a593-104">Gibt die durchschnittliche Bitrate in Bits pro Sekunde für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="9a593-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9a593-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9a593-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9a593-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a593-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="9a593-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9a593-107">Data Type</span></span>

<span data-ttu-id="9a593-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="9a593-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="9a593-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a593-109">Remarks</span></span>

<span data-ttu-id="9a593-110">Wenn die Eigenschaften [**mfpkey, \_ avgeingeschränkter**](mfpkey-avgconstrainedproperty.md) und [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) beide auf **Variant \_ true** festgelegt sind, verwendet der Encoder die durchschnittliche steuerbare VBR-Codierung.</span><span class="sxs-lookup"><span data-stu-id="9a593-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="9a593-111">In diesem Fall wird der Encoder gemäß dem Wert dieser Eigenschaft und der Eigenschaft [**mfpkey \_ dyn \_ VBR \_ bavg**](mfpkey-dyn-vbr-bavgproperty.md) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="9a593-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a593-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a593-112">Requirements</span></span>



| <span data-ttu-id="9a593-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a593-113">Requirement</span></span> | <span data-ttu-id="9a593-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9a593-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a593-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a593-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9a593-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a593-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9a593-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a593-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9a593-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a593-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a593-119">Header</span><span class="sxs-lookup"><span data-stu-id="9a593-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a593-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a593-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a593-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a593-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a593-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a593-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
