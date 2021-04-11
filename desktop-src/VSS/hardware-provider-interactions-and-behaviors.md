---
description: Interaktionen und Verhalten von Hardware Anbietern
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interaktionen und Verhalten von Hardware Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215547"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="799b5-103">Interaktionen und Verhalten von Hardware Anbietern</span><span class="sxs-lookup"><span data-stu-id="799b5-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="799b5-104">Hardware Anbieter unterstützen möglicherweise die Schatten Kopien Copy-on-Write und/oder Full Copy Mirror (differenzielle und/oder Plex).</span><span class="sxs-lookup"><span data-stu-id="799b5-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="799b5-105">Die Ressourcen Zuordnung für Schatten Kopien sollte dem Kontext folgen, der von der Anforderer im [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)-enumeriert durch den [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)für den Schattenkopiesatz angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="799b5-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="799b5-106">Wenn die anfordernde Person einen schattenkopiekontext angibt, der vom Anbieter unterstützt wird, sollte der Anbieter mithilfe dieser Methode eine Schatten Kopie erstellen.</span><span class="sxs-lookup"><span data-stu-id="799b5-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="799b5-107">Wenn die anfordernde Person einen schattenkopiekontext angibt, der vom Anbieter nicht unterstützt wird, sollte der Anbieter nicht versuchen, die Schatten Kopie zu erstellen und mit dem *pbissupported* -Parameter in [**ivsshardwaresnapshotprovider:: arelunssupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) **false** zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="799b5-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="799b5-108">Wenn der Anforderer nicht explizit einen schattenkopieskontext angibt, sollte der Anbieter ein angemessenes Standardverhalten für die Erstellung von Schatten Kopien verwenden.</span><span class="sxs-lookup"><span data-stu-id="799b5-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="799b5-109">Hardware Anbieter, die San-RAID-Subsystemen zugeordnet sind, sollten austauschen-Schatten Kopien unterstützen, um eine Verschiebung zwischen Hosts in einem San zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="799b5-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="799b5-110">Hardware Anbieter, die auf mehreren Computern in einem SAN ausgeführt werden und das gleiche RAID-Subsystem verwalten, müssen nicht zwischen Anbietern in einem San koordiniert werden.</span><span class="sxs-lookup"><span data-stu-id="799b5-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="799b5-111">Der Koordinator behält jeden notwendigen Zustand bei.</span><span class="sxs-lookup"><span data-stu-id="799b5-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="799b5-112">Zwei Arten von Zuständen werden erkannt:</span><span class="sxs-lookup"><span data-stu-id="799b5-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="799b5-113">Der Status, der zur Unterstützung des Datenzugriffs auf die auf einer Hardware Schatten Kopie enthaltenen Volumes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="799b5-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="799b5-114">Dies schließt alle Tags eines Volumes als schreibgeschützt oder ausgeblendet ein.</span><span class="sxs-lookup"><span data-stu-id="799b5-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="799b5-115">Dieser Status muss sich auf der Hardware-LUN befinden und mit der LUN unterwegs sein.</span><span class="sxs-lookup"><span data-stu-id="799b5-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="799b5-116">Dieser Status wird über Start-und/oder Geräte Ermittlung hinweg beibehalten.</span><span class="sxs-lookup"><span data-stu-id="799b5-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="799b5-117">VSS verwaltet diesen Zustand für die Lebensdauer der Schatten Kopie.</span><span class="sxs-lookup"><span data-stu-id="799b5-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="799b5-118">Der Status, der erforderlich ist, um ein bestimmtes Volume als Teil eines schattenkopiesatzes zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="799b5-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="799b5-119">Dieser Status wird von VSS in Verbindung mit dem Anforderer beibehalten, der ursprünglich den Schattenkopiesatz erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="799b5-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="799b5-120">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="799b5-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="799b5-121">Der Erstellungs Vorgang für Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="799b5-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="799b5-122">Erforderliches Verhalten für Schattenkopieanbieter</span><span class="sxs-lookup"><span data-stu-id="799b5-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="799b5-123">Zustandsübergänge in schattenkopieanbietern</span><span class="sxs-lookup"><span data-stu-id="799b5-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="799b5-124">Fehlerbehandlung bei schattenkopieanbietern</span><span class="sxs-lookup"><span data-stu-id="799b5-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



