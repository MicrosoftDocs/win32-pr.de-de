---
title: Verteiltes Dateisystem Funktionen
description: Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.
ms.assetid: 8f86b717-fe26-4550-8b71-8f7df5ca6022
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463c085115f6d3e88f9a3be80a890caa0aacb340
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483766"
---
# <a name="distributed-file-system-functions"></a><span data-ttu-id="12b53-103">Verteiltes Dateisystem Funktionen</span><span class="sxs-lookup"><span data-stu-id="12b53-103">Distributed File System Functions</span></span>

<span data-ttu-id="12b53-104">Im folgenden finden Sie die verteiltes Dateisystem (DFS)-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="12b53-104">The following are the Distributed File System (DFS) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="12b53-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="12b53-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="12b53-106">Netdfsadd</span><span class="sxs-lookup"><span data-stu-id="12b53-106">NetDfsAdd</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsadd)
</dt> <dd>
<span data-ttu-id="12b53-107">Erstellt eine neue DFS-Verknüpfung (verteiltes Dateisystem) oder fügt Ziele zu einem vorhandenen Link in einem DFS-Namespace hinzu.</span><span class="sxs-lookup"><span data-stu-id="12b53-107">Creates a new Distributed File System (DFS) link or adds targets to an existing link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-108">Netdfsaddftroot</span><span class="sxs-lookup"><span data-stu-id="12b53-108">NetDfsAddFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddftroot)
</dt> <dd>
<span data-ttu-id="12b53-109">Erstellt einen neuen domänenbasierten verteiltes Dateisystem-Namespace (DFS).</span><span class="sxs-lookup"><span data-stu-id="12b53-109">Creates a new domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="12b53-110">Wenn der Namespace bereits vorhanden ist, fügt die Funktion ihm das angegebene Stamm Ziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="12b53-110">If the namespace already exists, the function adds the specified root target to it.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-111">Netdfsaddroottarget</span><span class="sxs-lookup"><span data-stu-id="12b53-111">NetDfsAddRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddroottarget)
</dt> <dd>
<span data-ttu-id="12b53-112">Erstellt einen domänenbasierten oder eigenständigen DFS-Namespace oder fügt einem vorhandenen domänenbasierten Namespace ein neues Stamm Ziel hinzu.</span><span class="sxs-lookup"><span data-stu-id="12b53-112">Creates a domain-based or stand-alone DFS namespace or adds a new root target to an existing domain-based namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-113">Netdfsaddstdroot</span><span class="sxs-lookup"><span data-stu-id="12b53-113">NetDfsAddStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsaddstdroot)
</dt> <dd>
<span data-ttu-id="12b53-114">Erstellt einen neuen eigenständigen verteiltes Dateisystem-Namespace (DFS).</span><span class="sxs-lookup"><span data-stu-id="12b53-114">Creates a new stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-115">Netdfsenum</span><span class="sxs-lookup"><span data-stu-id="12b53-115">NetDfsEnum</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsenum)
</dt> <dd>
<span data-ttu-id="12b53-116">Listet die verteiltes Dateisystem (DFS)-Namespaces auf, die auf einem Server oder DFS-Verknüpfungen eines von einem Server gehosteten Namespace gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="12b53-116">Enumerates the Distributed File System (DFS) namespaces hosted on a server or DFS links of a namespace hosted by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-117">Netdfsgetclientinfo</span><span class="sxs-lookup"><span data-stu-id="12b53-117">NetDfsGetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> <dd>
<span data-ttu-id="12b53-118">Ruft Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link aus dem Cache ab, der vom DFS-Client verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="12b53-118">Retrieves information about a Distributed File System (DFS) root or link from the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-119">Netdfsgetftcontainersecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-119">NetDfsGetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="12b53-120">Ruft die Sicherheits Beschreibung für das Container Objekt für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory Domäne ab.</span><span class="sxs-lookup"><span data-stu-id="12b53-120">Retrieves the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-121">Netdfsgetinfo</span><span class="sxs-lookup"><span data-stu-id="12b53-121">NetDfsGetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetinfo)
</dt> <dd>
<span data-ttu-id="12b53-122">Ruft Informationen zu einem angegebenen verteiltes Dateisystem (DFS)-Stamm oder-Link in einem DFS-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="12b53-122">Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-123">Netdfsgetsecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-123">NetDfsGetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)
</dt> <dd>
<span data-ttu-id="12b53-124">Ruft die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="12b53-124">Retrieves the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-125">Netdfsgetstdcontainersecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-125">NetDfsGetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="12b53-126">Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="12b53-126">Retrieves the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-127">Netdfsgetsupportednamespaceversion</span><span class="sxs-lookup"><span data-stu-id="12b53-127">NetDfsGetSupportedNamespaceVersion</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsupportednamespaceversion)
</dt> <dd>
<span data-ttu-id="12b53-128">Bestimmt die unterstützte Metadatenversionsnummer.</span><span class="sxs-lookup"><span data-stu-id="12b53-128">Determines the supported metadata version number.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-129">Netdfsmove</span><span class="sxs-lookup"><span data-stu-id="12b53-129">NetDfsMove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsmove)
</dt> <dd>
<span data-ttu-id="12b53-130">Benennt oder verschiebt einen DFS-Link.</span><span class="sxs-lookup"><span data-stu-id="12b53-130">Renames or moves a DFS link.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-131">Netdfsremove</span><span class="sxs-lookup"><span data-stu-id="12b53-131">NetDfsRemove</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremove)
</dt> <dd>
<span data-ttu-id="12b53-132">Entfernt einen verteiltes Dateisystem (DFS)-Link oder ein bestimmtes Verknüpfungs Ziel eines DFS-Links in einem DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-132">Removes a Distributed File System (DFS) link or a specific link target of a DFS link in a DFS namespace.</span></span> <span data-ttu-id="12b53-133">Wenn Sie ein bestimmtes Verknüpfungs Ziel entfernen, wird der Link selbst entfernt, wenn das letzte Verknüpfungs Ziel der Verknüpfung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="12b53-133">When removing a specific link target, the link itself is removed if the last link target of the link is removed.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-134">Netdfsremovef</span><span class="sxs-lookup"><span data-stu-id="12b53-134">NetDfsRemoveFtRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftroot)
</dt> <dd>
<span data-ttu-id="12b53-135">Entfernt das angegebene Stamm Ziel aus einem domänenbasierten verteiltes Dateisystem (DFS)-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-135">Removes the specified root target from a domain-based Distributed File System (DFS) namespace.</span></span> <span data-ttu-id="12b53-136">Wenn das letzte Stamm Ziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-136">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="12b53-137">Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle darin Verknüpfungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="12b53-137">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-138">Netdfsremovestrootforced</span><span class="sxs-lookup"><span data-stu-id="12b53-138">NetDfsRemoveFtRootForced</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced)
</dt> <dd>
<span data-ttu-id="12b53-139">Entfernt das angegebene Stamm Ziel aus einem domänenbasierten verteiltes Dateisystem (DFS)-Namespace, auch wenn der Stamm Zielserver offline ist.</span><span class="sxs-lookup"><span data-stu-id="12b53-139">Removes the specified root target from a domain-based Distributed File System (DFS) namespace, even if the root target server is offline.</span></span> <span data-ttu-id="12b53-140">Wenn das letzte Stamm Ziel des DFS-Namespace entfernt wird, löscht die Funktion auch den DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-140">If the last root target of the DFS namespace is being removed, the function also deletes the DFS namespace.</span></span> <span data-ttu-id="12b53-141">Ein DFS-Namespace kann gelöscht werden, ohne zuerst alle darin Verknüpfungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="12b53-141">A DFS namespace can be deleted without first deleting all the links in it.</span></span>

