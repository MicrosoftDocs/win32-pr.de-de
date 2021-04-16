---
description: Requesters steuern die Features einer Schatten Kopie durch Festlegen Ihres Kontexts. Dieser Kontext gibt an, ob die Schatten Kopie den aktuellen Vorgang und den Grad der Koordination von Writer und Anbietern überstehen wird.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Kontext Konfigurationen für Schatten Kopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528697"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="481e7-104">Kontext Konfigurationen für Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="481e7-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="481e7-105">Requesters steuern die Features einer Schatten Kopie durch Festlegen Ihres Kontexts.</span><span class="sxs-lookup"><span data-stu-id="481e7-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="481e7-106">Dieser Kontext gibt an, ob die Schatten Kopie den aktuellen Vorgang und den Grad der Koordination von Writer und Anbietern überstehen wird.</span><span class="sxs-lookup"><span data-stu-id="481e7-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="481e7-107">Persistenz und Schatten Kopier Kontext</span><span class="sxs-lookup"><span data-stu-id="481e7-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="481e7-108">Eine Schatten Kopie ist möglicherweise [*persistent*](vssgloss-p.md)– das heißt, die Schatten Kopie wird nach der Beendigung eines Sicherungs Vorgangs oder der Freigabe eines [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) -Objekts nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="481e7-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="481e7-109">Persistente Schatten Kopien erfordern [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Kontexte des **VSS \_ ctx- \_ Clients \_**, auf die zugegriffen werden kann, **VSS \_ ctx- \_ App- \_ Rollback** oder **VSS \_ ctx \_ NAS- \_ Rollback**.</span><span class="sxs-lookup"><span data-stu-id="481e7-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="481e7-110">Persistente Schatten Kopien können nur für NTFS-Volumes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="481e7-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="481e7-111">Nicht persistente Schatten Kopien werden mit Kontexten der **VSS \_ ctx- \_ Sicherung** oder der **VSS \_ ctx- \_ Datei \_ Freigabe \_ Sicherung** erstellt.</span><span class="sxs-lookup"><span data-stu-id="481e7-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="481e7-112">Nicht persistente Schatten Kopien können für NTFS-und nicht-NTFS-Volumes erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="481e7-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="481e7-113">Writer-Teilnahme und Schatten Kopien</span><span class="sxs-lookup"><span data-stu-id="481e7-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="481e7-114">Ein schattenkopieskontext kann als Einbeziehung von Writern oder nicht zum Einschließen von Writern klassifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="481e7-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="481e7-115">Schattenkopiekontexte, die Writer in ihrer Erstellung einbeziehen, umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="481e7-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="481e7-116">**VSS- \_ ctx- \_ App- \_ Rollback**</span><span class="sxs-lookup"><span data-stu-id="481e7-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="481e7-117">**VSS \_ ctx- \_ Sicherung**</span><span class="sxs-lookup"><span data-stu-id="481e7-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="481e7-118">**VSS \_ ctx- \_ Client \_ barrierefreie \_ Writer**</span><span class="sxs-lookup"><span data-stu-id="481e7-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="481e7-119">Zu den Entwicklern, die in ihrer Erstellung keine Writer einschließen, gehören:</span><span class="sxs-lookup"><span data-stu-id="481e7-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="481e7-120">**verfügbarer VSS- \_ ctx- \_ Client \_**</span><span class="sxs-lookup"><span data-stu-id="481e7-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="481e7-121">**VSS \_ ctx- \_ Datei \_ Freigabe \_ Sicherung**</span><span class="sxs-lookup"><span data-stu-id="481e7-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="481e7-122">**VSS- \_ ctx- \_ NAS- \_ Rollback**</span><span class="sxs-lookup"><span data-stu-id="481e7-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="481e7-123">Ein Kontext kann mit beiden Arten von Schatten Kopien verwendet werden, kann jedoch nicht zum Erstellen einer Schatten Kopie verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="481e7-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="481e7-124">**VSS \_ ctx \_ alle**</span><span class="sxs-lookup"><span data-stu-id="481e7-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="481e7-125">Das Erstellen einer Schatten Kopie mit einem Kontext von **VSS \_ ctx \_ all** (mithilfe von [**IVssBackupComponents:: startnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) und [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="481e7-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="481e7-126">Bei Vorgängen, die einen Kontext von **VSS \_ ctx \_** unterstützen, handelt es sich dabei um administrative Vorgänge [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: breaksnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)und [**IVssBackupComponents:: exposesnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="481e7-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="481e7-127">Abrufen von Schattenkopieinformationen</span><span class="sxs-lookup"><span data-stu-id="481e7-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="481e7-128">Wenn ein Anforderer die identifizierende GUID einer Schatten Kopie (seine **VSS- \_ ID**) kennt, kann er Informationen über den Kontext einer bestimmten Schatten Kopie (identifiziert durch seine **VSS- \_ ID**) abrufen, indem die von einem Aufrufen von [**IVssBackupComponents:: gebrannapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)zurückgegebene VSS-momentaufnahmenstruktur entpackt wird. [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)</span><span class="sxs-lookup"><span data-stu-id="481e7-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="481e7-129">Zum Abrufen von Kontextinformationen über alle Schatten Kopien eines Systems ein Anforderer untersucht **das m \_ lsnapshotattributes** -Element des **obj. Snap** -Members der [**VSS- \_ Objekt \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (bei der es sich um eine [**VSS-momentaufnahmenstruktur \_ handelt \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ), die mithilfe von [**ivssenuwbject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) abgerufen wurde, um die Liste der Objekte zu durchlaufen, die durch einen-Befehl von [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)</span><span class="sxs-lookup"><span data-stu-id="481e7-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



