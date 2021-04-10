---
title: Itssbresourcepluginstoreex-Schnittstelle
description: Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste
- Itssbresourcepluginstoreex-Schnittstelle Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104295"
---
# <a name="itssbresourcepluginstoreex-interface"></a><span data-ttu-id="bbfe0-105">Itssbresourcepluginstoreex-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bbfe0-105">ITsSbResourcePluginStoreEx interface</span></span>

<span data-ttu-id="bbfe0-106">Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-106">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span> <span data-ttu-id="bbfe0-107">Mit diesen Methoden werden diese Objekte hinzugefügt, gelöscht und abgefragt.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-107">These methods add, delete, and query these objects.</span></span>

<span data-ttu-id="bbfe0-108">Diese Schnittstelle ist nur unter Windows Server 2012 R2 mit installiertem [KB3091411](https://support.microsoft.com/kb/3091411) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-108">This interface is only available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed.</span></span> <span data-ttu-id="bbfe0-109">Die Methoden [**acquiretargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) und [**releasetargetlock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) der [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) -Schnittstelle sind ab Windows Server 2016 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-109">The [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) and [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) methods of the [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface are available starting with Windows Server 2016.</span></span>

## <a name="members"></a><span data-ttu-id="bbfe0-110">Member</span><span class="sxs-lookup"><span data-stu-id="bbfe0-110">Members</span></span>

<span data-ttu-id="bbfe0-111">Die **itssbresourcepluginstoreex** -Schnittstelle erbt von [**itssbresourcepluginstore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span><span class="sxs-lookup"><span data-stu-id="bbfe0-111">The **ITsSbResourcePluginStoreEx** interface inherits from [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore).</span></span> <span data-ttu-id="bbfe0-112">**Itssbresourcepluginstoreex** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bbfe0-112">**ITsSbResourcePluginStoreEx** also has these types of members:</span></span>

-   [<span data-ttu-id="bbfe0-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="bbfe0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bbfe0-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="bbfe0-114">Methods</span></span>

<span data-ttu-id="bbfe0-115">Die **itssbresourcepluginstoreex** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-115">The **ITsSbResourcePluginStoreEx** interface has these methods.</span></span>



| <span data-ttu-id="bbfe0-116">Methode</span><span class="sxs-lookup"><span data-stu-id="bbfe0-116">Method</span></span>                                                                                                            | <span data-ttu-id="bbfe0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbfe0-117">Description</span></span>                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbfe0-118">**Acquiretargetlock**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-118">**AcquireTargetLock**</span></span>](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | <span data-ttu-id="bbfe0-119">Sperrt ein Ziel.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-119">Locks a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="bbfe0-120">**Addenvironmentonstore**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-120">**AddEnvironmentToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | <span data-ttu-id="bbfe0-121">Fügt dem Ressourcen-Plug-in-Speicher eine Umgebung hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-121">Adds an environment to the resource plug-in store.</span></span><br/>                                                   |
| [<span data-ttu-id="bbfe0-122">**Addsessionto Store**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-122">**AddSessionToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | <span data-ttu-id="bbfe0-123">Fügt dem Ressourcen-Plug-in-Speicher eine neue Sitzung hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-123">Adds a new session to the resource plug-in store.</span></span><br/>                                                    |
| [<span data-ttu-id="bbfe0-124">**AddTarget-Store**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-124">**AddTargetToStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | <span data-ttu-id="bbfe0-125">Fügt dem Ressourcen-Plug-in-Speicher ein Ziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-125">Adds a target to the resource plug-in store.</span></span><br/>                                                         |
| [<span data-ttu-id="bbfe0-126">**DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-126">**DeleteTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | <span data-ttu-id="bbfe0-127">Löscht ein Ziel.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-127">Deletes a target.</span></span><br/>                                                                                    |
| [<span data-ttu-id="bbfe0-128">**Enumerateenvironment**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-128">**EnumerateEnvironments**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | <span data-ttu-id="bbfe0-129">Gibt ein Array zurück, das die Umgebungen enthält, die im Ressourcen-Plug-in-Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-129">Returns an array that contains the environments present in the resource plug-in store.</span></span><br/>               |
| [<span data-ttu-id="bbfe0-130">**Enumeratefarms**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-130">**EnumerateFarms**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | <span data-ttu-id="bbfe0-131">Listet alle Farmen auf, die dem Ressourcen-Plug-in-Speicher hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-131">Enumerates all the farms that have been added to the resource plug-in store.</span></span><br/>                         |
| [<span data-ttu-id="bbfe0-132">**Enumeratesessions**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-132">**EnumerateSessions**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | <span data-ttu-id="bbfe0-133">Listet eine angegebene Gruppe von Sitzungen auf.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-133">Enumerates a specified set of sessions.</span></span><br/>                                                              |
| [<span data-ttu-id="bbfe0-134">**Enumeratetargets**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-134">**EnumerateTargets**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | <span data-ttu-id="bbfe0-135">Gibt ein Array zurück, das die angegebenen Ziele enthält, die im Ressourcen-Plug-in-Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-135">Returns an array that contains the specified targets that are present in the resource plug-in store.</span></span><br/> |
| [<span data-ttu-id="bbfe0-136">**Getfarmproperty**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-136">**GetFarmProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | <span data-ttu-id="bbfe0-137">Ruft eine Eigenschaft einer Farm ab.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-137">Retrieves a property of a farm.</span></span><br/>                                                                      |
| [<span data-ttu-id="bbfe0-138">**Queryenvironment**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-138">**QueryEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | <span data-ttu-id="bbfe0-139">Gibt das angegebene Umgebungs Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-139">Returns the specified environment object.</span></span><br/>                                                            |
| [<span data-ttu-id="bbfe0-140">**Querysessionbysessionid**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-140">**QuerySessionBySessionId**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | <span data-ttu-id="bbfe0-141">Gibt das Sitzungs Objekt zurück, das über die angegebene Sitzungs-ID verfügt.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-141">Returns the session object that has the specified session ID.</span></span><br/>                                        |
| [<span data-ttu-id="bbfe0-142">**Querytarget**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-142">**QueryTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | <span data-ttu-id="bbfe0-143">Gibt das Ziel mit dem angegebenen Zielnamen und dem Namen der Farm zurück.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-143">Returns the target that has the specified target name and farm name.</span></span><br/>                                 |
| [<span data-ttu-id="bbfe0-144">**Releasetargetlock**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-144">**ReleaseTargetLock**</span></span>](itssbresourcepluginstoreex-releasetargetlock.md)                                         | <span data-ttu-id="bbfe0-145">Gibt eine Sperre für ein Ziel frei.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-145">Releases a lock on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="bbfe0-146">**Removeumgebfromstore**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-146">**RemoveEnvironmentFromStore**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | <span data-ttu-id="bbfe0-147">Entfernt die angegebene Umgebung aus dem Ressourcen-Plug-in-Speicher.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-147">Removes the specified environment from the resource plug-in store.</span></span><br/>                                   |
| [<span data-ttu-id="bbfe0-148">**Saveenvironment**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-148">**SaveEnvironment**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | <span data-ttu-id="bbfe0-149">Speichert eine Umgebung.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-149">Saves an environment.</span></span><br/>                                                                                |
| [<span data-ttu-id="bbfe0-150">**Savesession**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-150">**SaveSession**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | <span data-ttu-id="bbfe0-151">Speichert eine Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-151">Saves a session.</span></span><br/>                                                                                     |
| [<span data-ttu-id="bbfe0-152">**Savetarget**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-152">**SaveTarget**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | <span data-ttu-id="bbfe0-153">Speichert ein Ziel.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-153">Saves a target.</span></span><br/>                                                                                      |
| [<span data-ttu-id="bbfe0-154">**"Abtenvironmentproperty"**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-154">**SetEnvironmentProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | <span data-ttu-id="bbfe0-155">Legt eine Eigenschaft für eine Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-155">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="bbfe0-156">**"Abtenvironmentpropertywithversioncheck"**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-156">**SetEnvironmentPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | <span data-ttu-id="bbfe0-157">Legt eine Eigenschaft für eine Umgebung fest.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-157">Sets a property on an environment.</span></span><br/>                                                                   |
| [<span data-ttu-id="bbfe0-158">**"Endessionstate"**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-158">**SetSessionState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | <span data-ttu-id="bbfe0-159">Legt den Status einer Sitzung fest</span><span class="sxs-lookup"><span data-stu-id="bbfe0-159">Sets the state of a session.</span></span><br/>                                                                         |
| [<span data-ttu-id="bbfe0-160">**SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-160">**SetTargetProperty**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | <span data-ttu-id="bbfe0-161">Legt eine Eigenschaft für ein Ziel fest.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-161">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="bbfe0-162">**Settargetpropertywithversioncheck**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-162">**SetTargetPropertyWithVersionCheck**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | <span data-ttu-id="bbfe0-163">Legt eine Eigenschaft für ein Ziel fest.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-163">Sets a property on a target.</span></span><br/>                                                                         |
| [<span data-ttu-id="bbfe0-164">**Settargetstate**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-164">**SetTargetState**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | <span data-ttu-id="bbfe0-165">Legt den Zustand eines Ziels fest.</span><span class="sxs-lookup"><span data-stu-id="bbfe0-165">Sets the state of a target.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="bbfe0-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbfe0-166">Requirements</span></span>



| <span data-ttu-id="bbfe0-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbfe0-167">Requirement</span></span> | <span data-ttu-id="bbfe0-168">Wert</span><span class="sxs-lookup"><span data-stu-id="bbfe0-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbfe0-169">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbfe0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfe0-170">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bbfe0-170">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bbfe0-171">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbfe0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfe0-172">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bbfe0-172">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="bbfe0-173">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bbfe0-173">End of server support</span></span><br/>    | <span data-ttu-id="bbfe0-174">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bbfe0-174">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="bbfe0-175">IID</span><span class="sxs-lookup"><span data-stu-id="bbfe0-175">IID</span></span><br/>                      | <span data-ttu-id="bbfe0-176">IID \_ itssbresourcepluginstoreex ist als 80b83ffd-625d-11e5-bea1-a0481c7e9064 definiert</span><span class="sxs-lookup"><span data-stu-id="bbfe0-176">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbfe0-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbfe0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbfe0-178">**Itssbresourcepluginstore**</span><span class="sxs-lookup"><span data-stu-id="bbfe0-178">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[<span data-ttu-id="bbfe0-179">Remotedesktop Virtualisierungsschnittstellen</span><span class="sxs-lookup"><span data-stu-id="bbfe0-179">Remote Desktop Virtualization Interfaces</span></span>](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





