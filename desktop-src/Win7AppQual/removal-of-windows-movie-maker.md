---
description: Entfernen von Windows-Movie Maker
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Entfernen von Windows-Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36df5ffe4498e05de9fcbbaadf49f8fc32c91b0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116268"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="b34fb-103">Entfernen von Windows-Movie Maker</span><span class="sxs-lookup"><span data-stu-id="b34fb-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="b34fb-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="b34fb-104">Affected Platforms</span></span>

<span data-ttu-id="b34fb-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="b34fb-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b34fb-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b34fb-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="b34fb-107">Auswirkungen auf Features</span><span class="sxs-lookup"><span data-stu-id="b34fb-107">Feature Impact</span></span>

 <span data-ttu-id="b34fb-108">**Schweregrad –** Hoch</span><span class="sxs-lookup"><span data-stu-id="b34fb-108">**Severity** - High</span></span>  
<span data-ttu-id="b34fb-109">**Häufigkeit** – Mittel</span><span class="sxs-lookup"><span data-stu-id="b34fb-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="b34fb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b34fb-110">Description</span></span>

<span data-ttu-id="b34fb-111">Microsoft ist veraltet und entfernt das Hilfsprogramm Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="b34fb-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="b34fb-112">Dies schließt Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="b34fb-112">This includes:</span></span>

-   <span data-ttu-id="b34fb-113">Alle Einstiegspunkte zu Windows Movie Maker (z. B. Startmenü, Start > Ausführen)</span><span class="sxs-lookup"><span data-stu-id="b34fb-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="b34fb-114">Alle Binärdateien, die von Windows Movie Maker verwendet wurden (alles, was sich in %ProgramFiles% \\ Movie Maker befand)</span><span class="sxs-lookup"><span data-stu-id="b34fb-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="b34fb-115">Die Movie Maker Projektdateien eines Benutzers verbleiben jedoch auf dem System und sind für andere Anwendungen zugänglich, die dieses Dateiformat unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b34fb-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b34fb-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="b34fb-116">Manifestation</span></span>

<span data-ttu-id="b34fb-117">Das Entfernen von Windows Movie Maker führt zu folgendem Ergebnis:</span><span class="sxs-lookup"><span data-stu-id="b34fb-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="b34fb-118">Jeder Versuch, Windows Movie Maker mit den Befehlszeilenargumenten zu starten, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="b34fb-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="b34fb-119">Alle Plug-Ins, die installiert wurden, um neue Transformationen und Animationen zu aktivieren, bleiben installiert, werden jedoch nicht für den Endbenutzer verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="b34fb-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="b34fb-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="b34fb-120">Solution</span></span>

<span data-ttu-id="b34fb-121">Um in Zukunft über eine solche Funktionalität zu verfügen, muss ein Benutzer eine ähnliche Anwendung von Microsoft oder einem anderen Softwareanbieter installieren.</span><span class="sxs-lookup"><span data-stu-id="b34fb-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



