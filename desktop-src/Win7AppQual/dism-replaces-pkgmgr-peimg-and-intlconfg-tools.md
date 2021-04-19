---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Abbildverwaltung für die Bereitstellung (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369856"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="c122b-103">Abbildverwaltung für die Bereitstellung (DISM)</span><span class="sxs-lookup"><span data-stu-id="c122b-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="c122b-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="c122b-104">Affected Platforms</span></span>

<span data-ttu-id="c122b-105">**Clients** -Windows Vista SP1 und höher \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="c122b-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="c122b-106">**Server** -Windows Server 2008 RTM und höher \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c122b-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="c122b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c122b-107">Description</span></span>

<span data-ttu-id="c122b-108">Das Tool zur Abbild Verwaltung für die Bereitstellung (Mage) ersetzt die Tools pkgmgr, peimg und intlconfg, die in Windows 7 eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c122b-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="c122b-109">Das-Verfahren bietet ein zentrales Tool für die Durchführung aller Funktionen dieser drei Tools auf effizientere und standardisierte Weise. Dadurch entfällt die Quelle vieler der Frustrationen, die von den aktuellen Benutzern dieser Tools genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="c122b-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="c122b-110">Der-Wert enthält einen Shim für Windows Vista SP1 und höher sowie für Windows Server 2008 RTM und höher, der pkgmgr-Aufrufe von älteren Anwendungen unter Windows 7 an den-Dienst umleitet.</span><span class="sxs-lookup"><span data-stu-id="c122b-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="c122b-111">Wenn die Anwendung unter einem der unterstützten Betriebssysteme ausgeführt wird, leitet der Shim den pkgmgr-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="c122b-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="c122b-112">Für Legacy Anwendungen, die peimg oder intlconfg anrufen, sind keine Shims vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c122b-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="c122b-113">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c122b-113">Usage</span></span>

<span data-ttu-id="c122b-114">Das-Paradigma ist für pkgmgr-Endbenutzer auf allen unterstützten Plattformen transparent.</span><span class="sxs-lookup"><span data-stu-id="c122b-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="c122b-115">Wenn eine Anwendung jedoch entweder peimg oder intlconfg von Windows 7 aufruft, schlägt der Aufruf fehl.</span><span class="sxs-lookup"><span data-stu-id="c122b-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="c122b-116">Aktualisieren Sie alle Skripts, die pkgmgr, peimg oder intlconfg anrufen, um stattdessen die-Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c122b-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="c122b-117">Es ist wichtig, dass Sie die Aktualisierung von Pkgmgr-Skripts in diesen Vorgang einschließen, da das Shim, das Abwärtskompatibilität für pkgmgr bereitstellt, in zukünftigen Versionen der Windows-Betriebssysteme entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c122b-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="c122b-118">Stellen Sie sicher, dass Aufrufe der-Funktion alle Aufrufe von Pkgmgr, peimg und intlconfg ersetzt haben und der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c122b-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c122b-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c122b-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c122b-120">[Abbild Verwaltung für die Bereitstellung (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="c122b-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
