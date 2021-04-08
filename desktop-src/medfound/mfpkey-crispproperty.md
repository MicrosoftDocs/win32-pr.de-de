---
description: Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität der Codec-Ausgabe an.
ms.assetid: 63915450-71c5-4097-91d7-5817249c1cda
title: MFPKEY_CRISP-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ff20b37bcedf3995ec3e16178b823c40b352ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755488"
---
# <a name="mfpkey_crisp-property"></a><span data-ttu-id="1d382-103">Mfpkey- \_ Eigenschaft (Crisp)</span><span class="sxs-lookup"><span data-stu-id="1d382-103">MFPKEY\_CRISP Property</span></span>

<span data-ttu-id="1d382-104">Gibt eine numerische Darstellung der Kompromisse zwischen Bewegungs Glätte und Bildqualität der Codec-Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="1d382-104">Specifies a numeric representation of the tradeoff between motion smoothness and image quality of codec output.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1d382-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="1d382-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1d382-106">g \_ wszwmvccrisp</span><span class="sxs-lookup"><span data-stu-id="1d382-106">g\_wszWMVCCrisp</span></span>

## <a name="data-type"></a><span data-ttu-id="1d382-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1d382-107">Data Type</span></span>

<span data-ttu-id="1d382-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1d382-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1d382-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="1d382-109">Default Value</span></span>

<span data-ttu-id="1d382-110">75</span><span class="sxs-lookup"><span data-stu-id="1d382-110">75</span></span>

## <a name="remarks"></a><span data-ttu-id="1d382-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d382-111">Remarks</span></span>

<span data-ttu-id="1d382-112">Dieser ganzzahlige Wert kann zwischen 0 und 100 liegen.</span><span class="sxs-lookup"><span data-stu-id="1d382-112">This integer value can range from 0 to 100.</span></span> <span data-ttu-id="1d382-113">Je höher der Wert ist, desto mehr wird der Codec die Codierung für die Bildqualität einzelner Frames optimieren, was normalerweise die Bewegungs Glätte reduziert.</span><span class="sxs-lookup"><span data-stu-id="1d382-113">The higher the value, the more the codec will optimize encoding for the image quality of individual frames, which usually reduces motion smoothness.</span></span>

<span data-ttu-id="1d382-114">Diese Eigenschaft sollte nur für die CBR-Codierung (Constant-Bit-Rate) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1d382-114">This property should be set only for constant-bit-rate (CBR) encoding.</span></span> <span data-ttu-id="1d382-115">Die Optimierungen für die Codierung variabler Bitrate (VBR) funktionieren anders.</span><span class="sxs-lookup"><span data-stu-id="1d382-115">The optimizations for variable-bit-rate (VBR) encoding work differently.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d382-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d382-116">Requirements</span></span>



| <span data-ttu-id="1d382-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d382-117">Requirement</span></span> | <span data-ttu-id="1d382-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1d382-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d382-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1d382-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1d382-120">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d382-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1d382-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1d382-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1d382-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1d382-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1d382-123">Header</span><span class="sxs-lookup"><span data-stu-id="1d382-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d382-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d382-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d382-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d382-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d382-126">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d382-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




