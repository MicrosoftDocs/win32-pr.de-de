---
title: Iwmdrmdeviceapp-Schnittstelle
description: Die iwmdrmdeviceapp-Schnittstelle ermöglicht es einer Anwendung, Lizenzen zu messen, zu synchronisieren und die DRM-Komponenten eines Geräts zu aktualisieren.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339511"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="01f0b-105">Iwmdrmdeviceapp-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="01f0b-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="01f0b-106">\[Das Windows Media DRM-Feature ist veraltet und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01f0b-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="01f0b-107">Verwenden Sie stattdessen [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="01f0b-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="01f0b-108">Die **iwmdrmdeviceapp** -Schnittstelle ermöglicht es einer Anwendung, Lizenzen zu messen, zu synchronisieren und die DRM-Komponenten eines Geräts zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="01f0b-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="01f0b-109">Diese Schnittstelle funktioniert nur mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="01f0b-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="01f0b-110">Um diese Schnittstelle zu erhalten, wenden Sie **cokreateinstance** an, und übergeben Sie CLSID \_ wmdrmdeviceapp.</span><span class="sxs-lookup"><span data-stu-id="01f0b-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="01f0b-111">Diese Schnittstelle ist in der Header Datei definiert, die aus wmdrmdeviceapp. idl erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="01f0b-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="01f0b-112">Dieser Header **\# enthält**"WMDM. h".</span><span class="sxs-lookup"><span data-stu-id="01f0b-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="01f0b-113">Möglicherweise müssen Sie diesen Dateinamen ändern, damit er mit dem aus WMDM. idl erstellten Header identisch ist.</span><span class="sxs-lookup"><span data-stu-id="01f0b-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="01f0b-114">Member</span><span class="sxs-lookup"><span data-stu-id="01f0b-114">Members</span></span>

<span data-ttu-id="01f0b-115">Die **iwmdrmdeviceapp** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="01f0b-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01f0b-116">**Iwmdrmdeviceapp** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="01f0b-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="01f0b-117">Methoden</span><span class="sxs-lookup"><span data-stu-id="01f0b-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01f0b-118">Methoden</span><span class="sxs-lookup"><span data-stu-id="01f0b-118">Methods</span></span>

<span data-ttu-id="01f0b-119">Die **iwmdrmdeviceapp** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="01f0b-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="01f0b-120">Methode</span><span class="sxs-lookup"><span data-stu-id="01f0b-120">Method</span></span>                                                                   | <span data-ttu-id="01f0b-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01f0b-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01f0b-122">**Acquiredevicedata**</span><span class="sxs-lookup"><span data-stu-id="01f0b-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="01f0b-123">Initialisiert oder setzt eine sichere Uhr des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="01f0b-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="01f0b-124">**Generatemeterchallenge**</span><span class="sxs-lookup"><span data-stu-id="01f0b-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="01f0b-125">Hiermit werden Messungs Daten von einem Gerät angefordert.</span><span class="sxs-lookup"><span data-stu-id="01f0b-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="01f0b-126">**Processmeterresponse**</span><span class="sxs-lookup"><span data-stu-id="01f0b-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="01f0b-127">Setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="01f0b-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="01f0b-128">**Querydevicestatus**</span><span class="sxs-lookup"><span data-stu-id="01f0b-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="01f0b-129">Fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.</span><span class="sxs-lookup"><span data-stu-id="01f0b-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="01f0b-130">**Synchronizelicenses**</span><span class="sxs-lookup"><span data-stu-id="01f0b-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="01f0b-131">Aktualisiert Lizenzen auf einem Gerät, wenn Sie bald ablaufen.</span><span class="sxs-lookup"><span data-stu-id="01f0b-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="01f0b-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01f0b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f0b-133">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="01f0b-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="01f0b-134">**Schnittstellen für Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="01f0b-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="01f0b-135">**Verwendung von Messungs Inhalten**</span><span class="sxs-lookup"><span data-stu-id="01f0b-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

