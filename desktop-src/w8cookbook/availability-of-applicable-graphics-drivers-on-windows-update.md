---
title: Verfügbarkeit der anwendbaren Grafiktreiber auf Windows Update
description: Die Verfügbarkeit dieser Treiber auf Windows Update (Wu) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird.
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341442"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="5bab1-103">Verfügbarkeit der anwendbaren Grafiktreiber auf Windows Update</span><span class="sxs-lookup"><span data-stu-id="5bab1-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="5bab1-104">Die Verfügbarkeit dieser Treiber auf Windows Update (Wu) bestimmt, ob einem Benutzer automatisch ein Upgrade von Windows 7, Windows 8 oder Windows 8.1 auf Windows 10 angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="5bab1-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="5bab1-105">Wenn in den Hardware Scans festgestellt wurde, dass auf Windows Update für den Grafikadapter des PCs kein Grafiktreiber verfügbar war, wurde den Benutzern das aktualisierte Windows 10-Betriebssystem nicht angeboten.</span><span class="sxs-lookup"><span data-stu-id="5bab1-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="5bab1-106">Allerdings können Benutzer Windows 10 weiterhin durch andere Quellen abrufen und das Upgrade manuell durchführen.</span><span class="sxs-lookup"><span data-stu-id="5bab1-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="5bab1-107">Einige Benutzer waren nicht sicher, warum Ihnen das Upgrade nicht angeboten wurde, als andere Benutzer waren, obwohl der Upgrade Advisor erläuterte, dass kein Grafiktreiber für die Hardware verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="5bab1-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="5bab1-108">Außerdem haben einige Benutzer ein Upgrade erzwungen und dann festgestellt, dass Ihre Grafik Funktionalität und Leistung aufgrund des Mangels an Hardware Treibern aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="5bab1-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="5bab1-109">Gegenmaßnahmen</span><span class="sxs-lookup"><span data-stu-id="5bab1-109">Mitigations</span></span>

<span data-ttu-id="5bab1-110">Um dies zu vermeiden, können Benutzer einen älteren Treiber manuell installieren, d. h. von Windows 7, Windows 8 oder Windows 8.1, indem Sie die IHV-oder OEM-Website aufrufen und einen Treiber explizit herunterladen.</span><span class="sxs-lookup"><span data-stu-id="5bab1-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="5bab1-111">Dies muss nach dem Upgrade erfolgen, und es ist nicht garantiert, dass es funktioniert.</span><span class="sxs-lookup"><span data-stu-id="5bab1-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="5bab1-112">Es gibt keine unterstützte Lösung, wenn in Wu kein geeigneter Grafiktreiber verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5bab1-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="5bab1-113">Der Benutzer muss entscheiden, ob Folgendes erforderlich ist:</span><span class="sxs-lookup"><span data-stu-id="5bab1-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="5bab1-114">Auf dem vorherigen Betriebssystem verbleiben;</span><span class="sxs-lookup"><span data-stu-id="5bab1-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="5bab1-115">Akzeptieren Sie die Einschränkungen des Software Treibers, Microsoft Basic Display Adapter (msbda); noch</span><span class="sxs-lookup"><span data-stu-id="5bab1-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="5bab1-116">Erwerben Sie eine neue Grafikkarte, die über einen unterstützten Windows 10-Treiber verfügt.</span><span class="sxs-lookup"><span data-stu-id="5bab1-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="5bab1-117">Lösungen</span><span class="sxs-lookup"><span data-stu-id="5bab1-117">Solutions</span></span>

<span data-ttu-id="5bab1-118">Es ist wichtig, dass IHVs und OEMs Ihre Windows 10-Grafiktreiber für alle Hardware, die Sie unterstützen möchten, in Wu hochladen.</span><span class="sxs-lookup"><span data-stu-id="5bab1-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="5bab1-119">Beachten Sie, dass die Hardware, die das Ende der Live-(EOL) erreicht hat, möglicherweise keine Treiber auf Wu hat.</span><span class="sxs-lookup"><span data-stu-id="5bab1-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="5bab1-120">In diesem Fall ist keine Lösung vorhanden – der Benutzer muss eine der Optionen unter entschärfungen oben auswählen.</span><span class="sxs-lookup"><span data-stu-id="5bab1-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




