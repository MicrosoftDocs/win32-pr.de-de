---
description: Die iwindowsdriverupdateentry-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: a0ff6ec2-13fe-4c0c-b375-9df55e1c1bb4
title: Iwindowsdriverupdateentry-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae63775bd7b13c67b4ec96c70107069730f828d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129608"
---
# <a name="iwindowsdriverupdateentry-properties"></a><span data-ttu-id="f07ad-103">Iwindowsdriverupdateentry-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f07ad-103">IWindowsDriverUpdateEntry Properties</span></span>

<span data-ttu-id="f07ad-104">Die [**iwindowsdriverupdateentry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f07ad-104">The [**IWindowsDriverUpdateEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdateentry) interface defines the following properties.</span></span>



| <span data-ttu-id="f07ad-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f07ad-105">Property</span></span>                                                                     | <span data-ttu-id="f07ad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f07ad-106">Description</span></span>                                                                                                          |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f07ad-107">**Deviceproblemnumber**</span><span class="sxs-lookup"><span data-stu-id="f07ad-107">**DeviceProblemNumber**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_deviceproblemnumber) | <span data-ttu-id="f07ad-108">Ruft die Problem Nummer des Geräts ab, das mit dem Windows-Treiberupdate übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f07ad-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                                    |
| [<span data-ttu-id="f07ad-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="f07ad-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_devicestatus)               | <span data-ttu-id="f07ad-110">Ruft den Status des Geräts ab, das mit dem Windows-Treiberupdate übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="f07ad-110">Gets the status of the device that matches for the Windows driver update.</span></span>                                            |
| [<span data-ttu-id="f07ad-111">**Driverclass**</span><span class="sxs-lookup"><span data-stu-id="f07ad-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverclass)                 | <span data-ttu-id="f07ad-112">Ruft die Klasse des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="f07ad-112">Gets the class of the Windows driver update.</span></span>                                                                         |
| [<span data-ttu-id="f07ad-113">**Driverhardwareid**</span><span class="sxs-lookup"><span data-stu-id="f07ad-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverhardwareid)       | <span data-ttu-id="f07ad-114">Ruft die Hardware oder den kompatiblen Bezeichner ab, der vom Windows-Treiberupdate abgeglichen werden muss, damit Sie installiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f07ad-114">Gets the hardware or the compatible identifier that the Windows driver update must match in order to be installable.</span></span> |
| [<span data-ttu-id="f07ad-115">**Driverhersteller**</span><span class="sxs-lookup"><span data-stu-id="f07ad-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermanufacturer)   | <span data-ttu-id="f07ad-116">Ruft den sprach invarianten Namen des Herstellers des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="f07ad-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                                   |
| [<span data-ttu-id="f07ad-117">**Drivermodel**</span><span class="sxs-lookup"><span data-stu-id="f07ad-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_drivermodel)                 | <span data-ttu-id="f07ad-118">Ruft den sprach invarianten Modellnamen des Geräts ab, für das das Windows-Treiberupdate vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f07ad-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span>                |
| [<span data-ttu-id="f07ad-119">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="f07ad-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driverprovider)           | <span data-ttu-id="f07ad-120">Ruft den sprach invarianten Namen des Anbieters des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="f07ad-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                                       |
| [<span data-ttu-id="f07ad-121">**Driverdatum**</span><span class="sxs-lookup"><span data-stu-id="f07ad-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdateentry-get_driververdate)             | <span data-ttu-id="f07ad-122">Ruft das Treiber Versions Datum des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="f07ad-122">Gets the driver version date of the Windows driver update.</span></span>                                                           |



 

 

 



