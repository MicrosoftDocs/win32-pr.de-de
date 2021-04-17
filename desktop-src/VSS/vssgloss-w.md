---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526267"
---
# <a name="w-volume-shadow-copy-service"></a><span data-ttu-id="07719-103">W (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="07719-103">W (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="07719-104">[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="07719-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="07719-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows-Datei Schutz**</span><span class="sxs-lookup"><span data-stu-id="07719-105"><span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="07719-106">Ein-Systemdienst, der spezielle Betriebssystemdateien schützt.</span><span class="sxs-lookup"><span data-stu-id="07719-106">A system service that protects special operating system files.</span></span> <span data-ttu-id="07719-107">Wenn eine dieser Dateien gelöscht oder überschrieben wird, ersetzt der Windows-Datei Schutz die Datei durch den ursprünglichen aus dem Cache.</span><span class="sxs-lookup"><span data-stu-id="07719-107">If one of these files is deleted or overwritten, Windows File Protection replaces the file with the original from its cache.</span></span>

</dd> <dt>

<span data-ttu-id="07719-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Maschine**</span><span class="sxs-lookup"><span data-stu-id="07719-108"><span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**writer**</span></span>
</dt> <dd>

<span data-ttu-id="07719-109">Eine Anwendung, die die e/a-Vorgänge mit VSS-schattenkopievorgängen (z. b. Sicherungen und Wiederherstellungen) koordiniert, sodass sich die auf dem schattenkopierten Volume enthaltenen Daten in einem konsistenten Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="07719-109">An application that coordinates its I/O operations with VSS shadow copy and shadow copy related operations (such as backups and restores) so that their data contained on the shadow copied volume is in a consistent state.</span></span>

<span data-ttu-id="07719-110">Zur Unterstützung dieser Koordination muss ein Writer eine Instanz einer Klasse implementieren, die von der abstrakten Basisklasse **CVssWriter** abgeleitet ist, um mit der VSS-Infrastruktur zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="07719-110">To support this coordination, a writer must implement an instance of a class derived from the abstract base class **CVssWriter** to communicate with the VSS infrastructure.</span></span> <span data-ttu-id="07719-111">Siehe auch [*Schatten Kopie*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="07719-111">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="07719-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Writer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="07719-112"><span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**writer class**</span></span>
</dt> <dd>

<span data-ttu-id="07719-113">Eine Globally Unique Identifier (GUID), die von einem Writer während der Initialisierung bereitgestellt wird, um anzugeben, dass er zu einem bestimmten Typ von Writern gehört.</span><span class="sxs-lookup"><span data-stu-id="07719-113">A globally unique identifier (GUID) supplied by a writer during initialization to indicate that it belongs to a given type of writers.</span></span> <span data-ttu-id="07719-114">Beispielsweise können mehrere Implementierungen eines Writers dieselbe Writer-Klassen-ID verwenden.</span><span class="sxs-lookup"><span data-stu-id="07719-114">For instance, multiple implementations of a writer could share the same writer class ID.</span></span>

<span data-ttu-id="07719-115">Writer derselben Klasse können von ihren Writer-Instanzen unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="07719-115">Writers of the same class may be distinguished by their writer instances.</span></span> <span data-ttu-id="07719-116">Es liegt an einem Anwendungsentwickler, Writer-Klassen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="07719-116">It is up to an application developer to specify writer classes.</span></span> <span data-ttu-id="07719-117">Siehe auch *Writer-Instanz*.</span><span class="sxs-lookup"><span data-stu-id="07719-117">See also *writer instance*.</span></span>

</dd> <dt>

<span data-ttu-id="07719-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**Writer-Instanz**</span><span class="sxs-lookup"><span data-stu-id="07719-118"><span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**writer instance**</span></span>
</dt> <dd>

<span data-ttu-id="07719-119">Eine Globally Unique Identifier (GUID), die von VSS für jeden Writer-Prozess bereitgestellt wird, der auf einem System ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07719-119">A globally unique identifier (GUID) supplied by VSS for each writer process running on a system.</span></span> <span data-ttu-id="07719-120">Bei jedem Start des Writers wird ein eindeutiger Wert für die Writer-Instanz generiert.</span><span class="sxs-lookup"><span data-stu-id="07719-120">A unique value for the writer instance is generated each time the writer starts.</span></span>

</dd> <dt>

<span data-ttu-id="07719-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer-Metadatendokument**</span><span class="sxs-lookup"><span data-stu-id="07719-121"><span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer Metadata Document**</span></span>
</dt> <dd>

<span data-ttu-id="07719-122">Ein XML-Dokument, das von einem Writer erstellt wurde (mithilfe der **ivsskreatewrite Metadata** -Schnittstelle), das Informationen über den Zustand und die Komponenten des Writers enthält.</span><span class="sxs-lookup"><span data-stu-id="07719-122">An XML document created by a writer (using the **IVssCreateWriterMetadata** interface) containing information about the writer's state and components.</span></span> <span data-ttu-id="07719-123">Ein Anforderer kann Writer-Metadatendokumente (mithilfe der **ivssexaminewrite Metadata** -Schnittstelle) Abfragen, wenn ein Wiederherstellungs-oder Sicherungs Vorgang durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07719-123">A requester can query Writer Metadata Documents (using the **IVssExamineWriterMetadata** interface) when performing a restore or backup operation.</span></span>

<span data-ttu-id="07719-124">Ein Writer-Metadatendokument enthält die Liste aller Komponenten eines Writers, von denen jedes möglicherweise an einer Sicherung beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="07719-124">A Writer Metadata Document contains the list of all of a writer's components, any one of which might participate in a backup.</span></span> <span data-ttu-id="07719-125">Dies unterscheidet sich vom Dokument mit den Sicherungs Komponenten der Anforderer, das nur die Komponenten enthält, die explizit für einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="07719-125">This differs from the requester's Backup Components Document, which contains only those components explicitly included for a backup or restore operation.</span></span>

<span data-ttu-id="07719-126">Nachdem das Writer-Metadatendokument erstellt wurde, sollte es als Schreib geschütztes Objekt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07719-126">Once constructed, the Writer Metadata Document should be viewed as a read-only object.</span></span> <span data-ttu-id="07719-127">Sie kann auf einem Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="07719-127">It can be saved to disk.</span></span> <span data-ttu-id="07719-128">Weitere Informationen finden Sie im [*Dokument zu Sicherungs Komponenten*](vssgloss-b.md), [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="07719-128">See also [*Backup Components Document*](vssgloss-b.md), [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> </dl>

 

 



