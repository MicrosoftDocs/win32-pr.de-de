---
description: Im folgenden finden Sie die verteiltes Dateisystem DFS-Strukturen.
ms.assetid: f55ad3c0-0457-4d5a-a7d3-8eff744d573d
title: Verteiltes Dateisystem Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fc3351402c4721952cbfc4dc3fe3c6ac6d3a76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483771"
---
# <a name="distributed-file-system-structures"></a><span data-ttu-id="0e0c2-103">Verteiltes Dateisystem Strukturen</span><span class="sxs-lookup"><span data-stu-id="0e0c2-103">Distributed File System Structures</span></span>

<span data-ttu-id="0e0c2-104">Im folgenden sind die verteiltes Dateisystem (DFS)-Strukturen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="0e0c2-104">The following are the Distributed File System (DFS) structures:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0e0c2-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0e0c2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0e0c2-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span><span class="sxs-lookup"><span data-stu-id="0e0c2-106">**DFS_GET_PKT_ENTRY_STATE_ARG**</span></span>](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg)
</dt> <dd>

<span data-ttu-id="0e0c2-107">Der Eingabepuffer wird mit dem [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) Steuerungs Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-107">Input buffer used with the [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code</span></span>
</dd> <dt>

[<span data-ttu-id="0e0c2-108">_DFS_INFO_1 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-108">_DFS_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_1)
</dt> <dd>
<span data-ttu-id="0e0c2-109">Enthält den Namen eines DFS-Stamms oder-Links (verteiltes Dateisystem).</span><span class="sxs-lookup"><span data-stu-id="0e0c2-109">Contains the name of a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-110">_DFS_INFO_2 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-110">_DFS_INFO_2 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_2)
</dt> <dd>
<span data-ttu-id="0e0c2-111">Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-111">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0e0c2-112">Diese Struktur enthält den Namen, den Status und die Anzahl der DFS-Ziele für den Stamm oder Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-112">This structure contains the name, status, and number of DFS targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-113">_DFS_INFO_3 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-113">_DFS_INFO_3 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_3)
</dt> <dd>
<span data-ttu-id="0e0c2-114">Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-114">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0e0c2-115">Diese Struktur enthält den Namen, den Status, die Anzahl der DFS-Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-115">This structure contains the name, status, number of DFS targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-116">_DFS_INFO_4 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-116">_DFS_INFO_4 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_4)
</dt> <dd>
<span data-ttu-id="0e0c2-117">Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-117">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0e0c2-118">Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, die Anzahl der Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-118">This structure contains the name, status, **GUID**, time-out, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-119">_DFS_INFO_5 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-119">_DFS_INFO_5 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_5)
</dt> <dd>
<span data-ttu-id="0e0c2-120">Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-120">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0e0c2-121">Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, den Namespace bzw. die Stamm-/Linkeigenschaften, die Metadatengröße und die Anzahl der Ziele für den Stamm oder Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-121">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, and number of targets for the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-122">_DFS_INFO_6 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-122">_DFS_INFO_6 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_6)
</dt> <dd>
<span data-ttu-id="0e0c2-123">Enthält Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-123">Contains information about a Distributed File System (DFS) root or link.</span></span> <span data-ttu-id="0e0c2-124">Diese Struktur enthält den Namen, den Status, die **GUID**, das Timeout, den Namespace bzw. die Stamm-/Linkeigenschaften, die Metadatengröße, die Anzahl der Ziele und Informationen zu den einzelnen Zielen des Stamms oder Links.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-124">This structure contains the name, status, **GUID**, time-out, namespace/root/link properties, metadata size, number of targets, and information about each target of the root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-125">_DFS_INFO_7 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-125">_DFS_INFO_7 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_7)
</dt> <dd>
<span data-ttu-id="0e0c2-126">Enthält Informationen zu einem DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-126">Contains information about a DFS namespace.</span></span> <span data-ttu-id="0e0c2-127">Diese Struktur enthält die Versions- **GUID** für die Metadaten für den Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-127">This structure contains the version **GUID** for the metadata for the namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-128">_DFS_INFO_8 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-128">_DFS_INFO_8 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_8)
</dt> <dd>
<span data-ttu-id="0e0c2-129">Enthält den Namen, den Status, die **GUID**, das Timeout, die Eigenschaftenflags, die Metadatengröße, Informationen zum DFS-Ziel und die Sicherheits Beschreibung für den Link Analyse Punkt für einen Stamm oder Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-129">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, and link reparse point security descriptor for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-130">_DFS_INFO_9 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-130">_DFS_INFO_9 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_9)
</dt> <dd>
<span data-ttu-id="0e0c2-131">Enthält den Namen, den Status, die **GUID**, das Timeout, die Eigenschaftenflags, die Metadatengröße, Informationen zum DFS-Ziel, die Sicherheits Beschreibung für den Link Analyse Punkt und eine Liste der DFS-Ziele für einen Stamm oder Link.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-131">Contains the name, status, **GUID**, time-out, property flags, metadata size, DFS target information, link reparse point security descriptor, and a list of DFS targets for a root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-132">_DFS_INFO_50 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-132">_DFS_INFO_50 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_50)
</dt> <dd>
<span data-ttu-id="0e0c2-133">Enthält die DFS-Metadatenversion und die Funktionen eines vorhandenen DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-133">Contains the DFS metadata version and capabilities of an existing DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-134">_DFS_INFO_100 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-134">_DFS_INFO_100 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_100)
</dt> <dd>
<span data-ttu-id="0e0c2-135">Enthält einen Kommentar, der einem DFS-Stamm oder einem verteiltes Dateisystem-Link zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-135">Contains a comment associated with a Distributed File System (DFS) root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-136">_DFS_INFO_101 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-136">_DFS_INFO_101 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_101)
</dt> <dd>
<span data-ttu-id="0e0c2-137">Beschreibt den Zustand des Speichers in einem DFS-Stamm, einem Link, einem Stammziel oder einem Verknüpfungs Ziel.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-137">Describes the state of storage on a DFS root, link, root target, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-138">_DFS_INFO_102 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-138">_DFS_INFO_102 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_102)
</dt> <dd>
<span data-ttu-id="0e0c2-139">Enthält einen Timeout Wert, der einem verteiltes Dateisystem (DFS)-Stamm oder einem Link in einem benannten DFS-Stamm zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-139">Contains a time-out value to associate with a Distributed File System (DFS) root or a link in a named DFS root.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-140">_DFS_INFO_103 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-140">_DFS_INFO_103 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_103)
</dt> <dd>
<span data-ttu-id="0e0c2-141">Enthält Eigenschaften, mit denen bestimmte Verhalten für einen DFS-Stamm oder-Link festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-141">Contains properties that set specific behaviors for a DFS root or link.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-142">_DFS_INFO_104 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-142">_DFS_INFO_104 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_104)
</dt> <dd>
<span data-ttu-id="0e0c2-143">Enthält die Priorität eines DFS-Stammpink oder-Verknüpfungs Ziels.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-143">Contains the priority of a DFS root target or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-144">_DFS_INFO_105 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-144">_DFS_INFO_105 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_105)
</dt> <dd>
<span data-ttu-id="0e0c2-145">Enthält Informationen zu einem DFS-Stamm oder-Link, einschließlich Kommentar-, Zustands-, Timeout-und DFS-Verhalten, die durch Eigenschaftenflags angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-145">Contains information about a DFS root or link, including comment, state, time-out, and DFS behaviors specified by property flags.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-146">_DFS_INFO_106 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-146">_DFS_INFO_106 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_106)
</dt> <dd>
<span data-ttu-id="0e0c2-147">Enthält den Speicher Zustand und die Priorität für ein DFS-Stamm Ziel oder-Verknüpfungs Ziel.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-147">Contains the storage state and priority for a DFS root target or link target.</span></span> <span data-ttu-id="0e0c2-148">Diese Struktur ist nur für die Verwendung mit der [**netdfssetinfo**](netdfssetinfo.md) -Funktion vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-148">This structure is only for use with the [**NetDfsSetInfo**](netdfssetinfo.md) function.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-149">_DFS_INFO_107 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-149">_DFS_INFO_107 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_107)
</dt> <dd>
<span data-ttu-id="0e0c2-150">Enthält Informationen zu einem DFS-Stamm oder-Link, einschließlich Kommentar, Status, Timeout, Eigenschaftenflags und Sicherheits Beschreibung für den Link Analyse Punkt.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-150">Contains information about a DFS root or link, including the comment, state, time-out, property flags, and link reparse point security descriptor.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-151">_DFS_INFO_150 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-151">_DFS_INFO_150 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_150)
</dt> <dd>
<span data-ttu-id="0e0c2-152">Enthält die Sicherheits Beschreibung für den Analyse Punkt eines DFS-Links.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-152">Contains the security descriptor for a DFS link's reparse point.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-153">_DFS_INFO_200 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-153">_DFS_INFO_200 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_200)
</dt> <dd>
<span data-ttu-id="0e0c2-154">Enthält den Namen eines domänenbasierten verteiltes Dateisystem-Namespace (DFS).</span><span class="sxs-lookup"><span data-stu-id="0e0c2-154">Contains the name of a domain-based Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-155">_DFS_INFO_300 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-155">_DFS_INFO_300 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_info_300)
</dt> <dd>
<span data-ttu-id="0e0c2-156">Enthält den Namen und den Typ (Domänen basiert oder eigenständig) eines DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-156">Contains the name and type (domain-based or stand-alone) of a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-157">_DFS_STORAGE_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-157">_DFS_STORAGE_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info)
</dt> <dd>
<span data-ttu-id="0e0c2-158">Enthält Informationen zu einem DFS-Stamm oder-Verknüpfungs Ziel in einem DFS-Namespace oder dem vom DFS-Client verwalteten Cache.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-158">Contains information about a DFS root or link target in a DFS namespace or from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-159">_DFS_STORAGE_INFO_1 Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-159">_DFS_STORAGE_INFO_1 structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_storage_info_1)
</dt> <dd>
<span data-ttu-id="0e0c2-160">Enthält Informationen zu einem DFS-Ziel, einschließlich des DFS-Zielserver namens und des Freigabe namens sowie des Ziel Zustands und der Ziel Priorität.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-160">Contains information about a DFS target, including the DFS target server name and share name as well as the target's state and priority.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-161">_DFS_SUPPORTED_NAMESPACE_VERSION_INFO structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_supported_namespace_version_info)
</dt> <dd>
<span data-ttu-id="0e0c2-162">Enthält Versionsinformationen für einen DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-162">Contains version information for a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="0e0c2-163">_DFS_TARGET_PRIORITY Struktur</span><span class="sxs-lookup"><span data-stu-id="0e0c2-163">_DFS_TARGET_PRIORITY structure</span></span>](/windows/desktop/api/lmdfs/ns-lmdfs-dfs_target_priority)
</dt> <dd>
<span data-ttu-id="0e0c2-164">Enthält die Prioritäts Klasse und den Rang eines bestimmten DFS-Ziels.</span><span class="sxs-lookup"><span data-stu-id="0e0c2-164">Contains the priority class and rank of a specific DFS target.</span></span>

</dd> </dl>
