---
title: IMsRdpClientNonScriptable6-Schnittstelle
description: Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement. Wird von der IMsRdpClientNonScriptable5-Schnittstelle abgeleitet.
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable6-Schnittstelle Remotedesktopdienste
- IMsRdpClientNonScriptable6 Interface Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/19/2020
ms.locfileid: "104392326"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="881c9-106">IMsRdpClientNonScriptable6-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="881c9-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="881c9-107">Bietet Zugriff auf die nicht Skript fähigen Eigenschaften der Remote Sitzung eines Clients auf dem Remotedesktop ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="881c9-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="881c9-108">Wird von der [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) -Schnittstelle abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="881c9-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="881c9-109">Auf Methoden dieser Schnittstelle kann nur über die Vtable zugegriffen werden. Sie sind nicht zur Verwendung mit Skript fähigen Clients verfügbar.</span><span class="sxs-lookup"><span data-stu-id="881c9-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="881c9-110">Eine Instanz dieser Schnittstelle wird durch Aufrufen von [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das [**imstscax**](imstscax-interface.md) -Objekt abgerufen, wobei **IID \_ IMsRdpClientNonScriptable6** übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="881c9-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="881c9-111">Member</span><span class="sxs-lookup"><span data-stu-id="881c9-111">Members</span></span>

<span data-ttu-id="881c9-112">Die **IMsRdpClientNonScriptable6** -Schnittstelle erbt von [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span><span class="sxs-lookup"><span data-stu-id="881c9-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="881c9-113">**IMsRdpClientNonScriptable6** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="881c9-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="881c9-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="881c9-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="881c9-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="881c9-115">Methods</span></span>

<span data-ttu-id="881c9-116">Die **IMsRdpClientNonScriptable6** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="881c9-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="881c9-117">Methode</span><span class="sxs-lookup"><span data-stu-id="881c9-117">Method</span></span>            | <span data-ttu-id="881c9-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="881c9-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="881c9-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="881c9-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="881c9-120">Sendet einen breiten-und Längengrad Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="881c9-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="881c9-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="881c9-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="881c9-122">Sendet einen breiten-, Längen-und Höhen Wert an den Server, damit der geografische Standort des Clients in der Remote Sitzung wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="881c9-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="881c9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="881c9-123">Requirements</span></span>

| <span data-ttu-id="881c9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="881c9-124">Requirement</span></span> | <span data-ttu-id="881c9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="881c9-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="881c9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="881c9-126">Minimum supported client</span></span>| <span data-ttu-id="881c9-127">Windows 10, Version 1709 (Build 16299)</span><span class="sxs-lookup"><span data-stu-id="881c9-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="881c9-128">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="881c9-128">Type library</span></span>            | <span data-ttu-id="881c9-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="881c9-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="881c9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="881c9-130">DLL</span></span>                  | <span data-ttu-id="881c9-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="881c9-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="881c9-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="881c9-132">CLSID</span></span>                    | <span data-ttu-id="881c9-133">Die CLSID- \_ MsRdpClient12 ist als 0bda33b8-9af1-4065-989e-5a7f 1acb09d8 definiert.</span><span class="sxs-lookup"><span data-stu-id="881c9-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="881c9-134">CLSID \_ MsRdpClient12NotSafeForScripting ist als 3bb805c2-d9e2-4174-8a1e-c87d69563662 definiert</span><span class="sxs-lookup"><span data-stu-id="881c9-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="881c9-135">CLSID \_ MsRdpClient11 ist als 22a7e88c-5bf 5-4de6-B687-60b7331df190 definiert.</span><span class="sxs-lookup"><span data-stu-id="881c9-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="881c9-136">CLSID \_ MsRdpClient11NotSafeForScripting ist als 1df7c823-b2d4-4b54-975a-f2ac5d7cf8b8 definiert.</span><span class="sxs-lookup"><span data-stu-id="881c9-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="881c9-137">IID</span><span class="sxs-lookup"><span data-stu-id="881c9-137">IID</span></span>                      | <span data-ttu-id="881c9-138">IID \_ IMsRdpClientNonScriptable6 ist als 05293249-B28B-4db8-BE64-1b2t496b910e definiert.</span><span class="sxs-lookup"><span data-stu-id="881c9-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="881c9-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="881c9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881c9-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="881c9-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
