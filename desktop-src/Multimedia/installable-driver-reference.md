---
title: Installerbarer Treiber Verweis
description: Installerbarer Treiber Verweis
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows Multimedia, installierbare Treiber Referenz
- Multimedia, installierbare Treiber Referenz
- installierbare Treiber, Referenz
- Referenz zum installierbaren Treiber, Informationen zu
- Referenz zu installierbaren Treibern, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858180"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="0f3bd-108">Installerbarer Treiber Verweis</span><span class="sxs-lookup"><span data-stu-id="0f3bd-108">Installable Driver Reference</span></span>

<span data-ttu-id="0f3bd-109">Die Funktionen und Nachrichten, die installierbaren Treibern zugeordnet sind, werden wie folgt gruppiert.</span><span class="sxs-lookup"><span data-stu-id="0f3bd-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="0f3bd-110">Laden und Entladen von Treibern</span><span class="sxs-lookup"><span data-stu-id="0f3bd-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="0f3bd-111">Getdrivermodulehandle</span><span class="sxs-lookup"><span data-stu-id="0f3bd-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="0f3bd-112">Opendriver</span><span class="sxs-lookup"><span data-stu-id="0f3bd-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="0f3bd-113">Senddrivermessage</span><span class="sxs-lookup"><span data-stu-id="0f3bd-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="0f3bd-114">Closedriver</span><span class="sxs-lookup"><span data-stu-id="0f3bd-114">CloseDriver</span></span>

-   [<span data-ttu-id="0f3bd-115">**DRV \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="0f3bd-116">**DRV \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="0f3bd-117">**DRV \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="0f3bd-118">**DRV \_ Free**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="0f3bd-119">**DRV- \_ Auslastung**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="0f3bd-120">**DRV \_ geöffnet**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="0f3bd-121">Konfigurieren eines Treibers</span><span class="sxs-lookup"><span data-stu-id="0f3bd-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="0f3bd-122">**DRV \_ Konfigurieren**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="0f3bd-123">**DRV \_ queryconfigure**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="0f3bd-124">**Drvconfiginfo**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="0f3bd-125">Installieren eines Treibers</span><span class="sxs-lookup"><span data-stu-id="0f3bd-125">Installing a Driver</span></span>

-   [<span data-ttu-id="0f3bd-126">**DRV- \_ Installation**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="0f3bd-127">**DRV \_ Entfernen**</span><span class="sxs-lookup"><span data-stu-id="0f3bd-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="0f3bd-128">Treiberfunktionen</span><span class="sxs-lookup"><span data-stu-id="0f3bd-128">Driver Functions</span></span>

-   [<span data-ttu-id="0f3bd-129">Defdriverproc</span><span class="sxs-lookup"><span data-stu-id="0f3bd-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="0f3bd-130">Drivercallback</span><span class="sxs-lookup"><span data-stu-id="0f3bd-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="0f3bd-131">Driverproc</span><span class="sxs-lookup"><span data-stu-id="0f3bd-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="0f3bd-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f3bd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f3bd-133">Installierbare Treiber</span><span class="sxs-lookup"><span data-stu-id="0f3bd-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 