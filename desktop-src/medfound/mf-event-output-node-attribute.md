---
description: Identifiziert den topologieknoten für eine streamsenke.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: MF_EVENT_OUTPUT_NODE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354600"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="c3698-103">\_Attribut für \_ Ausgabe \_ Knoten des MF-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="c3698-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="c3698-104">Identifiziert den topologieknoten für eine streamsenke.</span><span class="sxs-lookup"><span data-stu-id="c3698-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="c3698-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c3698-105">Data type</span></span>

<span data-ttu-id="c3698-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c3698-106">**UINT64**</span></span>

<span data-ttu-id="c3698-107">Als [**topoid**](topoid.md)behandeln.</span><span class="sxs-lookup"><span data-stu-id="c3698-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3698-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3698-108">Remarks</span></span>

<span data-ttu-id="c3698-109">Der Wert dieses Attributs ist ein Knoten Bezeichner für einen Ausgabe Knoten in der aktuellen Topologie.</span><span class="sxs-lookup"><span data-stu-id="c3698-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="c3698-110">Um einen Zeiger auf den zugeordneten Knoten abzurufen, nennen Sie [**imftopology:: getNodeById**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) für die Topologie.</span><span class="sxs-lookup"><span data-stu-id="c3698-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="c3698-111">Dieses Attribut wird mit den folgenden Ereignissen verwendet:</span><span class="sxs-lookup"><span data-stu-id="c3698-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="c3698-112">Mesessionstreamsinkformatchanged</span><span class="sxs-lookup"><span data-stu-id="c3698-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="c3698-113">Mesinkinvalidieren</span><span class="sxs-lookup"><span data-stu-id="c3698-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="c3698-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="c3698-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3698-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3698-115">Requirements</span></span>



| <span data-ttu-id="c3698-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3698-116">Requirement</span></span> | <span data-ttu-id="c3698-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c3698-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3698-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3698-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3698-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3698-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c3698-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3698-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3698-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3698-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c3698-122">Header</span><span class="sxs-lookup"><span data-stu-id="c3698-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3698-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3698-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3698-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3698-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3698-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="c3698-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3698-126">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="c3698-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c3698-127">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="c3698-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="c3698-128">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="c3698-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




