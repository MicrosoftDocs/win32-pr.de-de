---
title: WinNT-Objektklassen Hierarchie
description: Die Objektklassen Hierarchie von Winnt beginnt beim Namespace-Objekt.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, Objektklassen Hierarchie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515452"
---
# <a name="winnt-object-class-hierarchy"></a><span data-ttu-id="63731-104">WinNT-Objektklassen Hierarchie</span><span class="sxs-lookup"><span data-stu-id="63731-104">WinNT Object Class Hierarchy</span></span>

<span data-ttu-id="63731-105">Die Objektklassen Hierarchie von Winnt beginnt beim Namespace-Objekt.</span><span class="sxs-lookup"><span data-stu-id="63731-105">The WinNT object class hierarchy starts from the Namespace object.</span></span>



| <span data-ttu-id="63731-106">Objektklasse</span><span class="sxs-lookup"><span data-stu-id="63731-106">Object class</span></span>                   | <span data-ttu-id="63731-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63731-107">Description</span></span>                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="63731-108">Namespace</span><span class="sxs-lookup"><span data-stu-id="63731-108">Namespace</span></span><br/>           | <span data-ttu-id="63731-109">Objekt Container der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="63731-109">Top-level object container.</span></span><br/>                                            |
| <span data-ttu-id="63731-110">Domain</span><span class="sxs-lookup"><span data-stu-id="63731-110">Domain</span></span><br/>              | <span data-ttu-id="63731-111">Die Windows NT-Domäne.</span><span class="sxs-lookup"><span data-stu-id="63731-111">The Windows NT domain.</span></span><br/>                                                 |
| <span data-ttu-id="63731-112">Benutzer</span><span class="sxs-lookup"><span data-stu-id="63731-112">User</span></span><br/>                | <span data-ttu-id="63731-113">Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="63731-113">User account.</span></span><br/>                                                          |
| <span data-ttu-id="63731-114">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="63731-114">Group</span></span><br/>               | <span data-ttu-id="63731-115">Gruppenkonto zum Verwalten von Zugriffsrechten.</span><span class="sxs-lookup"><span data-stu-id="63731-115">Group account for managing access rights.</span></span><br/>                              |
| <span data-ttu-id="63731-116">Usergroupcollection</span><span class="sxs-lookup"><span data-stu-id="63731-116">UserGroupCollection</span></span><br/> | <span data-ttu-id="63731-117">Eine Gruppe von Benutzergruppen, die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.</span><span class="sxs-lookup"><span data-stu-id="63731-117">A set of user groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/>  |
| <span data-ttu-id="63731-118">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="63731-118">GroupCollection</span></span><br/>     | <span data-ttu-id="63731-119">Ein Satz anderer Gruppen, die [**iadsmembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)implementieren.</span><span class="sxs-lookup"><span data-stu-id="63731-119">A set of other groups implementing [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).</span></span><br/> |
| <span data-ttu-id="63731-120">Computer</span><span class="sxs-lookup"><span data-stu-id="63731-120">Computer</span></span><br/>            | <span data-ttu-id="63731-121">Windows NT 4,0-Server oder-Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="63731-121">Windows NT 4.0 server or workstation.</span></span><br/>                                  |
| <span data-ttu-id="63731-122">PrintJob</span><span class="sxs-lookup"><span data-stu-id="63731-122">PrintJob</span></span><br/>            | <span data-ttu-id="63731-123">Druckauftrag in der Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="63731-123">Print job in the print queue.</span></span><br/>                                          |
| <span data-ttu-id="63731-124">Printjobscollection</span><span class="sxs-lookup"><span data-stu-id="63731-124">PrintJobsCollection</span></span><br/> | <span data-ttu-id="63731-125">Ein Satz von Druckaufträgen.</span><span class="sxs-lookup"><span data-stu-id="63731-125">A set of print jobs.</span></span><br/>                                                   |
| <span data-ttu-id="63731-126">PrintQueue</span><span class="sxs-lookup"><span data-stu-id="63731-126">PrintQueue</span></span><br/>          | <span data-ttu-id="63731-127">Druck Warteschlange auf einem Druckerspooler.</span><span class="sxs-lookup"><span data-stu-id="63731-127">Print queue on a printer spooler.</span></span><br/>                                      |
| <span data-ttu-id="63731-128">Dienst</span><span class="sxs-lookup"><span data-stu-id="63731-128">Service</span></span><br/>             | <span data-ttu-id="63731-129">Anwendung, die als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63731-129">Application running as a service.</span></span><br/>                                      |
| <span data-ttu-id="63731-130">File Service</span><span class="sxs-lookup"><span data-stu-id="63731-130">FileService</span></span><br/>         | <span data-ttu-id="63731-131">Dienste, die auf das Dateisystem zugreifen</span><span class="sxs-lookup"><span data-stu-id="63731-131">Services accessing file system.</span></span><br/>                                        |
| <span data-ttu-id="63731-132">FileShare</span><span class="sxs-lookup"><span data-stu-id="63731-132">FileShare</span></span><br/>           | <span data-ttu-id="63731-133">Der Dateifreigabe Punkt.</span><span class="sxs-lookup"><span data-stu-id="63731-133">File share point.</span></span><br/>                                                      |
| <span data-ttu-id="63731-134">Resource</span><span class="sxs-lookup"><span data-stu-id="63731-134">Resource</span></span><br/>            | <span data-ttu-id="63731-135">Eine Ressource im Dienst.</span><span class="sxs-lookup"><span data-stu-id="63731-135">A resource in the service.</span></span><br/>                                             |
| <span data-ttu-id="63731-136">Sitzung</span><span class="sxs-lookup"><span data-stu-id="63731-136">Session</span></span><br/>             | <span data-ttu-id="63731-137">Eine aktive Datei Dienst Verbindung.</span><span class="sxs-lookup"><span data-stu-id="63731-137">An active file service connection.</span></span><br/>                                     |
| <span data-ttu-id="63731-138">Benutzer</span><span class="sxs-lookup"><span data-stu-id="63731-138">User</span></span><br/>                | <span data-ttu-id="63731-139">Lokales Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="63731-139">Local user account.</span></span><br/>                                                    |
| <span data-ttu-id="63731-140">Gruppieren</span><span class="sxs-lookup"><span data-stu-id="63731-140">Group</span></span><br/>               | <span data-ttu-id="63731-141">Lokale Gruppe.</span><span class="sxs-lookup"><span data-stu-id="63731-141">Local group.</span></span><br/>                                                           |
| <span data-ttu-id="63731-142">UserCollection</span><span class="sxs-lookup"><span data-stu-id="63731-142">UserCollection</span></span><br/>      | <span data-ttu-id="63731-143">Sammlung lokaler Benutzer.</span><span class="sxs-lookup"><span data-stu-id="63731-143">Collection of local users.</span></span><br/>                                             |
| <span data-ttu-id="63731-144">GroupCollection</span><span class="sxs-lookup"><span data-stu-id="63731-144">GroupCollection</span></span><br/>     | <span data-ttu-id="63731-145">Sammlung lokaler Gruppen.</span><span class="sxs-lookup"><span data-stu-id="63731-145">Collection of local groups.</span></span><br/>                                            |
| <span data-ttu-id="63731-146">Schema</span><span class="sxs-lookup"><span data-stu-id="63731-146">Schema</span></span><br/>              | <span data-ttu-id="63731-147">WinNT-Schema Container.</span><span class="sxs-lookup"><span data-stu-id="63731-147">WinNT Schema container.</span></span><br/>                                                |
| <span data-ttu-id="63731-148">Klasse</span><span class="sxs-lookup"><span data-stu-id="63731-148">Class</span></span><br/>               | <span data-ttu-id="63731-149">Schema Klassendefinition.</span><span class="sxs-lookup"><span data-stu-id="63731-149">Schema class definition.</span></span><br/>                                               |
| <span data-ttu-id="63731-150">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63731-150">Property</span></span><br/>            | <span data-ttu-id="63731-151">Schema Attribut Definition.</span><span class="sxs-lookup"><span data-stu-id="63731-151">Schema attribute definition.</span></span><br/>                                           |
| <span data-ttu-id="63731-152">Syntax</span><span class="sxs-lookup"><span data-stu-id="63731-152">Syntax</span></span><br/>              | <span data-ttu-id="63731-153">Syntax einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="63731-153">Syntax of a property.</span></span><br/>                                                  |



 

 

 





