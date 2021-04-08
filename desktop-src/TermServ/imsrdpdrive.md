---
title: Imsrdpdrive-Schnittstelle
description: Enthält Informationen zu einem Laufwerks Objekt.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Imsrdpdrive-Schnittstelle Remotedesktopdienste
- Imsrdpdrive-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739992"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="faf6f-105">Imsrdpdrive-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="faf6f-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="faf6f-106">Enthält Informationen zu einem Laufwerks Objekt.</span><span class="sxs-lookup"><span data-stu-id="faf6f-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="faf6f-107">Member</span><span class="sxs-lookup"><span data-stu-id="faf6f-107">Members</span></span>

<span data-ttu-id="faf6f-108">Die **imsrdpdrive** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="faf6f-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="faf6f-109">**Imsrdpdrive** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="faf6f-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="faf6f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faf6f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="faf6f-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="faf6f-111">Properties</span></span>

<span data-ttu-id="faf6f-112">Die **imsrdpdrive** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="faf6f-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="faf6f-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="faf6f-113">Property</span></span>                                                            | <span data-ttu-id="faf6f-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="faf6f-114">Access type</span></span>           | <span data-ttu-id="faf6f-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="faf6f-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="faf6f-116">**Name**</span><span class="sxs-lookup"><span data-stu-id="faf6f-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="faf6f-117">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="faf6f-117">Read-only</span></span><br/>  | <span data-ttu-id="faf6f-118">Ruft den Namen des Laufwerks ab.</span><span class="sxs-lookup"><span data-stu-id="faf6f-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="faf6f-119">**Redirectionstate**</span><span class="sxs-lookup"><span data-stu-id="faf6f-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="faf6f-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="faf6f-120">Read/write</span></span><br/> | <span data-ttu-id="faf6f-121">Gibt den Umleitungs Status des Laufwerks an.</span><span class="sxs-lookup"><span data-stu-id="faf6f-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="faf6f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="faf6f-122">Requirements</span></span>



| <span data-ttu-id="faf6f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faf6f-123">Requirement</span></span> | <span data-ttu-id="faf6f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="faf6f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="faf6f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faf6f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="faf6f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="faf6f-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="faf6f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faf6f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="faf6f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="faf6f-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="faf6f-129">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="faf6f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="faf6f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf6f-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="faf6f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="faf6f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faf6f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="faf6f-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="faf6f-133">IID</span><span class="sxs-lookup"><span data-stu-id="faf6f-133">IID</span></span><br/>                      | <span data-ttu-id="faf6f-134">IID \_ imsrdpdrive ist als d28b5458-f694-47a8-8e61-40356a767e46 definiert.</span><span class="sxs-lookup"><span data-stu-id="faf6f-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="faf6f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faf6f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf6f-136">Remotedesktop-Webverbindung Referenz</span><span class="sxs-lookup"><span data-stu-id="faf6f-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="faf6f-137">**Imsrdpdrivecollection**</span><span class="sxs-lookup"><span data-stu-id="faf6f-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