> [!Note]
> <span data-ttu-id="12b53-142">Die [**netdfsremoveftrootforced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) -Funktion aktualisiert die Registrierung auf dem DFS-Stamm Zielserver nicht.</span><span class="sxs-lookup"><span data-stu-id="12b53-142">The [**NetDfsRemoveFtRootForced**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveftrootforced) function does not update the registry on the DFS root target server.</span></span> <span data-ttu-id="12b53-143">Weitere Informationen finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="12b53-143">For more information, see the Remarks section.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-144">Netdfsremoveroottarget</span><span class="sxs-lookup"><span data-stu-id="12b53-144">NetDfsRemoveRootTarget</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremoveroottarget)
</dt> <dd>
<span data-ttu-id="12b53-145">Entfernt ein DFS-Stamm Ziel aus einem domänenbasierten DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-145">Removes a DFS root target from a domain-based DFS namespace.</span></span> <span data-ttu-id="12b53-146">Wenn das Stammziel das letzte Stamm Ziel im DFS-Namespace ist, entfernt diese Funktion den DFS-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-146">If the root target is the last root target in the DFS namespace, this function removes the DFS namespace.</span></span> <span data-ttu-id="12b53-147">Diese Funktion kann auch verwendet werden, um einen eigenständigen DFS-Namespace zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="12b53-147">This function can also be used to remove a stand-alone DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-148">Netdfsremovestdroot</span><span class="sxs-lookup"><span data-stu-id="12b53-148">NetDfsRemoveStdRoot</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsremovestdroot)
</dt> <dd>
<span data-ttu-id="12b53-149">Löscht einen eigenständigen verteiltes Dateisystem (DFS)-Namespace.</span><span class="sxs-lookup"><span data-stu-id="12b53-149">Deletes a stand-alone Distributed File System (DFS) namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-150">Netdfssetclientinfo</span><span class="sxs-lookup"><span data-stu-id="12b53-150">NetDfsSetClientInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetclientinfo)
</dt> <dd>
<span data-ttu-id="12b53-151">Ändert Informationen zu einem verteiltes Dateisystem (DFS)-Stamm oder-Link im Cache, der vom DFS-Client verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="12b53-151">Modifies information about a Distributed File System (DFS) root or link in the cache maintained by the DFS client.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-152">Netdfssetftcontainersecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-152">NetDfsSetFtContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)
</dt> <dd>
<span data-ttu-id="12b53-153">Legt die Sicherheits Beschreibung für das Container Objekt für die domänenbasierten DFS-Namespaces in der angegebenen Active Directory Domäne fest.</span><span class="sxs-lookup"><span data-stu-id="12b53-153">Sets the security descriptor of the container object for the domain-based DFS namespaces in the specified Active Directory domain.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-154">Netdfssetinfo</span><span class="sxs-lookup"><span data-stu-id="12b53-154">NetDfsSetInfo</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetinfo)
</dt> <dd>
<span data-ttu-id="12b53-155">Legt Informationen über einen bestimmten verteiltes Dateisystem (DFS)-Stamm, ein Stamm Ziel, einen Link oder ein Verknüpfungs Ziel fest oder ändert Sie.</span><span class="sxs-lookup"><span data-stu-id="12b53-155">Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-156">Netdfssetsecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-156">NetDfsSetSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)
</dt> <dd>
<span data-ttu-id="12b53-157">Legt die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="12b53-157">Sets the security descriptor for the root object of the specified DFS namespace.</span></span>

