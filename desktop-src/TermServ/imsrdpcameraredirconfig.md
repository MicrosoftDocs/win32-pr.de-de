---
title: IMsRdpCameraRedirConfig-Schnittstelle
description: Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.
ms.tgt_platform: multiple
keywords:
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste
- Imsrdpcameraredirconfig-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520307"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="63b57-105">IMsRdpCameraRedirConfig-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="63b57-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="63b57-106">Stellt die Konfigurationen für eine Kamera dar, die für die Umleitung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="63b57-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="63b57-107">Member</span><span class="sxs-lookup"><span data-stu-id="63b57-107">Members</span></span>

<span data-ttu-id="63b57-108">Die **imsrdpcameraredirconfig** -Schnittstelle erbt von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="63b57-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="63b57-109">**Imsrdpcameraredirconfig** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="63b57-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="63b57-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63b57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63b57-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="63b57-111">Properties</span></span>

<span data-ttu-id="63b57-112">Die **imsrdpcameraredirconfig** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="63b57-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="63b57-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63b57-113">Property</span></span>         | <span data-ttu-id="63b57-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="63b57-114">Access type</span></span>           | <span data-ttu-id="63b57-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63b57-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="63b57-116">**Deviceexistiert**</span><span class="sxs-lookup"><span data-stu-id="63b57-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="63b57-117">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63b57-117">Read-only</span></span> | <span data-ttu-id="63b57-118">Gibt an, ob das Kamera Gerät zurzeit vorhanden ist (d. h., die Kamera ist verbunden).</span><span class="sxs-lookup"><span data-stu-id="63b57-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="63b57-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="63b57-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="63b57-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63b57-120">Read-only</span></span> |    <span data-ttu-id="63b57-121">Ruft den anzeigen amen der Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="63b57-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="63b57-122">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="63b57-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="63b57-123">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63b57-123">Read-only</span></span> |  <span data-ttu-id="63b57-124">Ruft die Instanz-ID der Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="63b57-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="63b57-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="63b57-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="63b57-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63b57-126">Read-only</span></span> |    <span data-ttu-id="63b57-127">Ruft die Instanz-ID der übergeordneten Instanz der Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="63b57-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="63b57-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="63b57-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="63b57-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="63b57-129">Read/Write</span></span> |  <span data-ttu-id="63b57-130">Gibt an, ob die Kamera umgeleitet wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="63b57-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="63b57-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="63b57-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="63b57-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="63b57-132">Read-only</span></span> |   <span data-ttu-id="63b57-133">Ruft den symbolischen Link der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera ab.</span><span class="sxs-lookup"><span data-stu-id="63b57-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="63b57-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63b57-134">Requirements</span></span>

| <span data-ttu-id="63b57-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63b57-135">Requirement</span></span> | <span data-ttu-id="63b57-136">Wert</span><span class="sxs-lookup"><span data-stu-id="63b57-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="63b57-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63b57-137">Minimum supported client</span></span>| <span data-ttu-id="63b57-138">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="63b57-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="63b57-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="63b57-139">Type library</span></span>            | <span data-ttu-id="63b57-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="63b57-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="63b57-141">DLL</span><span class="sxs-lookup"><span data-stu-id="63b57-141">DLL</span></span>                  | <span data-ttu-id="63b57-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="63b57-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="63b57-143">IID</span><span class="sxs-lookup"><span data-stu-id="63b57-143">IID</span></span>                      | <span data-ttu-id="63b57-144">IID \_ imsrdpcameraredirconfig ist als 09750604-D625-47c1-9bcd-F09F735705D7 definiert.</span><span class="sxs-lookup"><span data-stu-id="63b57-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="63b57-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63b57-145">See also</span></span>

- [<span data-ttu-id="63b57-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="63b57-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="63b57-147">**IMsRdpClientNonScriptable7:: cameraredirconfigcollection**</span><span class="sxs-lookup"><span data-stu-id="63b57-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)