---
title: MDM-Registrierungsfunktionen
description: Die folgenden Funktionen werden von der MDM-Registrierung verwendet.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316610"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="234b7-103">MDM-Registrierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="234b7-103">MDM Registration Functions</span></span>

<span data-ttu-id="234b7-104">Die folgenden Funktionen werden von der MDM-Registrierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="234b7-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="234b7-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="234b7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="234b7-106">**Discovermanagementservice**</span><span class="sxs-lookup"><span data-stu-id="234b7-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="234b7-107">Ermittelt den MDM-Dienst.</span><span class="sxs-lookup"><span data-stu-id="234b7-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-108">**Discovermanagementserviceex**</span><span class="sxs-lookup"><span data-stu-id="234b7-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="234b7-109">Ermittelt den MDM-Dienst mithilfe eines Kandidaten Servers.</span><span class="sxs-lookup"><span data-stu-id="234b7-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-110">**Getdeviceregistrationinfo**</span><span class="sxs-lookup"><span data-stu-id="234b7-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="234b7-111">Ruft die Geräte Registrierungsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="234b7-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-112">**Getmanagementapphyperlink**</span><span class="sxs-lookup"><span data-stu-id="234b7-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="234b7-113">Ruft den dem MDM-Dienst zugeordneten Verwaltungs-App-Hyperlink ab.</span><span class="sxs-lookup"><span data-stu-id="234b7-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-114">**Isdeviceregisteredwithmanagement**</span><span class="sxs-lookup"><span data-stu-id="234b7-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="234b7-115">Hiermit wird überprüft, ob das Gerät bei einem MDM-Dienst registriert ist.</span><span class="sxs-lookup"><span data-stu-id="234b7-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-116">**Ismanagementregistrationallowed**</span><span class="sxs-lookup"><span data-stu-id="234b7-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="234b7-117">Überprüft, ob die MDM-Registrierung durch die lokale Richtlinie zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="234b7-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-118">**Registerdevicewithmanagement**</span><span class="sxs-lookup"><span data-stu-id="234b7-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="234b7-119">Registriert ein Gerät bei einem MDM-Dienst, wobei das Registrierungs [ \[ Protokoll MS-MDE \] : Mobile Geräte](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="234b7-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-120">**Registerdevicewithmanagementusingaadanmeldeinformationen**</span><span class="sxs-lookup"><span data-stu-id="234b7-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="234b7-121">Registriert ein Gerät bei einem MDM-Dienst unter Verwendung von Azure Active Directory Anmelde Informationen (AAD).</span><span class="sxs-lookup"><span data-stu-id="234b7-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-122">**Setmanagedexternally**</span><span class="sxs-lookup"><span data-stu-id="234b7-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="234b7-123">Gibt dem MDM-Agent an, dass das Gerät extern verwaltet wird und nicht bei einem MDM-Dienst registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="234b7-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="234b7-124">**Unregisterdevicewithmanagement**</span><span class="sxs-lookup"><span data-stu-id="234b7-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="234b7-125">Hebt die Registrierung eines Geräts beim MDM-Dienst auf.</span><span class="sxs-lookup"><span data-stu-id="234b7-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 