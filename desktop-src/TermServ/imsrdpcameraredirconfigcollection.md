---
title: IMsRdpCameraRedirConfigCollection-Schnittstelle
description: Stellt die Auflistung der Kameras (und der zugeordneten Konfigurationen) dar, die für die Umleitung verfügbar sind.
ms.tgt_platform: multiple
keywords:
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste
- Imsrdpcameraredirconfigcollection-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104123283"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="6b53a-105">IMsRdpCameraRedirConfigCollection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6b53a-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="6b53a-106">Stellt die Auflistung der Kameras (und der zugeordneten Konfigurationen) dar, die für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6b53a-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="6b53a-107">Member</span><span class="sxs-lookup"><span data-stu-id="6b53a-107">Members</span></span>

<span data-ttu-id="6b53a-108">Die **imsrdpcameraredirconfigcollection** -Schnittstelle erbt von **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="6b53a-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="6b53a-109">**Imsrdpcameraredirconfigcollection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6b53a-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="6b53a-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b53a-110">Methods</span></span>](#methods)
- [<span data-ttu-id="6b53a-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b53a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6b53a-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="6b53a-112">Methods</span></span>

<span data-ttu-id="6b53a-113">Die **imsrdpcameraredirconfigcollection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="6b53a-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="6b53a-114">Methode</span><span class="sxs-lookup"><span data-stu-id="6b53a-114">Method</span></span>            | <span data-ttu-id="6b53a-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b53a-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="6b53a-116">**AddConfig**</span><span class="sxs-lookup"><span data-stu-id="6b53a-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="6b53a-117">Fügt der Auflistung ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt hinzu (die entsprechende Kamera muss nicht verbunden sein).</span><span class="sxs-lookup"><span data-stu-id="6b53a-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="6b53a-118">**Neu einlesen**</span><span class="sxs-lookup"><span data-stu-id="6b53a-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="6b53a-119">Listet verbundene Kamerageräte auf.</span><span class="sxs-lookup"><span data-stu-id="6b53a-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="6b53a-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b53a-120">Properties</span></span>

<span data-ttu-id="6b53a-121">Die **imsrdpcameraredirconfigcollection** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6b53a-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="6b53a-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6b53a-122">Property</span></span>         | <span data-ttu-id="6b53a-123">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="6b53a-123">Access type</span></span>           | <span data-ttu-id="6b53a-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b53a-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="6b53a-125">**Byindex**</span><span class="sxs-lookup"><span data-stu-id="6b53a-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="6b53a-126">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b53a-126">Read-only</span></span> |  <span data-ttu-id="6b53a-127">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt nach dem Index in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="6b53a-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="6b53a-128">**Byinstanceid**</span><span class="sxs-lookup"><span data-stu-id="6b53a-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="6b53a-129">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b53a-129">Read-only</span></span> |    <span data-ttu-id="6b53a-130">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen Instanz-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b53a-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="6b53a-131">**Bysymboliclink**</span><span class="sxs-lookup"><span data-stu-id="6b53a-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="6b53a-132">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b53a-132">Read-only</span></span> |  <span data-ttu-id="6b53a-133">Gibt ein [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekt aus der Auflistung zurück, das der angegebenen symbolischen Verknüpfung der **KSCATEGORY_VIDEO_CAMERA** -Schnittstelle für die Kamera entspricht.</span><span class="sxs-lookup"><span data-stu-id="6b53a-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="6b53a-134">**Countdown**</span><span class="sxs-lookup"><span data-stu-id="6b53a-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="6b53a-135">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6b53a-135">Read-only</span></span> |    <span data-ttu-id="6b53a-136">Gibt die Anzahl der [imsrdpcameraredirconfig](imsrdpcameraredirconfig.md) -Objekte in der Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="6b53a-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="6b53a-137">**Encode Video**</span><span class="sxs-lookup"><span data-stu-id="6b53a-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="6b53a-138">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b53a-138">Read/Write</span></span> |  <span data-ttu-id="6b53a-139">Gibt an, ob der Videostream H. 264-codiert ist.</span><span class="sxs-lookup"><span data-stu-id="6b53a-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="6b53a-140">**Encodingquality**</span><span class="sxs-lookup"><span data-stu-id="6b53a-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="6b53a-141">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b53a-141">Read/Write</span></span> |    <span data-ttu-id="6b53a-142">Gibt die Codierungsqualität an (Bitrate).</span><span class="sxs-lookup"><span data-stu-id="6b53a-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="6b53a-143">**Redirectbydefault**</span><span class="sxs-lookup"><span data-stu-id="6b53a-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="6b53a-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="6b53a-144">Read/Write</span></span> |   <span data-ttu-id="6b53a-145">Gibt an, ob eine neue Kamera standardmäßig umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="6b53a-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="6b53a-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b53a-146">Requirements</span></span>

| <span data-ttu-id="6b53a-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b53a-147">Requirement</span></span> | <span data-ttu-id="6b53a-148">Wert</span><span class="sxs-lookup"><span data-stu-id="6b53a-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="6b53a-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b53a-149">Minimum supported client</span></span>| <span data-ttu-id="6b53a-150">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="6b53a-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="6b53a-151">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6b53a-151">Type library</span></span>            | <span data-ttu-id="6b53a-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6b53a-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="6b53a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6b53a-153">DLL</span></span>                  | <span data-ttu-id="6b53a-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="6b53a-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="6b53a-155">IID</span><span class="sxs-lookup"><span data-stu-id="6b53a-155">IID</span></span>                      | <span data-ttu-id="6b53a-156">IID \_ imsrdpcameraredirconfigcollection ist als AE45252B-aaab-4504-B681-649d6073a37a definiert.</span><span class="sxs-lookup"><span data-stu-id="6b53a-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="6b53a-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b53a-157">See also</span></span>

- [<span data-ttu-id="6b53a-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="6b53a-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="6b53a-159">**IMsRdpClientNonScriptable7:: cameraredirconfigcollection**</span><span class="sxs-lookup"><span data-stu-id="6b53a-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
