---
title: MCI-Gerätefunktionen
description: MCI-Gerätefunktionen
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Mciwndcanconfig-Makro
- Mciwndcaneject-Makro
- Mciwndcanplay-Makro
- Mciwndcanrecord-Makro
- Mciwndcansave-Makro
- Mciwndcanwindow-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037513"
---
# <a name="mci-device-capabilities"></a><span data-ttu-id="11df8-109">MCI-Gerätefunktionen</span><span class="sxs-lookup"><span data-stu-id="11df8-109">MCI Device Capabilities</span></span>

<span data-ttu-id="11df8-110">Mciwnd umfasst die folgenden Makros, damit Sie MCI-Geräte auf ihre Funktionen Abfragen können.</span><span class="sxs-lookup"><span data-stu-id="11df8-110">MCIWnd includes the following macros to let you query MCI devices for their capabilities.</span></span>



| <span data-ttu-id="11df8-111">Makro</span><span class="sxs-lookup"><span data-stu-id="11df8-111">Macro</span></span>                                      | <span data-ttu-id="11df8-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11df8-112">Description</span></span>                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11df8-113">**Mciwndcanconfig**</span><span class="sxs-lookup"><span data-stu-id="11df8-113">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | <span data-ttu-id="11df8-114">Bestimmt, ob ein Gerät über ein Konfigurations Dialogfeld verfügt, das mehrere Konfigurationen unterstützt, z. b. das MCIAVI-Gerät.</span><span class="sxs-lookup"><span data-stu-id="11df8-114">Determines whether a device has a configuration dialog box to support multiple configurations, such as the MCIAVI device.</span></span>                   |
| [<span data-ttu-id="11df8-115">**Mciwndcaneject**</span><span class="sxs-lookup"><span data-stu-id="11df8-115">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | <span data-ttu-id="11df8-116">Bestimmt, ob ein Gerät über eine softwaregesteuerte Auswerfen-Funktion verfügt.</span><span class="sxs-lookup"><span data-stu-id="11df8-116">Determines whether a device has a software-controlled eject function.</span></span>                                                                       |
| [<span data-ttu-id="11df8-117">**Mciwndcanplay**</span><span class="sxs-lookup"><span data-stu-id="11df8-117">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | <span data-ttu-id="11df8-118">Bestimmt, ob ein Gerät den vorhandenen Inhalt wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="11df8-118">Determines whether a device can play the existing content.</span></span>                                                                                  |
| [<span data-ttu-id="11df8-119">**Mciwndcanrecord**</span><span class="sxs-lookup"><span data-stu-id="11df8-119">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | <span data-ttu-id="11df8-120">Bestimmt, ob ein Gerät aufzeichnen kann.</span><span class="sxs-lookup"><span data-stu-id="11df8-120">Determines whether a device can record.</span></span>                                                                                                     |
| [<span data-ttu-id="11df8-121">**Mciwndcansave**</span><span class="sxs-lookup"><span data-stu-id="11df8-121">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | <span data-ttu-id="11df8-122">Bestimmt, ob ein Gerät Daten speichern kann.</span><span class="sxs-lookup"><span data-stu-id="11df8-122">Determines whether a device can store data.</span></span>                                                                                                 |
| [<span data-ttu-id="11df8-123">**Mciwndcanwindow**</span><span class="sxs-lookup"><span data-stu-id="11df8-123">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | <span data-ttu-id="11df8-124">Bestimmt, ob ein Gerät MCI-Fenster Befehle unterstützt (z. b. [**Fenster**](window.md), [**Put**](put.md) und [**Where**](where.md)).</span><span class="sxs-lookup"><span data-stu-id="11df8-124">Determines whether a device supports MCI window commands (such as [**window**](window.md), [**put**](put.md) and [**where**](where.md)).</span></span> |



 

<span data-ttu-id="11df8-125">Diese Makros geben " **true** " zurück, wenn das Gerät die bestimmte Funktion unterstützt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="11df8-125">These macros return **TRUE** if the device supports the specific capability, or **FALSE** otherwise.</span></span>

 

 




