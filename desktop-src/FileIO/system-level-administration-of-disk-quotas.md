---
description: Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen. Der Administrator kann auch Standard Kontingente für das Volume festlegen.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Verwaltung von Datenträger Kontingenten auf System Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214766"
---
# <a name="system-level-administration-of-disk-quotas"></a><span data-ttu-id="01250-104">Verwaltung von Datenträger Kontingenten auf System Ebene</span><span class="sxs-lookup"><span data-stu-id="01250-104">System-level Administration of Disk Quotas</span></span>

<span data-ttu-id="01250-105">Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen.</span><span class="sxs-lookup"><span data-stu-id="01250-105">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="01250-106">Der Administrator kann auch Standard Kontingente für das Volume festlegen.</span><span class="sxs-lookup"><span data-stu-id="01250-106">The administrator can also set default quotas for the volume.</span></span> <span data-ttu-id="01250-107">Ein neuer Benutzer auf dem Volume erhält das Standard Kontingent, es sei denn, der Administrator hat ein speziell für diesen Benutzerspezifisches Kontingent festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01250-107">A new user on the volume receives the default quota unless the administrator established a quota specifically for that user.</span></span>

<span data-ttu-id="01250-108">Der Administrator kann die Ebene der Kontingent Nachverfolgung und Erzwingung (oder Kontingent Status), die Standard Kontingent Limits und die Kontingent Informationen pro Benutzer Abfragen.</span><span class="sxs-lookup"><span data-stu-id="01250-108">The administrator can query the level of quota tracking and enforcement (or quota states), the default quota limits, and the per-user quota information.</span></span> <span data-ttu-id="01250-109">Die Kontingent Informationen pro Benutzer enthalten die feste Kontingent Grenze, den Warnungs Schwellenwert und die Kontingent Nutzung des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="01250-109">The per-user quota information contains the user's hard quota limit, warning threshold, and the quota usage.</span></span> <span data-ttu-id="01250-110">Der Administrator kann die Kontingent Erzwingung auch aktivieren oder deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="01250-110">The administrator can also enable or disable quota enforcement.</span></span>

<span data-ttu-id="01250-111">Es gibt drei Kontingent Zustände, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="01250-111">There are three quota states, as shown in the following table.</span></span>



| <span data-ttu-id="01250-112">State</span><span class="sxs-lookup"><span data-stu-id="01250-112">State</span></span>          | <span data-ttu-id="01250-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01250-113">Description</span></span>                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01250-114">Kontingent deaktiviert</span><span class="sxs-lookup"><span data-stu-id="01250-114">Quota disabled</span></span> | <span data-ttu-id="01250-115">Kontingent Nutzungsänderungen werden nicht nachverfolgt, die Kontingent Limits werden jedoch nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="01250-115">Quota usage changes are not tracked, but the quota limits are not removed.</span></span> <span data-ttu-id="01250-116">In diesem Zustand wird die Leistung von Datenträger Kontingenten nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="01250-116">In this state, performance is not affected by disk quotas.</span></span> <span data-ttu-id="01250-117">Dies ist die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="01250-117">This is the default state.</span></span>                         |
| <span data-ttu-id="01250-118">Kontingent nachverfolgt</span><span class="sxs-lookup"><span data-stu-id="01250-118">Quota tracked</span></span>  | <span data-ttu-id="01250-119">Kontingent Nutzungsänderungen werden nachverfolgt, aber Kontingent Limits werden nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="01250-119">Quota usage changes are tracked, but quota limits are not enforced.</span></span> <span data-ttu-id="01250-120">In diesem Zustand werden keine Kontingent Verletzungs Ereignisse generiert, und es sind keine Datei Vorgänge aufgrund von Datenträger Kontingent Verstößen fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="01250-120">In this state, no quota violation events are generated and no file operations fail because of disk quota violations.</span></span> |
| <span data-ttu-id="01250-121">Kontingent erzwungen</span><span class="sxs-lookup"><span data-stu-id="01250-121">Quota enforced</span></span> | <span data-ttu-id="01250-122">Kontingent Nutzungsänderungen werden nachverfolgt, und Kontingent Limits werden erzwungen.</span><span class="sxs-lookup"><span data-stu-id="01250-122">Quota usage changes are tracked and quota limits are enforced.</span></span>                                                                                                                           |



 

 

 



