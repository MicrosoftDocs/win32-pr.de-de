---
description: Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist.
ms.assetid: f7d98837-75da-48cc-8307-091be2d95392
title: MF_TOPONODE_PRIMARYOUTPUT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4130f1df4789ad910ae013eab43168983b47c316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344168"
---
# <a name="mf_toponode_primaryoutput-attribute"></a><span data-ttu-id="ed2aa-103">MF \_ toponode \_ primaryoutput-Attribut</span><span class="sxs-lookup"><span data-stu-id="ed2aa-103">MF\_TOPONODE\_PRIMARYOUTPUT attribute</span></span>

<span data-ttu-id="ed2aa-104">Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist.</span><span class="sxs-lookup"><span data-stu-id="ed2aa-104">Indicates which output is the primary output on a tee node.</span></span>

## <a name="data-type"></a><span data-ttu-id="ed2aa-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ed2aa-105">Data type</span></span>

<span data-ttu-id="ed2aa-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ed2aa-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ed2aa-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed2aa-107">Remarks</span></span>

<span data-ttu-id="ed2aa-108">Dieses Attribut gilt für Tee-Knoten (**MF- \_ topologieknoten \_ \_**).</span><span class="sxs-lookup"><span data-stu-id="ed2aa-108">This attribute applies to tee nodes (**MF\_TOPOLOGY\_TEE\_NODE**).</span></span>

<span data-ttu-id="ed2aa-109">Der Wert dieses Attributs ist der null basierte Index einer Ausgabe Verbindung auf diesem Tee-Knoten.</span><span class="sxs-lookup"><span data-stu-id="ed2aa-109">The value of this attribute is the zero-based index of an output connection on this tee node.</span></span> <span data-ttu-id="ed2aa-110">Dieser Wert gibt an, welche Ausgabe der primäre Ausgabestream ist.</span><span class="sxs-lookup"><span data-stu-id="ed2aa-110">This value indicates which output is the primary output stream.</span></span> <span data-ttu-id="ed2aa-111">Die Pipeline wartet auf eine Anforderung von der primären Ausgabe, bevor Anforderungen aus den anderen Ausgaben verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="ed2aa-111">The pipeline waits for a request from the primary output before processing requests from the other outputs.</span></span>

<span data-ttu-id="ed2aa-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ed2aa-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2aa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed2aa-113">Requirements</span></span>



| <span data-ttu-id="ed2aa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed2aa-114">Requirement</span></span> | <span data-ttu-id="ed2aa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ed2aa-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2aa-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed2aa-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed2aa-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed2aa-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ed2aa-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed2aa-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed2aa-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed2aa-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ed2aa-120">Header</span><span class="sxs-lookup"><span data-stu-id="ed2aa-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed2aa-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed2aa-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed2aa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed2aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2aa-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ed2aa-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ed2aa-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ed2aa-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ed2aa-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="ed2aa-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ed2aa-126">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="ed2aa-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ed2aa-127">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="ed2aa-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




