---
description: Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt.
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: MF_TOPONODE_D3DAWARE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d94d06f2834092159fb813ecffd69ec8a157c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485811"
---
# <a name="mf_toponode_d3daware-attribute"></a><span data-ttu-id="05c8e-103">MF \_ toponode \_ D3DAWARE-Attribut</span><span class="sxs-lookup"><span data-stu-id="05c8e-103">MF\_TOPONODE\_D3DAWARE attribute</span></span>

<span data-ttu-id="05c8e-104">Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05c8e-104">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA).</span></span>

## <a name="data-type"></a><span data-ttu-id="05c8e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="05c8e-105">Data type</span></span>

<span data-ttu-id="05c8e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="05c8e-106">**UINT32**</span></span>

<span data-ttu-id="05c8e-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="05c8e-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05c8e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05c8e-108">Remarks</span></span>

<span data-ttu-id="05c8e-109">Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="05c8e-109">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="05c8e-110">Anwendungen verwenden dieses Attribut in der Regel nicht direkt.</span><span class="sxs-lookup"><span data-stu-id="05c8e-110">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="05c8e-111">Die Medien Sitzung legt dieses Attribut für einen Transformations Knoten fest, wenn die zugrunde liegende Media Foundation Transformation über das D3D-Attribut " [**MF \_ sa \_ \_**](mf-sa-d3d-aware-attribute.md) " verfügt.</span><span class="sxs-lookup"><span data-stu-id="05c8e-111">The Media Session sets this attribute on a transform node if the underlying Media Foundation transform has the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute.</span></span>

<span data-ttu-id="05c8e-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="05c8e-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="05c8e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05c8e-113">Requirements</span></span>



| <span data-ttu-id="05c8e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05c8e-114">Requirement</span></span> | <span data-ttu-id="05c8e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="05c8e-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="05c8e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05c8e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="05c8e-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05c8e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="05c8e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05c8e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="05c8e-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05c8e-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="05c8e-120">Header</span><span class="sxs-lookup"><span data-stu-id="05c8e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="05c8e-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c8e-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05c8e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05c8e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c8e-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="05c8e-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="05c8e-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="05c8e-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="05c8e-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="05c8e-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="05c8e-126">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="05c8e-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="05c8e-127">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="05c8e-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




