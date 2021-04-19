---
description: Die iwindowsdriverupdate-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 2177c5e0-47db-44ae-a0ce-2544ff2d0855
title: Iwindowsdriverupdate-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291d7933cf3e73dee6f47edab3240c4ebd14f454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346967"
---
# <a name="iwindowsdriverupdate-properties"></a><span data-ttu-id="4b4cc-103">Iwindowsdriverupdate-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4b4cc-103">IWindowsDriverUpdate Properties</span></span>

<span data-ttu-id="4b4cc-104">Die [**iwindowsdriverupdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) -Schnittstelle definiert die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-104">The [**IWindowsDriverUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate) interface defines the following properties.</span></span>



| <span data-ttu-id="4b4cc-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4b4cc-105">Property</span></span>                                                                                                    | <span data-ttu-id="4b4cc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b4cc-106">Description</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4cc-107">[**Deviceproblemnumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)-[**Adresse**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span><span class="sxs-lookup"><span data-stu-id="4b4cc-107">[**DeviceProblemNumber**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_deviceproblemnumber)[**Address**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)</span></span> | <span data-ttu-id="4b4cc-108">Ruft die Problem Nummer des Geräts ab, das mit dem Windows-Treiberupdate übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-108">Gets the problem number of the device that matches for the Windows driver update.</span></span>                     |
| [<span data-ttu-id="4b4cc-109">**DeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-109">**DeviceStatus**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_devicestatus)                                                   | <span data-ttu-id="4b4cc-110">Ruft den Status des Geräts ab, das mit dem Windows-Treiberupdate übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-110">Gets the status of the device that matches for the Windows driver update.</span></span>                             |
| [<span data-ttu-id="4b4cc-111">**Driverclass**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-111">**DriverClass**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverclass)                                                     | <span data-ttu-id="4b4cc-112">Ruft die Klasse des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-112">Gets the class of the Windows driver update.</span></span>                                                          |
| [<span data-ttu-id="4b4cc-113">**Driverhardwareid**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-113">**DriverHardwareID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverhardwareid)                                           | <span data-ttu-id="4b4cc-114">Ruft die Hardware-ID oder die kompatible ID ab, mit der das Windows-Treiberupdate installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-114">Gets the hardware ID or compatible ID that the Windows driver update must match to be installable.</span></span>    |
| [<span data-ttu-id="4b4cc-115">**Driverhersteller**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-115">**DriverManufacturer**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermanufacturer)                                       | <span data-ttu-id="4b4cc-116">Ruft den sprach invarianten Namen des Herstellers des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-116">Gets the language-invariant name of the manufacturer of the Windows driver update.</span></span>                    |
| [<span data-ttu-id="4b4cc-117">**Drivermodel**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-117">**DriverModel**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_drivermodel)                                                     | <span data-ttu-id="4b4cc-118">Ruft den sprach invarianten Modellnamen des Geräts ab, für das das Windows-Treiberupdate vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-118">Gets the language-invariant model name of the device for which the Windows driver update is intended.</span></span> |
| [<span data-ttu-id="4b4cc-119">**Driverprovider**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-119">**DriverProvider**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driverprovider)                                               | <span data-ttu-id="4b4cc-120">Ruft den sprach invarianten Namen des Anbieters des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-120">Gets the language-invariant name of the provider of the Windows driver update.</span></span>                        |
| [<span data-ttu-id="4b4cc-121">**Driverdatum**</span><span class="sxs-lookup"><span data-stu-id="4b4cc-121">**DriverVerDate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate-get_driververdate)                                                 | <span data-ttu-id="4b4cc-122">Ruft das Treiber Versions Datum des Windows-Treiber Updates ab.</span><span class="sxs-lookup"><span data-stu-id="4b4cc-122">Gets the driver version date of the Windows driver update.</span></span>                                            |



 

 

 



