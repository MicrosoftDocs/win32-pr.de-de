---
description: Der Klassen Bezeichner (CLSID) der dem topologieknoten zugeordneten Media Foundation Transformation (MFT).
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: MF_TOPONODE_TRANSFORM_OBJECTID-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527419"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="09f88-103">MF \_ toponode \_ Transform \_ objectID-Attribut</span><span class="sxs-lookup"><span data-stu-id="09f88-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="09f88-104">Der Klassen Bezeichner (CLSID) der dem topologieknoten zugeordneten Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="09f88-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="09f88-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="09f88-105">Data type</span></span>

<span data-ttu-id="09f88-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="09f88-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="09f88-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09f88-107">Remarks</span></span>

<span data-ttu-id="09f88-108">Dieses Attribut gilt für Transformations Knoten (**MF- \_ topologietransformations- \_ \_ Knoten**).</span><span class="sxs-lookup"><span data-stu-id="09f88-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="09f88-109">Anwendungen können dieses Attribut verwenden, um einen transfrom-Knoten zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="09f88-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="09f88-110">Wenn Sie dieses Attribut festlegen, müssen Sie [**imftopologynode:: SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) nicht mit einem Zeiger auf ein MFT-oder Aktivierungs Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="09f88-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="09f88-111">Wenn Sie hingegen **SetObject** aufrufen, muss dieses Attribut nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="09f88-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="09f88-112">Weitere Informationen finden Sie unter [Erstellen von Topologien](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="09f88-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="09f88-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="09f88-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f88-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09f88-114">Requirements</span></span>



| <span data-ttu-id="09f88-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09f88-115">Requirement</span></span> | <span data-ttu-id="09f88-116">Wert</span><span class="sxs-lookup"><span data-stu-id="09f88-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09f88-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09f88-117">Minimum supported client</span></span><br/> | <span data-ttu-id="09f88-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09f88-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="09f88-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09f88-119">Minimum supported server</span></span><br/> | <span data-ttu-id="09f88-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09f88-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09f88-121">Header</span><span class="sxs-lookup"><span data-stu-id="09f88-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f88-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f88-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f88-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09f88-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f88-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="09f88-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09f88-125">**Imfattributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="09f88-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="09f88-126">**Imfattributes:: SetGuid**</span><span class="sxs-lookup"><span data-stu-id="09f88-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="09f88-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="09f88-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="09f88-128">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="09f88-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="09f88-129">Erstellen von Topologien</span><span class="sxs-lookup"><span data-stu-id="09f88-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="09f88-130">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="09f88-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




