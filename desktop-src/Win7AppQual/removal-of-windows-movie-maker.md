---
description: .
ms.assetid: af55e570-0f24-4376-905a-3b879d5f3a1c
title: Entfernen von Windows Movie Maker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71a3336421ae2bde761aa1d4f238b5cd135ba64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362920"
---
# <a name="removal-of-windows-movie-maker"></a><span data-ttu-id="68f37-103">Entfernen von Windows Movie Maker</span><span class="sxs-lookup"><span data-stu-id="68f37-103">Removal of Windows Movie Maker</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="68f37-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="68f37-104">Affected Platforms</span></span>

<span data-ttu-id="68f37-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="68f37-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="68f37-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68f37-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="68f37-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="68f37-107">Feature Impact</span></span>

 <span data-ttu-id="68f37-108">**Schweregrad** -hoch</span><span class="sxs-lookup"><span data-stu-id="68f37-108">**Severity** - High</span></span>  
<span data-ttu-id="68f37-109">**Frequency** -Medium</span><span class="sxs-lookup"><span data-stu-id="68f37-109">**Frequency** - Medium</span></span>  


## <a name="description"></a><span data-ttu-id="68f37-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="68f37-110">Description</span></span>

<span data-ttu-id="68f37-111">Microsoft ist veraltet und entfernt das Hilfsprogramm Windows Movie Maker.</span><span class="sxs-lookup"><span data-stu-id="68f37-111">Microsoft is deprecating and removing the Windows Movie Maker utility.</span></span> <span data-ttu-id="68f37-112">Dies schließt Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="68f37-112">This includes:</span></span>

-   <span data-ttu-id="68f37-113">Alle Einstiegspunkte für Windows Movie Maker (z. b. Startmenü, Start > ausführen)</span><span class="sxs-lookup"><span data-stu-id="68f37-113">All entry points to Windows Movie Maker (for example, Start Menu, Start > Run)</span></span>
-   <span data-ttu-id="68f37-114">Alle Binärdateien, die von Windows Movie Maker verwendet wurden (alles in% Program Files% \\ Movie Maker)</span><span class="sxs-lookup"><span data-stu-id="68f37-114">All binaries that were used by Windows Movie Maker (everything that was in %ProgramFiles%\\Movie Maker)</span></span>

<span data-ttu-id="68f37-115">Die Movie Maker-Projektdateien eines Benutzers verbleiben jedoch auf dem System und sind für andere Anwendungen zugänglich, die dieses Dateiformat unterstützen.</span><span class="sxs-lookup"><span data-stu-id="68f37-115">However, a user's Movie Maker project files will remain on the system and be accessible to other applications that support this file format.</span></span>

## <a name="manifestation"></a><span data-ttu-id="68f37-116">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="68f37-116">Manifestation</span></span>

<span data-ttu-id="68f37-117">Das Entfernen von Windows Movie Maker führt zu folgendem:</span><span class="sxs-lookup"><span data-stu-id="68f37-117">Remove of Windows Movie Maker results in the following:</span></span>

-   <span data-ttu-id="68f37-118">Bei jedem Versuch, Windows Movie Maker mit den Befehlszeilen Argumenten zu starten, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="68f37-118">Any attempt to launch Windows Movie Maker with its command line arguments will fail</span></span>
-   <span data-ttu-id="68f37-119">Alle Plug-ins, die zum Aktivieren neuer Transformationen und Animationen installiert wurden, bleiben installiert, werden aber nicht für den Endbenutzer verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="68f37-119">Any plug-ins that were installed to enable new transforms and animations will remain installed but will not be exposed to the end user</span></span>

## <a name="solution"></a><span data-ttu-id="68f37-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="68f37-120">Solution</span></span>

<span data-ttu-id="68f37-121">Um solche Funktionen in Zukunft zu haben, muss ein Benutzer eine ähnliche Anwendung von Microsoft oder einem anderen Softwareanbieter installieren.</span><span class="sxs-lookup"><span data-stu-id="68f37-121">To have such functionality in the future, a user will need to install a similar application from Microsoft or another software provider.</span></span>

 

 



