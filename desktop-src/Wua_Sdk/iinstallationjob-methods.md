---
description: Die iinstallationjob-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 4990ef7c-b6cd-46fc-9e7d-8d1d78edc9f2
title: Iinstallationjob-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0c1a5850f3d71ad1a6a51046fe890ea9bc7426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129652"
---
# <a name="iinstallationjob-methods"></a><span data-ttu-id="1bf80-103">Iinstallationjob-Methoden</span><span class="sxs-lookup"><span data-stu-id="1bf80-103">IInstallationJob Methods</span></span>

<span data-ttu-id="1bf80-104">Die [**iinstallationjob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="1bf80-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following methods.</span></span>



| <span data-ttu-id="1bf80-105">Methode</span><span class="sxs-lookup"><span data-stu-id="1bf80-105">Method</span></span>                                                | <span data-ttu-id="1bf80-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1bf80-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bf80-107">**Bereinigung**</span><span class="sxs-lookup"><span data-stu-id="1bf80-107">**CleanUp**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)           | <span data-ttu-id="1bf80-108">Wartet, bis ein asynchroner Vorgang abgeschlossen ist, und gibt dann alle Rückrufe frei.</span><span class="sxs-lookup"><span data-stu-id="1bf80-108">Waits for an asynchronous operation to be completed and then releases all the callbacks.</span></span>                                                              |
| [<span data-ttu-id="1bf80-109">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="1bf80-109">**GetProgress**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-getprogress)   | <span data-ttu-id="1bf80-110">Gibt eine [**iinstallationprogress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) -Schnittstelle zurück, die den aktuellen Status einer Installation oder der Uninstallation beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1bf80-110">Returns an [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface that describes the current progress of an installation or uninstallation.</span></span> |
| [<span data-ttu-id="1bf80-111">**Requestabort**</span><span class="sxs-lookup"><span data-stu-id="1bf80-111">**RequestAbort**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-requestabort) | <span data-ttu-id="1bf80-112">Stellt eine Anforderung zum Abbrechen der Installation oder der Installation von bereit.</span><span class="sxs-lookup"><span data-stu-id="1bf80-112">Makes a request to cancel the installation or uninstallation.</span></span>                                                                                         |



 

 

 



