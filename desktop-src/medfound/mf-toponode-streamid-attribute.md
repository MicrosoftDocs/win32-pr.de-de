---
description: Der Datenstrom Bezeichner der Stream-Senke, die diesem topologieknoten zugeordnet ist.
ms.assetid: 0b8060ab-1463-45c2-8277-d15122561248
title: MF_TOPONODE_STREAMID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2377183927cf75c6e0a7436384426dcab94680c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345171"
---
# <a name="mf_toponode_streamid-attribute"></a><span data-ttu-id="282ce-103">MF- \_ toponode- \_ streamid-Attribut</span><span class="sxs-lookup"><span data-stu-id="282ce-103">MF\_TOPONODE\_STREAMID attribute</span></span>

<span data-ttu-id="282ce-104">Der Datenstrom Bezeichner der Stream-Senke, die diesem topologieknoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="282ce-104">The stream identifier of the stream sink associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="282ce-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="282ce-105">Data type</span></span>

<span data-ttu-id="282ce-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="282ce-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="282ce-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="282ce-107">Remarks</span></span>

<span data-ttu-id="282ce-108">Dieses Attribut gilt für Ausgabe Knoten (**MF- \_ topologieausgabe- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="282ce-108">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="282ce-109">Wenn die Medien Sitzung die Topologie lädt, fragt Sie die Medien Senke nach einer streamsenke mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="282ce-109">When the Media Session loads the topology, it queries the media sink for a stream sink with the specified identifier.</span></span> <span data-ttu-id="282ce-110">Wenn dies nicht möglich ist, wird versucht, der Medien Senke eine neue streamsenke hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="282ce-110">If that fails, it attempts to add a new stream sink to the media sink.</span></span>

<span data-ttu-id="282ce-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="282ce-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="282ce-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="282ce-112">Requirements</span></span>



| <span data-ttu-id="282ce-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="282ce-113">Requirement</span></span> | <span data-ttu-id="282ce-114">Wert</span><span class="sxs-lookup"><span data-stu-id="282ce-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="282ce-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="282ce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="282ce-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="282ce-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="282ce-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="282ce-117">Minimum supported server</span></span><br/> | <span data-ttu-id="282ce-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="282ce-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="282ce-119">Header</span><span class="sxs-lookup"><span data-stu-id="282ce-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="282ce-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="282ce-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="282ce-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="282ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="282ce-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="282ce-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="282ce-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="282ce-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="282ce-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="282ce-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="282ce-125">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="282ce-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="282ce-126">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="282ce-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




