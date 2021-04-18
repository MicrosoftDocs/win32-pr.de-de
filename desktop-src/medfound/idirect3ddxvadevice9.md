---
description: Stellt einen Hardwarebeschleuniger für die DirectX-Video Beschleunigung (DXVA) 1,0 dar.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: IDirect3DDXVADevice9-Schnittstelle (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347114"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="18331-103">IDirect3DDXVADevice9-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="18331-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="18331-104">Stellt einen Hardwarebeschleuniger für die DirectX-Video Beschleunigung (DXVA) 1,0 dar.</span><span class="sxs-lookup"><span data-stu-id="18331-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="18331-105">Member</span><span class="sxs-lookup"><span data-stu-id="18331-105">Members</span></span>

<span data-ttu-id="18331-106">Die **IDirect3DDXVADevice9** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="18331-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18331-107">**IDirect3DDXVADevice9** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="18331-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="18331-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="18331-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18331-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="18331-109">Methods</span></span>

<span data-ttu-id="18331-110">Die **IDirect3DDXVADevice9** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="18331-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="18331-111">Methode</span><span class="sxs-lookup"><span data-stu-id="18331-111">Method</span></span>                                                  | <span data-ttu-id="18331-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="18331-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="18331-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="18331-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="18331-114">Startet die Verarbeitung zum Erstellen eines decodierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="18331-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="18331-115">**Endframe**</span><span class="sxs-lookup"><span data-stu-id="18331-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="18331-116">Beendet die Verarbeitung zum Erstellen eines decodierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="18331-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="18331-117">**Auszuführen**</span><span class="sxs-lookup"><span data-stu-id="18331-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="18331-118">Führt einen DXVA-Decodierungs Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="18331-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="18331-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="18331-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="18331-120">Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="18331-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="18331-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18331-121">Remarks</span></span>

<span data-ttu-id="18331-122">Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie [**IDirect3DVideoDevice9:: kreatedxvadevice**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="18331-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18331-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18331-123">Requirements</span></span>



| <span data-ttu-id="18331-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18331-124">Requirement</span></span> | <span data-ttu-id="18331-125">Wert</span><span class="sxs-lookup"><span data-stu-id="18331-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18331-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18331-126">Minimum supported client</span></span><br/> | <span data-ttu-id="18331-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18331-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18331-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18331-128">Minimum supported server</span></span><br/> | <span data-ttu-id="18331-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18331-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18331-130">Header</span><span class="sxs-lookup"><span data-stu-id="18331-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="18331-131"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="18331-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18331-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18331-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18331-133">Direct3D-Video Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="18331-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
