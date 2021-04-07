---
description: Gibt den Status eines Versuchs zum Auflösen einer Topologie an.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: MF_TOPOLOGY_RESOLUTION_STATUS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863579"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="909a3-103">Status Attribut der MF- \_ topologieauflösung \_ \_</span><span class="sxs-lookup"><span data-stu-id="909a3-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="909a3-104">Gibt den Status eines Versuchs zum Auflösen einer Topologie an.</span><span class="sxs-lookup"><span data-stu-id="909a3-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="909a3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="909a3-105">Data type</span></span>

<span data-ttu-id="909a3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="909a3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="909a3-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="909a3-107">Remarks</span></span>

<span data-ttu-id="909a3-108">Das topologielader oder die Medien Sitzung kann dieses Attribut in einer Topologie festlegen.</span><span class="sxs-lookup"><span data-stu-id="909a3-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="909a3-109">Der Wert dieses Attributs ist ein bitweises **or** von Flags aus der-Enumeration der [**MF- \_ topologiestatusflags \_ \_ \_**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="909a3-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="909a3-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="909a3-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="909a3-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="909a3-111">Requirements</span></span>



| <span data-ttu-id="909a3-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="909a3-112">Requirement</span></span> | <span data-ttu-id="909a3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="909a3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="909a3-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="909a3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="909a3-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="909a3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="909a3-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="909a3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="909a3-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="909a3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="909a3-118">Header</span><span class="sxs-lookup"><span data-stu-id="909a3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="909a3-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="909a3-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="909a3-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="909a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="909a3-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="909a3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="909a3-122">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="909a3-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="909a3-123">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="909a3-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="909a3-124">**Imftopology**</span><span class="sxs-lookup"><span data-stu-id="909a3-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="909a3-125">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="909a3-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




