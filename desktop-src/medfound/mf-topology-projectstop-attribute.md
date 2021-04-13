---
description: Gibt die Startzeit für eine Topologie relativ zum Anfang der ersten Topologie in der Sequenz an.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: MF_TOPOLOGY_PROJECTSTOP-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528232"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="2f794-103">Das MF- \_ topologieprojectstoppattribut \_</span><span class="sxs-lookup"><span data-stu-id="2f794-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="2f794-104">Gibt die Startzeit für eine Topologie relativ zum Anfang der ersten Topologie in der Sequenz an.</span><span class="sxs-lookup"><span data-stu-id="2f794-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="2f794-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2f794-105">Data type</span></span>

<span data-ttu-id="2f794-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2f794-106">**UINT64**</span></span>

<span data-ttu-id="2f794-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="2f794-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f794-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f794-108">Remarks</span></span>

<span data-ttu-id="2f794-109">Der Wert wird in Einheiten von 100 Nanosekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="2f794-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="2f794-110">Wenn die Medien Sitzung mit dem [**\_ \_ globalen \_ time**](mf-session-global-time-attribute.md) -Attribut der MF-Sitzung gleich **true** erstellt wurde, müssen alle Topologien das Projekt für die **MF- \_ Topologie \_ projectstoppt** enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f794-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="2f794-111">Andernfalls dürfen Topologien nicht das Projekt für die **MF- \_ Topologie \_ projectstoppt** enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f794-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="2f794-112">Weitere Informationen finden Sie unter [Sequenz Präsentations Zeiten](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="2f794-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="2f794-113">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="2f794-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="2f794-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="2f794-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f794-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f794-115">Requirements</span></span>



| <span data-ttu-id="2f794-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f794-116">Requirement</span></span> | <span data-ttu-id="2f794-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2f794-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2f794-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f794-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f794-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f794-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2f794-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f794-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f794-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f794-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2f794-122">Header</span><span class="sxs-lookup"><span data-stu-id="2f794-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f794-123"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f794-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f794-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f794-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f794-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="2f794-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f794-126">Sequenz Präsentations Zeiten</span><span class="sxs-lookup"><span data-stu-id="2f794-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="2f794-127">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="2f794-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="2f794-128">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="2f794-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="2f794-129">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="2f794-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="2f794-130">**MF- \_ Topologie \_ ProjectStart**</span><span class="sxs-lookup"><span data-stu-id="2f794-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




