---
description: Leser sind Standardgeräte in einem Smartcardsystem. Sie werden über Treiber gesteuert und in das System über Plug & Play oder über die System Steuerungsgeräte-Elemente eingeführt und daraus entfernt.
ms.assetid: 694902b9-e43c-4558-8fab-baa853f9fc4d
title: Smartcardleser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6f4f5c4d1d487f136fb25052d44659f4b073bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350814"
---
# <a name="smart-card-readers"></a><span data-ttu-id="26029-104">Smartcardleser</span><span class="sxs-lookup"><span data-stu-id="26029-104">Smart Card Readers</span></span>

<span data-ttu-id="26029-105">Leser sind Standardgeräte in einem [*Smartcardsystem*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="26029-105">Readers are standard devices in a [*smart card*](../secgloss/s-gly.md) system.</span></span> <span data-ttu-id="26029-106">Sie werden über Treiber gesteuert und in das System über Plug & Play oder über die System Steuerungsgeräte-Elemente eingeführt und daraus entfernt.</span><span class="sxs-lookup"><span data-stu-id="26029-106">They are controlled through drivers, and are introduced to and removed from the system through Plug and Play or through the Control Panel Devices item.</span></span>

<span data-ttu-id="26029-107">Jeder Reader muss für die Verwendung durch das [*Smartcard-Subsystem*](../secgloss/s-gly.md)definiert werden.</span><span class="sxs-lookup"><span data-stu-id="26029-107">Each reader must be defined for use by the [*smart card subsystem*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="26029-108">Das Subsystem ist nicht verantwortlich für Leser, die ihm nicht explizit übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="26029-108">The subsystem is not responsible for any reader not specifically given to it.</span></span>

<span data-ttu-id="26029-109">Smartcardleser können in logische Gruppen unterteilt werden, die als Lesergruppen bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="26029-109">Smart card readers can be divided into logical groups called reader groups.</span></span> <span data-ttu-id="26029-110">Diese Gruppen können durch das-Subsystem definiert und von Administratoren und Benutzern definiert werden.</span><span class="sxs-lookup"><span data-stu-id="26029-110">These groups can be defined by the subsystem, as well as defined by administrators and users.</span></span> <span data-ttu-id="26029-111">Ein Reader kann mehreren Lesegruppen angehören.</span><span class="sxs-lookup"><span data-stu-id="26029-111">A reader can belong to more than one reader group</span></span>

<span data-ttu-id="26029-112">Das Smartcard-Subsystem definiert die folgenden Gruppen.</span><span class="sxs-lookup"><span data-stu-id="26029-112">The smart card subsystem defines the following groups.</span></span>



| <span data-ttu-id="26029-113">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="26029-113">Group</span></span>                | <span data-ttu-id="26029-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26029-114">Description</span></span>                                                                                                                                                                                            |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26029-115">Card $ allreaders</span><span class="sxs-lookup"><span data-stu-id="26029-115">SCard$AllReaders</span></span>     | <span data-ttu-id="26029-116">Diese Gruppe enthält alle Leser im System.</span><span class="sxs-lookup"><span data-stu-id="26029-116">This group contains all the readers in the system.</span></span> <span data-ttu-id="26029-117">Ein neuer Reader, der dem Smartcard-Subsystem zugewiesen ist, wird automatisch in die systemweite Reader-Gruppe, "SCard $ allreaders", eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="26029-117">A new reader given to the smart card subsystem is automatically included in the system-wide reader group, SCard$AllReaders.</span></span>                         |
| <span data-ttu-id="26029-118">"SCard $ defaultreaders"</span><span class="sxs-lookup"><span data-stu-id="26029-118">SCard$DefaultReaders</span></span> | <span data-ttu-id="26029-119">Diese Standardgruppe, eine für jedes [*Terminal*](../secgloss/t-gly.md), enthält alle dem Terminal zugewiesenen Leser, die nicht für eine bestimmte Verwendung reserviert sind.</span><span class="sxs-lookup"><span data-stu-id="26029-119">This default group, one for each [*terminal*](../secgloss/t-gly.md), contains all the readers assigned to the terminal that are not reserved for specific use.</span></span> |



 

 

 
