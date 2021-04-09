---
description: Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologietknoten.
ms.assetid: fae90e06-0ae0-43a1-aaf2-7a2d1dabc79b
title: MF_TOPONODE_ERRORCODE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4b28c8f630d06f3545ca44c5b064c0bb6dac32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130144"
---
# <a name="mf_toponode_errorcode-attribute"></a><span data-ttu-id="004e4-103">MF- \_ toponode- \_ errorCode-Attribut</span><span class="sxs-lookup"><span data-stu-id="004e4-103">MF\_TOPONODE\_ERRORCODE attribute</span></span>

<span data-ttu-id="004e4-104">Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologietknoten.</span><span class="sxs-lookup"><span data-stu-id="004e4-104">Contains the error code from the most recent connection failure for this toplogy node.</span></span>

## <a name="data-type"></a><span data-ttu-id="004e4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="004e4-105">Data type</span></span>

<span data-ttu-id="004e4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="004e4-106">**UINT32**</span></span>

<span data-ttu-id="004e4-107">"Ttreat" als **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="004e4-107">Ttreat as an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="004e4-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="004e4-108">Remarks</span></span>

<span data-ttu-id="004e4-109">Dieses Attribut gilt für alle Knoten Typen.</span><span class="sxs-lookup"><span data-stu-id="004e4-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="004e4-110">Der Wert dieses Attributs ist ein **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="004e4-110">The value of this attribute is an **HRESULT** value.</span></span>

<span data-ttu-id="004e4-111">Das-Attribut kann von der Medien Sitzung oder dem topologielader festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="004e4-111">The Media Session or the topology loader might set the attribute.</span></span> <span data-ttu-id="004e4-112">Anwendungen lesen dieses Attribut in der Regel, ohne es festzulegen.</span><span class="sxs-lookup"><span data-stu-id="004e4-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="004e4-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="004e4-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="004e4-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="004e4-114">Requirements</span></span>



| <span data-ttu-id="004e4-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="004e4-115">Requirement</span></span> | <span data-ttu-id="004e4-116">Wert</span><span class="sxs-lookup"><span data-stu-id="004e4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="004e4-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="004e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="004e4-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="004e4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="004e4-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="004e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="004e4-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="004e4-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="004e4-121">Header</span><span class="sxs-lookup"><span data-stu-id="004e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="004e4-122"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="004e4-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="004e4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="004e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="004e4-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="004e4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="004e4-125">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="004e4-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="004e4-126">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="004e4-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="004e4-127">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="004e4-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="004e4-128">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="004e4-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




