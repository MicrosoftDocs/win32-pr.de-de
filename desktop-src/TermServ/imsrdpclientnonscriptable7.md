---
title: IMsRdpClientNonScriptable7-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable6-Schnittstelle abgeleitet.
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable7-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable7 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "106345572"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="c5d1e-106">IMsRdpClientNonScriptable7-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c5d1e-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="c5d1e-107">Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="c5d1e-108">Wird von der [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="c5d1e-109">Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="c5d1e-110">Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**imstscax**](imstscax-interface.md) -Objekt abgerufen, wobei **IID \_ IMsRdpClientNonScriptable7** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="c5d1e-111">Member</span><span class="sxs-lookup"><span data-stu-id="c5d1e-111">Members</span></span>

<span data-ttu-id="c5d1e-112">Die **IMsRdpClientNonScriptable7** -Schnittstelle erbt von [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="c5d1e-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="c5d1e-113">**IMsRdpClientNonScriptable7** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5d1e-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="c5d1e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="c5d1e-114">Methods</span></span>](#methods)
- [<span data-ttu-id="c5d1e-115">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5d1e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c5d1e-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="c5d1e-116">Methods</span></span>

<span data-ttu-id="c5d1e-117">Die **IMsRdpClientNonScriptable7** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="c5d1e-118">Methode</span><span class="sxs-lookup"><span data-stu-id="c5d1e-118">Method</span></span>            | <span data-ttu-id="c5d1e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5d1e-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="c5d1e-120">**Disabledpicurrsorscalingforprocess**</span><span class="sxs-lookup"><span data-stu-id="c5d1e-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="c5d1e-121">Deaktiviert die lokale Skalierung des Mauszeigers, der vom Server empfangen wurde. Dadurch wird sichergestellt, dass die Cursor Form ohne Änderung korrekt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="c5d1e-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5d1e-122">Properties</span></span>

<span data-ttu-id="c5d1e-123">Die **IMsRdpClientNonScriptable7** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="c5d1e-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c5d1e-124">Property</span></span>         | <span data-ttu-id="c5d1e-125">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c5d1e-125">Access type</span></span>           | <span data-ttu-id="c5d1e-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5d1e-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="c5d1e-127">**Cameraredirconfigcollection**</span><span class="sxs-lookup"><span data-stu-id="c5d1e-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="c5d1e-128">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5d1e-128">Read-only</span></span> |  <span data-ttu-id="c5d1e-129">Ruft die Auflistung der Kameras (und der zugeordneten Konfigurationen) ab, die für die Umleitung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="c5d1e-130">**Zwischenablage**</span><span class="sxs-lookup"><span data-stu-id="c5d1e-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="c5d1e-131">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5d1e-131">Read-only</span></span> |    <span data-ttu-id="c5d1e-132">Ruft den Zwischenablage Controller ab, der zum Synchronisieren der lokalen und Remote-zwischen Ablagen verwendet wird, wenn die manuelle Zwischenablage Synchronisierung aktiviert</span><span class="sxs-lookup"><span data-stu-id="c5d1e-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="c5d1e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5d1e-133">Requirements</span></span>

| <span data-ttu-id="c5d1e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5d1e-134">Requirement</span></span> | <span data-ttu-id="c5d1e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="c5d1e-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c5d1e-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5d1e-136">Minimum supported client</span></span>| <span data-ttu-id="c5d1e-137">Windows 10, Version 1803 (Build 17134)</span><span class="sxs-lookup"><span data-stu-id="c5d1e-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="c5d1e-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c5d1e-138">Type library</span></span>            | <span data-ttu-id="c5d1e-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c5d1e-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c5d1e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c5d1e-140">DLL</span></span>                  | <span data-ttu-id="c5d1e-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c5d1e-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c5d1e-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="c5d1e-142">CLSID</span></span>                    | <span data-ttu-id="c5d1e-143">Die CLSID- \_ MsRdpClient12 ist als 0bda33b8-9af1-4065-989e-5a7f 1acb09d8 definiert.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="c5d1e-144">CLSID \_ MsRdpClient12NotSafeForScripting ist als 3bb805c2-d9e2-4174-8a1e-c87d69563662 definiert</span><span class="sxs-lookup"><span data-stu-id="c5d1e-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="c5d1e-145">CLSID \_ MsRdpClient11 ist als 22a7e88c-5bf 5-4de6-B687-60b7331df190 definiert.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="c5d1e-146">CLSID \_ MsRdpClient11NotSafeForScripting ist als 1df7c823-b2d4-4b54-975a-f2ac5d7cf8b8 definiert.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="c5d1e-147">IID</span><span class="sxs-lookup"><span data-stu-id="c5d1e-147">IID</span></span>                      | <span data-ttu-id="c5d1e-148">IID \_ IMsRdpClientNonScriptable7 ist als 71b4a60a-fe21-46d8-a39b-8e32ba0c5ecc definiert.</span><span class="sxs-lookup"><span data-stu-id="c5d1e-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="c5d1e-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5d1e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d1e-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="c5d1e-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
