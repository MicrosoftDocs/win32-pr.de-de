---
description: Wichtig für die Organisation der zu sichernden oder wiederherzustellenden Dateien ist das Konzept einer Komponente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: VSS-Metadatenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372823"
---
# <a name="vss-metadata-components"></a><span data-ttu-id="0682d-103">VSS-Metadatenkomponenten</span><span class="sxs-lookup"><span data-stu-id="0682d-103">VSS Metadata Components</span></span>

<span data-ttu-id="0682d-104">Wichtig für die Organisation der zu sichernden oder wiederherzustellenden Dateien ist das Konzept einer [*Komponente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="0682d-104">Critical to organizing which files of which writer are to be backed up or restored is the concept of a [*component*](vssgloss-c.md).</span></span>

<span data-ttu-id="0682d-105">Mit-Komponenten kann ein Writer einem Sicherungs Modul zeigen, wie seine Dateien organisiert werden sollen, Abhängigkeiten zwischen Dateien und welchen Datentyp diese Dateien enthalten können.</span><span class="sxs-lookup"><span data-stu-id="0682d-105">Components allow a writer to indicate to a backup engine how its files are to be organized, dependencies between files, and what type of data those files can contain.</span></span> <span data-ttu-id="0682d-106">Dadurch kann eine Sicherungs-Engine entscheiden, wie Dateien für maximale Effizienz gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0682d-106">This allows a backup engine to decide how to store files for maximum efficiency.</span></span>

<span data-ttu-id="0682d-107">Außerdem verwenden VSS-basierte Anwendungen Komponenten als Bausteine für Ihre Metadaten und das Medium für die Kommunikation zwischen Writer und Anforderer.</span><span class="sxs-lookup"><span data-stu-id="0682d-107">In addition, VSS-based applications use components as the building blocks for their metadata and the medium for writer/requester communication.</span></span>

<span data-ttu-id="0682d-108">Writer und Anforderer speichert Informationen zu Komponenten separat – im Writer-Metadatendokument und in den Sicherungs Komponenten Dokumenten bzw. –, und die Informationen unterscheiden sich in den einzelnen Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="0682d-108">Writers and requesters store information about components separately—in the Writer Metadata Document and the Backup Components Document, respectively—and the information differs in each representation.</span></span>

<span data-ttu-id="0682d-109">Zu den Komponenten Informationen in Writer-Metadatendokumenten zählen die folgenden:</span><span class="sxs-lookup"><span data-stu-id="0682d-109">Component information in Writer Metadata Documents includes the following:</span></span>

-   <span data-ttu-id="0682d-110">Informationen aus nur einem Writer in jedem Dokument</span><span class="sxs-lookup"><span data-stu-id="0682d-110">Information from only one writer in each document</span></span>
-   <span data-ttu-id="0682d-111">Alle diese Writer-Komponenten, unabhängig davon, ob Sie [*explizit eingeschlossen*](vssgloss-e.md) werden können oder [*implizit*](vssgloss-i.md) in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden müssen</span><span class="sxs-lookup"><span data-stu-id="0682d-111">All of that writer's components, whether they can be [*explicitly included*](vssgloss-e.md) or must be [*implicitly included*](vssgloss-i.md) in a backup or restore operation</span></span>
-   <span data-ttu-id="0682d-112">[*Logische Pfad*](vssgloss-l.md) Informationen, die verwendet werden, um eine wählbare für Sicherungs Komponente mit bestimmten nicht auswählbaren Sicherungs Komponenten zuzuordnen und so einen Komponenten Satz zu bilden.</span><span class="sxs-lookup"><span data-stu-id="0682d-112">[*Logical path*](vssgloss-l.md) information used to associate a selectable for backup component with particular nonselectable for backup components, thus forming a component set</span></span>
-   <span data-ttu-id="0682d-113">Die [*Datei Satz*](vssgloss-f.md) Informationen – Pfad, Datei Angabe und Rekursions Flag – werden für jede Komponente verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0682d-113">The [*file set*](vssgloss-f.md) information—path, file specification, and recursion flag—managed for each component</span></span>

<span data-ttu-id="0682d-114">Writer-Metadatendokumente enthalten außerdem Metadateninformationen auf Schreib Ebene, z. b. Wiederherstellungsmethoden und Alternative Speicherort Zuordnungen für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="0682d-114">Writer Metadata Documents also contain writer-level metadata information, such as restore methods and alternate location mappings for restore.</span></span> <span data-ttu-id="0682d-115">Writer-Metadatendokumente sind schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0682d-115">Writer Metadata Documents are read-only.</span></span> <span data-ttu-id="0682d-116">Die Schnittstelle zur Untersuchung dieser Informationen ist [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span><span class="sxs-lookup"><span data-stu-id="0682d-116">The interface for examining this information is [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span></span>

<span data-ttu-id="0682d-117">Die Komponenten Informationen in den Dokumenten der Sicherungs Komponenten umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0682d-117">Component information in Backup Components Documents includes the following:</span></span>

-   <span data-ttu-id="0682d-118">Nur Informationen zu explizit enthaltenen Komponenten</span><span class="sxs-lookup"><span data-stu-id="0682d-118">Only information on explicitly included components</span></span>
-   <span data-ttu-id="0682d-119">Metadateninformationen auf Writer-Ebene, z. b. Alternative Speicherort Zuordnungen und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="0682d-119">Writer-level metadata information, such as alternate location mappings and restore</span></span>
-   <span data-ttu-id="0682d-120">Zustandsinformationen, die einen Sicherungs-oder Wiederherstellungs Vorgang beschreiben</span><span class="sxs-lookup"><span data-stu-id="0682d-120">State information describing a backup or restore operation</span></span>

<span data-ttu-id="0682d-121">Sicherungs Komponenten Dokumente enthalten keine Informationen über die [*Dateigruppen*](vssgloss-f.md)der Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0682d-121">Backup Component Documents do not contain information on components' [*file sets*](vssgloss-f.md).</span></span> <span data-ttu-id="0682d-122">Sicherungs Komponenten Dokumente sind nicht schreibgeschützt und können vom Writer geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0682d-122">Backup Component Documents are not read-only and can be modified by the writer.</span></span> <span data-ttu-id="0682d-123">Die Schnittstelle für den Zugriff auf diese Informationen ist [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span><span class="sxs-lookup"><span data-stu-id="0682d-123">The interface for accessing this information is [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span></span>

<span data-ttu-id="0682d-124">Der Lebenszyklus und die Beziehung zwischen den beiden Ausdrücken einer Komponente können wie folgt interpretiert werden:</span><span class="sxs-lookup"><span data-stu-id="0682d-124">The life cycle and relationship between the two expressions of a component can be understood as follows:</span></span>

-   <span data-ttu-id="0682d-125">Writer sind für die anfänglichen Definitionen von Komponenten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="0682d-125">Writers are responsible for the initial definitions of components.</span></span>
-   <span data-ttu-id="0682d-126">Ein Anforderer überprüft die Metadaten aller Writer und deren Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0682d-126">A requester examines the metadata of all writers and their components.</span></span>
-   <span data-ttu-id="0682d-127">Aus der selekabilität und den logischen Pfadinformationen der Komponenten bestimmt ein Anforderer, welche Komponenten explizit eingeschlossen werden müssen. diese sind möglicherweise explizit eingeschlossen, wodurch Komponenten Sätze definiert werden und die Mitglieder von Komponenten Sätzen sind.</span><span class="sxs-lookup"><span data-stu-id="0682d-127">From components' selectability and logical path information, a requester determines which components must be explicitly included, which may be explicitly included, which define component sets, and which are members of component sets.</span></span>
-   <span data-ttu-id="0682d-128">Ein Anforderer fügt die Komponenten hinzu, die eine explizite Einbindung erfordern, und umfasst implizit unter Komponenten in [*Komponenten Sätze*](/windows) (deren Informationen sich nicht im Dokument mit den Sicherungs Komponenten befinden).</span><span class="sxs-lookup"><span data-stu-id="0682d-128">A requester adds those components that require explicit inclusion, and implicitly includes subcomponents in [*component sets*](/windows) (whose information is not in the Backup Components Document).</span></span>
-   <span data-ttu-id="0682d-129">Bei der Ereignis Behandlung können Writer und Anforderer die im Dokument der Sicherungs Komponenten gespeicherten Komponenten Informationen ändern und untersuchen, um deren Aktivität zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="0682d-129">When handling events, writers and requesters may modify and examine the component information stored in the Backup Components Document to coordinate their activity.</span></span>

<span data-ttu-id="0682d-130">Zum ordnungsgemäßen Ausführen von Sicherungs-und Wiederherstellungs Vorgängen sind sowohl die Writer-als auch die RequestVersion-Komponenten Informationen erforderlich, und beide müssen mit allen gesicherten Daten gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="0682d-130">Both the writer and the requester versions component information are required to properly execute backup and restore operations, and both must be stored with any backed-up data:</span></span>

-   [<span data-ttu-id="0682d-131">Komponenten Typen</span><span class="sxs-lookup"><span data-stu-id="0682d-131">Component Types</span></span>](component-types.md)
-   [<span data-ttu-id="0682d-132">Definition von Komponenten durch Writer</span><span class="sxs-lookup"><span data-stu-id="0682d-132">Definition of Components by Writers</span></span>](definition-of-components-by-writers.md)
-   [<span data-ttu-id="0682d-133">Verwendung von Komponenten durch den Anforderer</span><span class="sxs-lookup"><span data-stu-id="0682d-133">Use of Components by the Requester</span></span>](use-of-components-by-the-requestor.md)

 

 
