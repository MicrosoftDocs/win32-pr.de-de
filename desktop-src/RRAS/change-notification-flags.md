---
title: Benachrichtigungshub ändern
description: Benachrichtigungshub ändern
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Änderung
- Benachrichtigungshub ändern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310187"
---
# <a name="change-notification-flags"></a><span data-ttu-id="8cb88-105">Benachrichtigungshub ändern</span><span class="sxs-lookup"><span data-stu-id="8cb88-105">Change Notification Flags</span></span>



| <span data-ttu-id="8cb88-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="8cb88-106">Constant</span></span>                         | <span data-ttu-id="8cb88-107">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb88-107">Value</span></span>      | <span data-ttu-id="8cb88-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8cb88-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb88-109">RTM \_ NUM- \_ Änderungs \_ Typen</span><span class="sxs-lookup"><span data-stu-id="8cb88-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="8cb88-110">3</span><span class="sxs-lookup"><span data-stu-id="8cb88-110">3</span></span>          | <span data-ttu-id="8cb88-111">Gibt die Anzahl der Änderungs Typen an, die zurzeit vom Routing Tabellen-Manager verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb88-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="8cb88-112">RTM \_ - \_ Änderungstyp \_ alle</span><span class="sxs-lookup"><span data-stu-id="8cb88-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="8cb88-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="8cb88-113">0x0001</span></span>     | <span data-ttu-id="8cb88-114">Benachrichtigt den Client über alle Änderungen an einem Ziel.</span><span class="sxs-lookup"><span data-stu-id="8cb88-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="8cb88-115">RTM \_ - \_ Änderungstyp \_ am besten</span><span class="sxs-lookup"><span data-stu-id="8cb88-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="8cb88-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="8cb88-116">0x0002</span></span>     | <span data-ttu-id="8cb88-117">Benachrichtigt den Client über Änderungen an der besten Route oder wenn die beste Route geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8cb88-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="8cb88-118">RTM \_ - \_ Änderungstyp \_ Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="8cb88-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="8cb88-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="8cb88-119">0x0004</span></span>     | <span data-ttu-id="8cb88-120">Benachrichtigt den Client über alle optimalen Weiterleitungs Änderungen, die sich auf die Weiterleitung auswirken (z. b. Änderungen am nächsten Hop).</span><span class="sxs-lookup"><span data-stu-id="8cb88-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="8cb88-121">RTM \_ benachrichtigt \_ nur \_ markierte \_ Geräte-Geräte</span><span class="sxs-lookup"><span data-stu-id="8cb88-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="8cb88-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="8cb88-122">0x00010000</span></span> | <span data-ttu-id="8cb88-123">Benachrichtigt den Client über Änderungen an Zielen, die der Client markiert hat.</span><span class="sxs-lookup"><span data-stu-id="8cb88-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="8cb88-124">Wenn dieses Flag nicht angegeben wird, werden Änderungs Benachrichtigungs Meldungen für alle Ziele gesendet.</span><span class="sxs-lookup"><span data-stu-id="8cb88-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




