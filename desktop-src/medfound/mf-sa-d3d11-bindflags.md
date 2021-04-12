---
description: Gibt die Bindungsflags an, die beim Zuordnen von Microsoft Direct3D 11-Oberflächen für Medien Beispiele verwendet werden.
ms.assetid: C3B475B1-9A44-47EA-BCE7-D3D0FB56DDAC
title: MF_SA_D3D11_BINDFLAGS-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb5ae4161a6782a3ea7a69b471044e43c5ee7a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345838"
---
# <a name="mf_sa_d3d11_bindflags-attribute"></a><span data-ttu-id="e1fc3-103">MF \_ sa \_ D3D11 \_ bindflags-Attribut</span><span class="sxs-lookup"><span data-stu-id="e1fc3-103">MF\_SA\_D3D11\_BINDFLAGS attribute</span></span>

<span data-ttu-id="e1fc3-104">Gibt die Bindungsflags an, die beim Zuordnen von Microsoft Direct3D 11-Oberflächen für Medien Beispiele verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-104">Specifies the binding flags to use when allocating Microsoft Direct3D 11 surfaces for media samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="e1fc3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1fc3-105">Data type</span></span>

<span data-ttu-id="e1fc3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e1fc3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e1fc3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1fc3-107">Remarks</span></span>

<span data-ttu-id="e1fc3-108">Der Wert dieses Attributs ist ein bitweises **or** von [**D3D11 \_ Bind- \_ Flag**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) -Flags.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-108">The value of this attribute is a bitwise **OR** of [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) flags.</span></span>

### <a name="microsoft-media-foundation-transforms"></a><span data-ttu-id="e1fc3-109">Microsoft Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="e1fc3-109">Microsoft Media Foundation Transforms</span></span>

<span data-ttu-id="e1fc3-110">In diesem Kontext wird das-Attribut nur angewendet, wenn die Microsoft Media Foundation Transformation (MFT) **true** für das MF-Attribut [ \_ \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-110">In this context, the attribute applies only when the Microsoft Media Foundation transform (MFT) returns **TRUE** for the [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) attribute.</span></span>

<span data-ttu-id="e1fc3-111">Wenn eine MFT Direct3D 11 unterstützt, stellt dieses Attribut einen Hinweis für die MFT bereit, wenn Microsoft Direct3D-Oberflächen für die Ausgabe zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-111">If an MFT supports Direct3D 11, this attribute provides a hint to the MFT when allocating Microsoft Direct3D surfaces for output.</span></span> <span data-ttu-id="e1fc3-112">Legen Sie das-Attribut wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="e1fc3-112">Set the attribute as follows:</span></span>

1.  <span data-ttu-id="e1fc3-113">Aufrufen von [**imftransform:: getoutputstreamtribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) zum Abrufen des MFT-Attribut Speicher.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-113">Call [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) to get the MFT attribute store.</span></span>
2.  <span data-ttu-id="e1fc3-114">Rückrufe [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e1fc3-114">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

<span data-ttu-id="e1fc3-115">Die Media Foundation Pipeline legt das-Attribut vor dem Starten des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-115">The Media Foundation pipeline sets the attribute before streaming starts.</span></span> <span data-ttu-id="e1fc3-116">Der MFT sollte die Einstellung bei der Zuweisung von Oberflächen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-116">The MFT should attempt to honor the setting when it allocates surfaces.</span></span> <span data-ttu-id="e1fc3-117">Wenn dies nicht möglich ist, kann das MFT das Attribut ignorieren und nicht die Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-117">If that is not possible, the MFT can ignore the attribute, rather than failing the allocation.</span></span>

<span data-ttu-id="e1fc3-118">Wenn der MFT außerdem Direct3D-Oberflächen für die Eingabe erfordert, kann er dieses Attribut als Hinweis dafür verfügbar machen, wie die Eingabe Oberflächen zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-118">In addition, if the MFT requires Direct3D surfaces for input, it can expose this attribute as a hint for how the input surfaces should be allocated.</span></span> <span data-ttu-id="e1fc3-119">Fragen Sie das Attribut wie folgt ab:</span><span class="sxs-lookup"><span data-stu-id="e1fc3-119">Query the attribute as follows:</span></span>

1.  <span data-ttu-id="e1fc3-120">Aufrufen von [**imftransform:: getinputstreamattributs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) , um die Eingabedaten Strom Attribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-120">Call [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) to get the input stream attributes.</span></span>
2.  <span data-ttu-id="e1fc3-121">Rückrufe [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e1fc3-121">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

### <a name="sample-allocator"></a><span data-ttu-id="e1fc3-122">Beispiel Zuweisung</span><span class="sxs-lookup"><span data-stu-id="e1fc3-122">Sample Allocator</span></span>

<span data-ttu-id="e1fc3-123">Dieses Attribut kann für die Video Sample-Zuweisung in der [**IMF-Methode IMF videosamplezuordcatorex:: initializesampledepcatorex**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e1fc3-123">This attribute can be set on the video sample allocator, in the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1fc3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1fc3-124">Requirements</span></span>



| <span data-ttu-id="e1fc3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1fc3-125">Requirement</span></span> | <span data-ttu-id="e1fc3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e1fc3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fc3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1fc3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e1fc3-128">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1fc3-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e1fc3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1fc3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e1fc3-130">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="e1fc3-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e1fc3-131">Header</span><span class="sxs-lookup"><span data-stu-id="e1fc3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1fc3-132"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e1fc3-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1fc3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1fc3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fc3-134">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e1fc3-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
