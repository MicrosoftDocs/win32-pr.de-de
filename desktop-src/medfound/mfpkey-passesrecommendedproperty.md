---
description: Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215505"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="29ff5-103">Mfpkey \_ passesrecommended-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="29ff5-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="29ff5-104">Gibt die maximale Anzahl von durch den Encoder unterstützten Durchläufen an.</span><span class="sxs-lookup"><span data-stu-id="29ff5-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="29ff5-105">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="29ff5-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="29ff5-106">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="29ff5-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="29ff5-107">g \_ wszwmvcpassesrecommended, g \_ wszwmcpmaxpass</span><span class="sxs-lookup"><span data-stu-id="29ff5-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="29ff5-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="29ff5-108">Data Type</span></span>

<span data-ttu-id="29ff5-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="29ff5-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="29ff5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29ff5-110">Remarks</span></span>

<span data-ttu-id="29ff5-111">Sie können den Wert dieser Eigenschaft abrufen, indem Sie [iwmcodec-Eigenschaften:: getcodecprop](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="29ff5-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="29ff5-112">Wenn Sie **IPropertyBag** verwenden, müssen Sie zuerst den FourCC-Wert des gewünschten komprimierten Formats mithilfe der Eigenschaft [mfpkey \_ FourCC](mfpkey-fourccproperty.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="29ff5-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ff5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29ff5-113">Requirements</span></span>



| <span data-ttu-id="29ff5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29ff5-114">Requirement</span></span> | <span data-ttu-id="29ff5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="29ff5-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29ff5-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29ff5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="29ff5-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29ff5-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="29ff5-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29ff5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="29ff5-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29ff5-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29ff5-120">Header</span><span class="sxs-lookup"><span data-stu-id="29ff5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ff5-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ff5-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ff5-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ff5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ff5-123">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29ff5-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




