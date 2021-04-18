---
description: Gibt das Puffer Fenster (in Millisekunden) für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: MFPKEY_DYN_VBR_BAVG-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357502"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="cb9ab-103">Mfpkey \_ dyn \_ VBR \_ bavg (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cb9ab-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="cb9ab-104">Gibt das Puffer Fenster (in Millisekunden) für einen Encoder an, der für die Verwendung der durchschnittlich kontrollierbaren VBR-Codierung konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9ab-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="cb9ab-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="cb9ab-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="cb9ab-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb9ab-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="cb9ab-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cb9ab-107">Data Type</span></span>

<span data-ttu-id="cb9ab-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="cb9ab-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb9ab-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb9ab-109">Remarks</span></span>

<span data-ttu-id="cb9ab-110">Wenn die Eigenschaften [**mfpkey, \_ avgeingeschränkter**](mfpkey-avgconstrainedproperty.md) und [**mfpkey \_ vbrenabled**](mfpkey-vbrenabledproperty.md) beide auf **Variant \_ true** festgelegt sind, verwendet der Encoder die durchschnittliche steuerbare VBR-Codierung.</span><span class="sxs-lookup"><span data-stu-id="cb9ab-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="cb9ab-111">In diesem Fall wird der Encoder gemäß dem Wert dieser Eigenschaft und der Eigenschaft [**mfpkey \_ dyn \_ VBR \_ Ravg**](mfpkey-dyn-vbr-ravgproperty.md) konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="cb9ab-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb9ab-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb9ab-112">Requirements</span></span>



| <span data-ttu-id="cb9ab-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb9ab-113">Requirement</span></span> | <span data-ttu-id="cb9ab-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cb9ab-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9ab-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb9ab-115">Minimum supported client</span></span><br/> | <span data-ttu-id="cb9ab-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb9ab-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cb9ab-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb9ab-117">Minimum supported server</span></span><br/> | <span data-ttu-id="cb9ab-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb9ab-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cb9ab-119">Header</span><span class="sxs-lookup"><span data-stu-id="cb9ab-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb9ab-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb9ab-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb9ab-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb9ab-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb9ab-122">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb9ab-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
