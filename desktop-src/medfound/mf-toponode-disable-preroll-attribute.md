---
description: Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: MF_TOPONODE_DISABLE_PREROLL-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373314"
---
# <a name="mf_toponode_disable_preroll-attribute"></a><span data-ttu-id="f373c-103">MF- \_ toponode- \_ Attribut deaktivieren ( \_ vorab)</span><span class="sxs-lookup"><span data-stu-id="f373c-103">MF\_TOPONODE\_DISABLE\_PREROLL attribute</span></span>

<span data-ttu-id="f373c-104">Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f373c-104">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="f373c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f373c-105">Data type</span></span>

<span data-ttu-id="f373c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f373c-106">**UINT32**</span></span>

<span data-ttu-id="f373c-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="f373c-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f373c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f373c-108">Remarks</span></span>

<span data-ttu-id="f373c-109">Dieses Attribut gilt für Ausgabe Knoten (**MF- \_ topologieausgabe- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="f373c-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="f373c-110">Wenn der Wert dieses Attributs **true** ist, werden von der Medien Sitzung keine Daten für die Medien Senke vorab erstellt, auch wenn die Medien Senke die [**imfmediasinkpreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f373c-110">If the value of this attribute is **TRUE**, the Media Session does not preroll any data to the media sink, even if the media sink exposes the [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) interface.</span></span> <span data-ttu-id="f373c-111">Wenn der Wert **false** ist, werden die Daten in der Medien Sitzung vorab erstellt, wenn die Medien Senke **imfmediasinkpreroll** implementiert.</span><span class="sxs-lookup"><span data-stu-id="f373c-111">If the value is **FALSE**, the Media Session prerolls data if the media sink implements **IMFMediaSinkPreroll**.</span></span> <span data-ttu-id="f373c-112">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f373c-112">The default value is **FALSE**.</span></span>

<span data-ttu-id="f373c-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f373c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f373c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f373c-114">Requirements</span></span>



| <span data-ttu-id="f373c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f373c-115">Requirement</span></span> | <span data-ttu-id="f373c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f373c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f373c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f373c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f373c-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f373c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f373c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f373c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f373c-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f373c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f373c-121">Header</span><span class="sxs-lookup"><span data-stu-id="f373c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f373c-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f373c-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f373c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f373c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f373c-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f373c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f373c-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f373c-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f373c-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="f373c-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f373c-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="f373c-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f373c-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="f373c-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




