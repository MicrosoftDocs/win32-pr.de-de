---
description: Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medien Beispiele zugeteilt werden.
ms.assetid: E9A415FA-74BF-4822-BB0E-D8AAA7D73664
title: MF_SA_D3D11_USAGE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0609435cf42134f28e8464fd3173412836c8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214885"
---
# <a name="mf_sa_d3d11_usage-attribute"></a><span data-ttu-id="4eb2d-103">MF \_ sa \_ D3D11 \_ Usage-Attribut</span><span class="sxs-lookup"><span data-stu-id="4eb2d-103">MF\_SA\_D3D11\_USAGE attribute</span></span>

<span data-ttu-id="4eb2d-104">Gibt an, wie Microsoft Direct3D 11-Oberflächen für Medien Beispiele zugeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-104">Specifies how to allocate Microsoft Direct3D 11 surfaces for media samples.</span></span> <span data-ttu-id="4eb2d-105">Die Verwendung gibt direkt an, ob eine Stichprobe für die CPU oder die GPU zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-105">The usage directly reflects whether a sample is accessible by the CPU or GPU.</span></span>

## <a name="data-type"></a><span data-ttu-id="4eb2d-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4eb2d-106">Data type</span></span>

<span data-ttu-id="4eb2d-107">**D3D11 \_** Als **UInt32** gespeicherte Verwendung</span><span class="sxs-lookup"><span data-stu-id="4eb2d-107">**D3D11\_USAGE** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4eb2d-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4eb2d-108">Remarks</span></span>

<span data-ttu-id="4eb2d-109">Der Wert dieses Attributs ist ein [**D3D11 \_ Usage**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) -Wert.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-109">The value of this attribute is a [**D3D11\_USAGE**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) value.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="4eb2d-110">Microsoft Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="4eb2d-110">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="4eb2d-111">In diesem Kontext wird das-Attribut nur angewendet, wenn die Microsoft Media Foundation Transformation (MFT) **true** für das MF-Attribut [ \_ \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-111">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="4eb2d-112">Wenn eine MFT Direct3D 11 unterstützt, stellt dieses Attribut einen Hinweis für die MFT bereit, wenn Microsoft Direct3D-Oberflächen für die Ausgabe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-112">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="4eb2d-113">Legen Sie das-Attribut wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="4eb2d-113">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="4eb2d-114">Aufrufen von [**imftransform:: getoutputstreamtribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) zum Abrufen des MFT-Attribut Speicher.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-114">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="4eb2d-115">Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="4eb2d-115">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="4eb2d-116">Die Media Foundation Pipeline legt das-Attribut vor dem Starten des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-116">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="4eb2d-117">Der MFT sollte die Einstellung bei der Zuweisung von Oberflächen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-117">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="4eb2d-118">Wenn dies nicht möglich ist, kann das MFT das Attribut ignorieren und nicht die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-118">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="4eb2d-119">Wenn der MFT außerdem Direct3D-Oberflächen für die Eingabe erfordert, kann er dieses Attribut als Hinweis dafür verfügbar machen, wie die Eingabe Oberflächen zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-119">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="4eb2d-120">Fragen Sie das Attribut wie folgt ab:</span><span class="sxs-lookup"><span data-stu-id="4eb2d-120">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="4eb2d-121">Aufrufen von [**imftransform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , um die Eingabedaten Strom Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-121">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="4eb2d-122">Rückrufe [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="4eb2d-122">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="4eb2d-123">Beispiel Zuweisung</span><span class="sxs-lookup"><span data-stu-id="4eb2d-123">Sample Allocator</span></span>

<span data-ttu-id="4eb2d-124">Dieses Attribut kann für die Video Sample-Zuweisung in der [**IMF-Methode IMF videosamplezuordcatorex:: initializesampledepcatorex**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4eb2d-124">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eb2d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4eb2d-125">Requirements</span></span>



| <span data-ttu-id="4eb2d-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4eb2d-126">Requirement</span></span> | <span data-ttu-id="4eb2d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="4eb2d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4eb2d-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4eb2d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb2d-129">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4eb2d-129">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4eb2d-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4eb2d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb2d-131">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4eb2d-131">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4eb2d-132">Header</span><span class="sxs-lookup"><span data-stu-id="4eb2d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eb2d-133"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4eb2d-133"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eb2d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb2d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb2d-135">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4eb2d-135">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
