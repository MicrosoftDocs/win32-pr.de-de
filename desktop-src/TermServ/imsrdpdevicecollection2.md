---
title: IMsRdpDeviceCollection2-Schnittstelle
description: Stellt eine Auflistung von Geräte Objekten dar. Dies ist eine Erweiterung der imsrdpdebug-Schnittstelle.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- IMsRdpDeviceCollection2-Schnittstelle Remotedesktopdienste
- IMsRdpDeviceCollection2 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344072"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="2ca89-106">IMsRdpDeviceCollection2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ca89-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="2ca89-107">Stellt eine Auflistung von Geräte Objekten dar.</span><span class="sxs-lookup"><span data-stu-id="2ca89-107">Represents a collection of device objects.</span></span> <span data-ttu-id="2ca89-108">Dies ist eine Erweiterung der [**imsrdpdebug**](imsrdpdevicecollection.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2ca89-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="2ca89-109">Member</span><span class="sxs-lookup"><span data-stu-id="2ca89-109">Members</span></span>

<span data-ttu-id="2ca89-110">Die **IMsRdpDeviceCollection2** -Schnittstelle erbt von [**imsrdpde vicecollection**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="2ca89-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="2ca89-111">**IMsRdpDeviceCollection2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2ca89-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="2ca89-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ca89-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ca89-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ca89-113">Methods</span></span>

<span data-ttu-id="2ca89-114">Die **IMsRdpDeviceCollection2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2ca89-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="2ca89-115">Methode</span><span class="sxs-lookup"><span data-stu-id="2ca89-115">Method</span></span>                                                                         | <span data-ttu-id="2ca89-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ca89-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ca89-117">**Adddevicebyinstanceid**</span><span class="sxs-lookup"><span data-stu-id="2ca89-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="2ca89-118">Fügt der Geräte Sammlung ein nicht aufgeführtes Gerät hinzu.</span><span class="sxs-lookup"><span data-stu-id="2ca89-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="2ca89-119">**Redirectnow**</span><span class="sxs-lookup"><span data-stu-id="2ca89-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="2ca89-120">Erzwingt das umgeleitet oder Entfernen von Geräten, die in der Sammlung ausgewählt oder nicht ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="2ca89-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2ca89-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ca89-121">Requirements</span></span>



| <span data-ttu-id="2ca89-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ca89-122">Requirement</span></span> | <span data-ttu-id="2ca89-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2ca89-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca89-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ca89-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2ca89-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2ca89-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="2ca89-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ca89-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2ca89-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2ca89-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="2ca89-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2ca89-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="2ca89-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca89-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="2ca89-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2ca89-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ca89-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ca89-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="2ca89-132">IID</span><span class="sxs-lookup"><span data-stu-id="2ca89-132">IID</span></span><br/>                      | <span data-ttu-id="2ca89-133">IID \_ IMsRdpDeviceCollection2 ist als e0e5d68a-f2e7-4350-adfe-ac0e08d74de0 definiert.</span><span class="sxs-lookup"><span data-stu-id="2ca89-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





