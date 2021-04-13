---
description: Für den Active Directory Writer sind bei Sicherungs Vorgängen keine besonderen Aktionen erforderlich.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: VSS-Sicherung und-Wiederherstellung des Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526291"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a><span data-ttu-id="06087-103">VSS-Sicherung und-Wiederherstellung des Active Directory</span><span class="sxs-lookup"><span data-stu-id="06087-103">VSS Backup and Restore of the Active Directory</span></span>

<span data-ttu-id="06087-104">Für den Active Directory Writer sind bei Sicherungs Vorgängen keine besonderen Aktionen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06087-104">The Active Directory writer requires no special actions during backup operations.</span></span> <span data-ttu-id="06087-105">Der Writer stellt dem Anforderer Informationen zu Komponenten-und Datei Satz Informationen zur Verfügung, und der Anforderer verwendet diese Informationen, um zu entscheiden, welche Dateien auf die Sicherungsmedien kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="06087-105">The writer will provide the requester with component and file set information, and the requester uses that information to decide which files to copy to backup media.</span></span> <span data-ttu-id="06087-106">Zum Sichern des Active Directory müssen keine speziellen APIs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06087-106">There is no need to use any special APIs to back up the Active Directory.</span></span>

<span data-ttu-id="06087-107">Die Art und Weise, wie eine Wiederherstellung ausgeführt wird, hängt davon ab, ob die Active Directory im Rahmen eines Notfall Wiederherstellungs Vorgangs wieder hergestellt wird oder ob die Wiederherstellung auf einem System ausgeführt wird, auf dem die Active Directory ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06087-107">How a restore is performed depends on whether the Active Directory is be restored as part of a disaster recovery operation, or if the restore is to a system on which the Active Directory is running.</span></span> <span data-ttu-id="06087-108">Außerdem kann das Alter der Sicherungskopie des Active Directory Zustands aufgrund Active Directory Tombstones ein Problem sein.</span><span class="sxs-lookup"><span data-stu-id="06087-108">In addition, the age of the backup copy of the Active Directory state may be an issue because of Active Directory tombstones.</span></span>

## <a name="active-directory-restoration-following-disaster-recovery"></a><span data-ttu-id="06087-109">Active Directory Wiederherstellung nach der Notfall Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="06087-109">Active Directory Restoration following Disaster Recovery</span></span>

<span data-ttu-id="06087-110">Nach einem Absturz, der eine Notfall Wiederherstellung erfordert, kann der Active Directory im Rahmen der Wiederherstellung des Betriebssystem Status wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="06087-110">Following a crash requiring disaster recovery, the Active Directory can be restored as part of the restoration of the operating system state.</span></span>

<span data-ttu-id="06087-111">Dieser Wiederherstellungs Vorgang ist im Wesentlichen eine Schreib lose Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="06087-111">This restore operation is essentially a writerless restore.</span></span>

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a><span data-ttu-id="06087-112">Active Directory Wiederherstellung auf dem System, auf dem es ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="06087-112">Active Directory Restoration on the System where It Is Running</span></span>

<span data-ttu-id="06087-113">Das System muss im Modus für die Verzeichnisdienst Wiederherstellung neu gestartet werden, wenn die Active Directory derzeit auf dem Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06087-113">The system must be rebooted in Directory Services Restore mode if the Active Directory is currently running on the server.</span></span>

<span data-ttu-id="06087-114">Das Betriebssystem wird dann ohne den Active Directory ausgeführt, und alle Benutzer Validierung erfolgt über den Security Accounts Manager (Sam) in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="06087-114">The operating system will then be running without the Active Directory, and all user validation occurs through the Security Accounts Manager (SAM) in the registry.</span></span> <span data-ttu-id="06087-115">Nur der Administrator verfügt über die Berechtigung zum Wiederherstellen des Active Directory.</span><span class="sxs-lookup"><span data-stu-id="06087-115">Only the administrator has permission to recover the Active Directory.</span></span>

<span data-ttu-id="06087-116">Im Verzeichnisdienst-Wiederherstellungs Modus kann eine VSS-Wiederherstellung normal fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="06087-116">Once in Directory Service Restore mode, a VSS restore can proceed normally.</span></span> <span data-ttu-id="06087-117">Es gibt keinen Grund, nicht-VSS-Win32-Active Directory-APIs zu verwenden, um den Active Directory-Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="06087-117">There is no reason to use non-VSS Win32 Active Directory APIs to restore the Active Directory state.</span></span>

## <a name="active-directory-restores-and-active-directory-tombstones"></a><span data-ttu-id="06087-118">Active Directory Wiederherstellungen und Active Directory Tombstones</span><span class="sxs-lookup"><span data-stu-id="06087-118">Active Directory Restores and Active Directory Tombstones</span></span>

<span data-ttu-id="06087-119">Jeder Wiederherstellungs Plan sollte sicherstellen, dass das Alter der Sicherung die Active Directory Tombstone-Lebensdauer (Standardwert 60 Tage) nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="06087-119">Any recovery plan should ensure that the age of the backup should not exceed the Active Directory Tombstone Lifetime (default is 60 days).</span></span>

<span data-ttu-id="06087-120">Durch die Wiederherstellung einer Sicherung, die älter als der Tombstone ist, werden von einem Domänen Controller Objekte verwendet, die nicht auf den anderen Servern repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="06087-120">Restoration of a backup older than the tombstone will cause a domain controller to have objects that are not replicated to the other servers.</span></span>

<span data-ttu-id="06087-121">Diese Objekte, die nicht repliziert werden, werden auf dem (wiederhergestellten) Domänen Controller nicht automatisch gelöscht, da die Tombstones dieser Objekte auf den anderen Replikaten bereits gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="06087-121">Those objects that are not replicated will not be deleted automatically on that (restored) domain controller because the tombstones of those objects on the other replicas have already been deleted.</span></span>

<span data-ttu-id="06087-122">Ein Administrator muss alle Objekte auf dem wiederhergestellten Domänen Controller, die nicht repliziert werden, manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="06087-122">An administrator will have to manually delete each of the objects on the restored domain controller that are not replicated.</span></span> <span data-ttu-id="06087-123">Inkrementelle Sicherungen der Active Directory werden nicht unterstützt. eine vollständige Sicherung ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="06087-123">Incremental backups of the Active Directory are not supported; a full backup is required.</span></span>

 

 



