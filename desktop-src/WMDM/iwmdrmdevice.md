---
title: Iwmdrmdevice-Schnittstelle
description: Diese Schnittstelle ist nicht dafür vorgesehen, von einem Dienstanbieter implementiert zu werden. Sie wird jedoch für eine komplette Dokumentation bereitgestellt. Die iwmdrmdevice-Schnittstelle ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte verwendet wird.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager
- Iwmdrmdevice-Schnittstelle Windows Media Device Manager, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315476"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="f43c1-105">Iwmdrmdevice-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f43c1-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="f43c1-106">Diese Schnittstelle ist nicht dafür vorgesehen, von einem Dienstanbieter implementiert zu werden. Sie wird jedoch für eine komplette Dokumentation bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f43c1-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="f43c1-107">Die **iwmdrmdevice** -Schnittstelle ermöglicht einem sicheren Inhaltsanbieter die Kommunikation mit Geräten, von denen Windows Media DRM 10 für tragbare Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f43c1-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="f43c1-108">Member</span><span class="sxs-lookup"><span data-stu-id="f43c1-108">Members</span></span>

<span data-ttu-id="f43c1-109">Die **iwmdrmdevice** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f43c1-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f43c1-110">**Iwmdrmdevice** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f43c1-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="f43c1-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="f43c1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f43c1-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f43c1-112">Methods</span></span>

<span data-ttu-id="f43c1-113">Die **iwmdrmdevice** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f43c1-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="f43c1-114">Methode</span><span class="sxs-lookup"><span data-stu-id="f43c1-114">Method</span></span>                                                                  | <span data-ttu-id="f43c1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f43c1-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f43c1-116">**Cleandatastore**</span><span class="sxs-lookup"><span data-stu-id="f43c1-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="f43c1-117">Startet die Bereinigung des DRM-Datenspeicher auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f43c1-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="f43c1-118">**Getde vicecertificate**</span><span class="sxs-lookup"><span data-stu-id="f43c1-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="f43c1-119">Ruft das Gerätezertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="f43c1-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="f43c1-120">**Getmeterchallenge**</span><span class="sxs-lookup"><span data-stu-id="f43c1-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="f43c1-121">Ruft die Messungs Herausforderung ab.</span><span class="sxs-lookup"><span data-stu-id="f43c1-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="f43c1-122">**Getsecureclock**</span><span class="sxs-lookup"><span data-stu-id="f43c1-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="f43c1-123">Ruft die sichere Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="f43c1-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="f43c1-124">**Getsecureclockchallenge**</span><span class="sxs-lookup"><span data-stu-id="f43c1-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="f43c1-125">Ruft die Anforderung der sicheren Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="f43c1-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="f43c1-126">**Getsynclist**</span><span class="sxs-lookup"><span data-stu-id="f43c1-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="f43c1-127">Ruft die Lizenz Synchronisierungs Liste ab.</span><span class="sxs-lookup"><span data-stu-id="f43c1-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="f43c1-128">**Iswmdrmdevice**</span><span class="sxs-lookup"><span data-stu-id="f43c1-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="f43c1-129">Bestimmt, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f43c1-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="f43c1-130">**SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="f43c1-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="f43c1-131">Legt die Lizenz Antwort fest.</span><span class="sxs-lookup"><span data-stu-id="f43c1-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="f43c1-132">**Setmeterresponse**</span><span class="sxs-lookup"><span data-stu-id="f43c1-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="f43c1-133">Legt die Messungs Antwort fest.</span><span class="sxs-lookup"><span data-stu-id="f43c1-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="f43c1-134">**Setsecureclockresponse**</span><span class="sxs-lookup"><span data-stu-id="f43c1-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="f43c1-135">Legt die Antwort auf die sichere Uhr fest.</span><span class="sxs-lookup"><span data-stu-id="f43c1-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="f43c1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f43c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f43c1-137">**Schnittstellen für Dienstanbieter**</span><span class="sxs-lookup"><span data-stu-id="f43c1-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

