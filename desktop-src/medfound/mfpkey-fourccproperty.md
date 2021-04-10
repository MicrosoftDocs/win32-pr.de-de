---
description: Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: MFPKEY_FOURCC-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959418"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="feb31-103">Mfpkey \_ FourCC-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="feb31-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="feb31-104">Gibt den FourCC-Wert an, der den Encoder identifiziert, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="feb31-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="feb31-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="feb31-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="feb31-106">g \_ wszwmvcfourcc</span><span class="sxs-lookup"><span data-stu-id="feb31-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="feb31-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="feb31-107">Data Type</span></span>

<span data-ttu-id="feb31-108">VT \_ I4 (FourCC-Wert)</span><span class="sxs-lookup"><span data-stu-id="feb31-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="feb31-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="feb31-109">Remarks</span></span>

<span data-ttu-id="feb31-110">Sie müssen diesen Wert festlegen, bevor Sie die Werte für die folgenden Eigenschaften mithilfe von **IPropertyBag** oder **IPropertyStore** abrufen:</span><span class="sxs-lookup"><span data-stu-id="feb31-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="feb31-111">mfpkey \_ bufferfullnessinfirstbyte</span><span class="sxs-lookup"><span data-stu-id="feb31-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="feb31-112">mfpkey- \_ passesempfohlen</span><span class="sxs-lookup"><span data-stu-id="feb31-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="feb31-113">Zum Abrufen der Werte der zuvor aufgeführten FourCC-abhängigen Eigenschaften sollten Sie [**iwmcodecproperties:: getcodecprop**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) verwenden.</span><span class="sxs-lookup"><span data-stu-id="feb31-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="feb31-114">Wenn Sie **getcodecprop** verwenden, müssen Sie **mfpkey \_ FourCC** nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="feb31-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb31-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="feb31-115">Requirements</span></span>



| <span data-ttu-id="feb31-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="feb31-116">Requirement</span></span> | <span data-ttu-id="feb31-117">Wert</span><span class="sxs-lookup"><span data-stu-id="feb31-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feb31-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="feb31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="feb31-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="feb31-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="feb31-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="feb31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="feb31-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="feb31-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="feb31-122">Header</span><span class="sxs-lookup"><span data-stu-id="feb31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb31-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb31-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb31-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="feb31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb31-125">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="feb31-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




