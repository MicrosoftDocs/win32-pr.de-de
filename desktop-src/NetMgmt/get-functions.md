---
title: Get-Funktionen
description: Die Get-Funktionen der Netzwerkverwaltung rufen Informationen zu einer Domäne ab. Sie können diese Funktionen auch aufrufen, um Informationen zu lokalen, globalen, Arbeitsstations-und Server Benutzerkonten abzurufen.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515854"
---
# <a name="get-functions"></a><span data-ttu-id="e5dad-104">Get-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e5dad-104">Get Functions</span></span>

<span data-ttu-id="e5dad-105">Die Get-Funktionen der Netzwerkverwaltung rufen Informationen zu einer Domäne ab.</span><span class="sxs-lookup"><span data-stu-id="e5dad-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="e5dad-106">Sie können diese Funktionen auch aufrufen, um Informationen zu lokalen, globalen, Arbeitsstations-und Server Benutzerkonten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e5dad-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="e5dad-107">Die Get-Funktionen der Netzwerkverwaltung sind nachfolgend aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5dad-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="e5dad-108">Funktion</span><span class="sxs-lookup"><span data-stu-id="e5dad-108">Function</span></span>                                                               | <span data-ttu-id="e5dad-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5dad-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5dad-110">**Netgetanydcname**</span><span class="sxs-lookup"><span data-stu-id="e5dad-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="e5dad-111">Gibt den Namen eines beliebigen Domänen Controllers für eine Domäne zurück, die direkt von einem angegebenen Server als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="e5dad-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="e5dad-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="e5dad-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="e5dad-113">Gibt den Namen des primären Domänen Controllers (PDC) für die angegebene Domäne zurück.</span><span class="sxs-lookup"><span data-stu-id="e5dad-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="e5dad-114">**Netgetdisplayinformationindex**</span><span class="sxs-lookup"><span data-stu-id="e5dad-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="e5dad-115">Gibt den Index des ersten Anzeige Informations Eintrags zurück, dessen Name mit einer angegebenen Zeichenfolge beginnt oder alphabetisch auf die Zeichenfolge folgt.</span><span class="sxs-lookup"><span data-stu-id="e5dad-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="e5dad-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="e5dad-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="e5dad-117">Gibt Informationen zu Benutzern, Computern oder globalen Gruppenkonten zurück.</span><span class="sxs-lookup"><span data-stu-id="e5dad-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="e5dad-118">Die von der Funktion [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) zurückgegebenen Informationen sind auf folgenden Ebenen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="e5dad-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="e5dad-119">**Netzwerk \_ Anzeige \_ Gruppe**</span><span class="sxs-lookup"><span data-stu-id="e5dad-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="e5dad-120">**Netzwerk \_ Anzeige \_ Computer**</span><span class="sxs-lookup"><span data-stu-id="e5dad-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="e5dad-121">**Benutzer für Netzwerk \_ Anzeige \_**</span><span class="sxs-lookup"><span data-stu-id="e5dad-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




