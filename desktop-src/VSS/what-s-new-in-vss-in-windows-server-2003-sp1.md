---
description: 'Die folgende Liste gibt Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1) an:'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Neues in VSS unter Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485019"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="d0e6f-103">Neues in VSS unter Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="d0e6f-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="d0e6f-104">Die folgende Liste gibt Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1) an:</span><span class="sxs-lookup"><span data-stu-id="d0e6f-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="d0e6f-105">Automatische Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="d0e6f-105">Auto-recovery</span></span>

<span data-ttu-id="d0e6f-106">Die [*Automatische Wiederherstellung*](vssgloss-a.md) ermöglicht Writer eine Zeit zum Aktualisieren von Komponenten in einer Schatten Kopie, bevor die Schatten Kopie dauerhaft in schreibgeschützt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d0e6f-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="d0e6f-107">Beispielsweise muss eine Datenbank möglicherweise unvollständige Transaktionen für alle Schatten Kopien zurücksetzen (der datenbankwriter würde das **VSS CF- \_ \_ \_ sicherungswiederherstellungsflag** für die Datenbankkomponenten festlegen).</span><span class="sxs-lookup"><span data-stu-id="d0e6f-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="d0e6f-108">Die automatische Wiederherstellung, die von der anfordernden Person initiiert wurde, ermöglicht eine differenzierte Wiederherstellung (z. b. das Wiederherstellen einer Tabelle in einer Datenbank oder eines Ordners auf einem e-Mail-Server) oder das Rollback zur Unterstützung von Data Mining zur Durchführung von Analysen, die für einen Produktions **Server zu langsam \_ \_ \_ \_** sind. Die automatische Wiederherstellung ist nicht mit transportfähigen Schatten Kopien kompatibel, aber die gleiche Funktionalität wird durch die Verwendung der [schnellen Wiederherstellung mithilfe von austauschen schattenkopierten Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0e6f-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="d0e6f-109">Die folgenden Programmier Elemente haben Änderungen zur Unterstützung der automatischen Wiederherstellung:</span><span class="sxs-lookup"><span data-stu-id="d0e6f-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="d0e6f-110">Klassen Methoden</span><span class="sxs-lookup"><span data-stu-id="d0e6f-110">Class methods</span></span>

-   [<span data-ttu-id="d0e6f-111">**CVssWriter:: geznapshotdevicename**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="d0e6f-112">**CVssWriter:: OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="d0e6f-113">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="d0e6f-113">Enumerations</span></span>

-   [<span data-ttu-id="d0e6f-114">**VSS \_ - \_ Komponentenflags**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="d0e6f-115">**\_VSS \_ - \_ volumesnapshotattribute \_**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="d0e6f-116">Schnittstellen Methoden</span><span class="sxs-lookup"><span data-stu-id="d0e6f-116">Interface methods</span></span>

-   [<span data-ttu-id="d0e6f-117">**Ivssproviderkreatesnapshotset::P Verfeinerungs Momentaufnahmen**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="d0e6f-118">**Ivssproviderkreatesnapshotset::P ostfinalcommitsnapshot**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="d0e6f-119">Vollständige Unterstützung für transportable-Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="d0e6f-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="d0e6f-120">Transportable-Schatten Kopien werden in allen Editionen von Windows Server 2003 mit SP1 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0e6f-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="d0e6f-121">Weitere Informationen finden Sie unter [importieren transportable-Schattenkopievolumes](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="d0e6f-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="d0e6f-122">Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes</span><span class="sxs-lookup"><span data-stu-id="d0e6f-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="d0e6f-123">Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes</span><span class="sxs-lookup"><span data-stu-id="d0e6f-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="d0e6f-124">Schatten Kopie-Speicherbereichs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d0e6f-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="d0e6f-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="d0e6f-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