</dd> <dt>

[<span data-ttu-id="12b53-158">Netdfssetstdcontainersecurity</span><span class="sxs-lookup"><span data-stu-id="12b53-158">NetDfsSetStdContainerSecurity</span></span>](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity)
</dt> <dd>
<span data-ttu-id="12b53-159">Legt die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Namespace fest.</span><span class="sxs-lookup"><span data-stu-id="12b53-159">Sets the security descriptor for the container object of the specified stand-alone DFS namespace.</span></span>

</dd> </dl>

<span data-ttu-id="12b53-160">Beachten Sie, dass eine Anwendung, die eine der Funktionen aufruft, indirekt bewirken kann, dass der lokale DFS-Namespace Server, der den Funktionsaufruf verarbeitet, eine vollständige Synchronisierung der zugehörigen Namespace Metadaten aus dem PDC-Emulatormaster für diese Domäne ausführt.</span><span class="sxs-lookup"><span data-stu-id="12b53-160">Note that an application invoking any of the functions may indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of the related namespace metadata from the PDC emulator master for that domain.</span></span> <span data-ttu-id="12b53-161">Diese vollständige Synchronisierung kann auch dann erfolgen, wenn der root-Skalierbarkeits Modus für diesen Namespace konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="12b53-161">This full synchronization could happen even when root scalability mode is configured for that namespace.</span></span>
