---
description: Die iupdateservicemanager-Schnittstelle definiert die folgenden Methoden.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Iupdateservicemanager-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525085"
---
# <a name="iupdateservicemanager-methods"></a><span data-ttu-id="c7b79-103">Iupdateservicemanager-Methoden</span><span class="sxs-lookup"><span data-stu-id="c7b79-103">IUpdateServiceManager Methods</span></span>

<span data-ttu-id="c7b79-104">Die [**iupdateservicemanager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) -Schnittstelle definiert die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="c7b79-104">The [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) interface defines the following methods.</span></span>



| <span data-ttu-id="c7b79-105">Methode</span><span class="sxs-lookup"><span data-stu-id="c7b79-105">Method</span></span>                                                                           | <span data-ttu-id="c7b79-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7b79-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7b79-107">**Addscanpackageservice**</span><span class="sxs-lookup"><span data-stu-id="c7b79-107">**AddScanPackageService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | <span data-ttu-id="c7b79-108">Registriert ein Überprüfungspaket als Dienst bei Windows Update-Agent (WUA) und gibt dann eine [**iupdateservice**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="c7b79-108">Registers a scan package as a service with Windows Update Agent (WUA) and then returns an [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) interface.</span></span>    |
| [<span data-ttu-id="c7b79-109">**AddService**</span><span class="sxs-lookup"><span data-stu-id="c7b79-109">**AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | <span data-ttu-id="c7b79-110">Registriert einen Dienst bei WUA.</span><span class="sxs-lookup"><span data-stu-id="c7b79-110">Registers a service with WUA.</span></span>                                                                                                                    |
| [<span data-ttu-id="c7b79-111">**Registerservicewithau**</span><span class="sxs-lookup"><span data-stu-id="c7b79-111">**RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | <span data-ttu-id="c7b79-112">Registriert einen Dienst bei automatische Updates.</span><span class="sxs-lookup"><span data-stu-id="c7b79-112">Registers a service with Automatic Updates.</span></span>                                                                                                      |
| [<span data-ttu-id="c7b79-113">**RemoveService**</span><span class="sxs-lookup"><span data-stu-id="c7b79-113">**RemoveService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | <span data-ttu-id="c7b79-114">Entfernt eine Dienst Registrierung aus WUA.</span><span class="sxs-lookup"><span data-stu-id="c7b79-114">Removes a service registration from WUA.</span></span>                                                                                                         |
| [<span data-ttu-id="c7b79-115">**SetOption**</span><span class="sxs-lookup"><span data-stu-id="c7b79-115">**SetOption**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | <span data-ttu-id="c7b79-116">Legt Optionen für das-Objekt fest, das die Dienst-ID angibt, und gibt an, ob beim Ändern der Registrierung von Automatische Updates eine Warnung angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7b79-116">Sets options for the object that specifies the service ID, and whether to display a warning when changing the registration of Automatic Updates.</span></span> |
| [<span data-ttu-id="c7b79-117">**Unregisterservicewithau**</span><span class="sxs-lookup"><span data-stu-id="c7b79-117">**UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | <span data-ttu-id="c7b79-118">Hebt die Registrierung eines Dienstanbieter bei automatische Updates auf.</span><span class="sxs-lookup"><span data-stu-id="c7b79-118">Unregisters a service with Automatic Updates.</span></span>                                                                                                    |



 

 

 



