---
description: Abbildverwaltung für die Bereitstellung (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Abbildverwaltung für die Bereitstellung (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088488"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="01ffe-103">Abbildverwaltung für die Bereitstellung (DISM)</span><span class="sxs-lookup"><span data-stu-id="01ffe-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="01ffe-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="01ffe-104">Affected Platforms</span></span>

<span data-ttu-id="01ffe-105">**Clients** : Windows Vista SP1 und höher \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="01ffe-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="01ffe-106">**Server** : Windows Server 2008 RTM und höher \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="01ffe-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="01ffe-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01ffe-107">Description</span></span>

<span data-ttu-id="01ffe-108">Das dism-Tool (Abbildverwaltung für die Bereitstellung) ersetzt die Tools pkgmgr, PEImg und IntlConfg, die in Windows 7 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01ffe-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="01ffe-109">DISM bietet ein einzelnes zentralisiertes Tool, mit dem alle Funktionen dieser drei Tools effizienter und standardisierter ausgeführt werden können, sodass viele der frustrierten Benutzer dieser Tools nicht mehr auftreten können.</span><span class="sxs-lookup"><span data-stu-id="01ffe-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="01ffe-110">DISM enthält einen Shim für Windows Vista SP1 und höher sowie für Windows Server 2008 RTM und höher, der pkgmgr-Aufrufe von Legacyanwendungen, die unter Windows 7 ausgeführt werden, an DISM umleitet.</span><span class="sxs-lookup"><span data-stu-id="01ffe-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="01ffe-111">Wenn die Anwendung unter einem der unterstützten Betriebssysteme ausgeführt wird, leitet der Shim den Aufruf an pkgmgr weiter.</span><span class="sxs-lookup"><span data-stu-id="01ffe-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="01ffe-112">Für Legacyanwendungen, die PEImg oder IntlConfg aufrufen, sind keine Shims vorhanden.</span><span class="sxs-lookup"><span data-stu-id="01ffe-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="01ffe-113">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="01ffe-113">Usage</span></span>

<span data-ttu-id="01ffe-114">DISM ist für pkgmgr-Endbenutzer auf allen unterstützten Plattformen transparent.</span><span class="sxs-lookup"><span data-stu-id="01ffe-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="01ffe-115">Wenn eine Anwendung jedoch entweder PEImg oder IntlConfg von Windows 7 aufruft, schlägt der Aufruf fehl.</span><span class="sxs-lookup"><span data-stu-id="01ffe-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="01ffe-116">Aktualisieren Sie alle Skripts, die pkgmgr, PEImg oder IntlConfg aufrufen, um stattdessen DISM aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="01ffe-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="01ffe-117">Es ist wichtig, die Aktualisierung von pkgmgr-Skripts in diesen Aufwand einzubeziehen, da der Shim, der Abwärtskompatibilität für pkgmgr bereitstellt, in zukünftigen Versionen der Windows-Betriebssysteme entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="01ffe-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="01ffe-118">Überprüfen Sie, ob Aufrufe von DISM alle Aufrufe von pkgmgr, PEImg und IntlConfg ersetzt haben und dass der Vorgang erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01ffe-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01ffe-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01ffe-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="01ffe-120">[Abbildverwaltung für die Bereitstellung (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="01ffe-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
