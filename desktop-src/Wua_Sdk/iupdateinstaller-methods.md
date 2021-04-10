---
description: Die iupdaterstaller-Schnittstelle definiert die folgenden Methoden.
ms.assetid: 94e2516e-19e1-4e9c-9b9a-fa9a68222b08
title: Iupdateingestaller-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1422c149d2de287c4863078f4012e526212b64ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214729"
---
# <a name="iupdateinstaller-methods"></a><span data-ttu-id="081fd-103">Iupdateingestaller-Methoden</span><span class="sxs-lookup"><span data-stu-id="081fd-103">IUpdateInstaller Methods</span></span>

<span data-ttu-id="081fd-104">Die [**iupdaterstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="081fd-104">The [**IUpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller) interface defines the following methods.</span></span>



| <span data-ttu-id="081fd-105">Methode</span><span class="sxs-lookup"><span data-stu-id="081fd-105">Method</span></span>                                                    | <span data-ttu-id="081fd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="081fd-106">Description</span></span>                                                                          |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="081fd-107">**Begininstall**</span><span class="sxs-lookup"><span data-stu-id="081fd-107">**BeginInstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)     | <span data-ttu-id="081fd-108">Startet eine asynchrone Installation der Updates.</span><span class="sxs-lookup"><span data-stu-id="081fd-108">Starts an asynchronous installation of the updates.</span></span>                                  |
| [<span data-ttu-id="081fd-109">**Beginuninstall**</span><span class="sxs-lookup"><span data-stu-id="081fd-109">**BeginUninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) | <span data-ttu-id="081fd-110">Startet eine asynchrone Installation der Updates.</span><span class="sxs-lookup"><span data-stu-id="081fd-110">Starts an asynchronous uninstallation of the updates.</span></span>                                |
| [<span data-ttu-id="081fd-111">**Umdinstall**</span><span class="sxs-lookup"><span data-stu-id="081fd-111">**EndInstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall)         | <span data-ttu-id="081fd-112">Schließt eine asynchrone Installation der Updates ab.</span><span class="sxs-lookup"><span data-stu-id="081fd-112">Completes an asynchronous installation of the updates.</span></span>                               |
| [<span data-ttu-id="081fd-113">**Enduninstall**</span><span class="sxs-lookup"><span data-stu-id="081fd-113">**EndUninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall)     | <span data-ttu-id="081fd-114">Schließt eine asynchrone Installation der Updates ab.</span><span class="sxs-lookup"><span data-stu-id="081fd-114">Completes an asynchronous uninstallation of the updates.</span></span>                             |
| [<span data-ttu-id="081fd-115">**Installieren**</span><span class="sxs-lookup"><span data-stu-id="081fd-115">**Install**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-install)               | <span data-ttu-id="081fd-116">Startet eine synchrone Installation der Updates.</span><span class="sxs-lookup"><span data-stu-id="081fd-116">Starts a synchronous installation of the updates.</span></span>                                    |
| [<span data-ttu-id="081fd-117">**Runwizard**</span><span class="sxs-lookup"><span data-stu-id="081fd-117">**RunWizard**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-runwizard)           | <span data-ttu-id="081fd-118">Hiermit wird ein Assistent gestartet, der den lokalen Benutzer durch die Schritte zum Installieren der Updates führt.</span><span class="sxs-lookup"><span data-stu-id="081fd-118">Starts a wizard that guides the local user through the steps to install the updates.</span></span> |
| [<span data-ttu-id="081fd-119">**Deinstallieren**</span><span class="sxs-lookup"><span data-stu-id="081fd-119">**Uninstall**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-uninstall)           | <span data-ttu-id="081fd-120">Startet eine synchrone Neuinstallation der Updates.</span><span class="sxs-lookup"><span data-stu-id="081fd-120">Starts a synchronous uninstallation of the updates.</span></span>                                  |



 

 

 



