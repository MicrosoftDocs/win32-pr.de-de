---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751553"
---
# <a name="c-volume-shadow-copy-service"></a><span data-ttu-id="0cdaf-103">C (Volumeschattenkopie-Dienst)</span><span class="sxs-lookup"><span data-stu-id="0cdaf-103">C (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="0cdaf-104">[a](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="0cdaf-104">[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0cdaf-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**Zertifizierungsstelle**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-105"><span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**certification authority**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-106">Eine Entität, die zur Ausstellung von Zertifikaten anvertraut ist, die behaupten, dass der Empfänger, der Computer oder die Organisation, der das Zertifikat anfordert, die Bedingungen einer festgelegten</span><span class="sxs-lookup"><span data-stu-id="0cdaf-106">An entity entrusted to issue certificates asserting that the recipient individual, machine, or organization requesting the certificate fulfills the conditions of an established policy.</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**vom Client zugänglichen Schatten Kopie**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-107"><span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**client-accessible shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-108">Eine Schatten Kopie, die vom Systemanbieter zur Unterstützung von Schattenkopien für freigegebene Ordner und anderen Roll Back Mechanismen erstellt wird, die es Clients ermöglichen, alte Versionen von Dateien anzuzeigen und Fehler rückgängig zu machen, ohne eine vollständige Wiederherstellung zu erfordern</span><span class="sxs-lookup"><span data-stu-id="0cdaf-108">A shadow copy created by the system provider to support Shadow Copies for Shared Folders and other rollback mechanisms, which allow clients to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="0cdaf-109">Eine vom Client zugängliche Schatten Kopie wird mithilfe des **VSS \_ ctx- \_ Clients \_** erstellt, auf den zugegriffen werden kann. der [**\_ VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) -momentaufnahmenaufzählungs Kontext</span><span class="sxs-lookup"><span data-stu-id="0cdaf-109">A client-accessible shadow copy is created using the **VSS\_CTX\_CLIENT\_ACCESSIBLE** value of the [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) enumeration.</span></span> <span data-ttu-id="0cdaf-110">Außerdem wird der barrierefreie VSS-Volsnap attr-Client, auf den zugegriffen werden kann, \_ \_ \_ \_ die Enumeration der [**\_ VSS-Volumesnapshot- \_ \_ \_ Attribute**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) automatisch für die vom Client zugänglichen Schatten Kopien festlegen.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-110">In addition, the VSS\_VOLSNAP\_ATTR\_CLIENT\_ACCESSIBLE value of the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration is set automatically for client-accessible shadow copies.</span></span> <span data-ttu-id="0cdaf-111">Siehe auch [*Schattenkopien für freigegebene Ordner*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="0cdaf-111">See also [*Shadow Copies for Shared Folders*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Zulieferern**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-112"><span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-113">Eine Gruppe von Dateien, die von einem Writer definiert werden und bei Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-113">A group of files, defined by a writer, that must be handled as a unit during backup and restore operations.</span></span> <span data-ttu-id="0cdaf-114">Siehe auch [*Datenbankkomponente*](vssgloss-d.md), [*Dateigruppen Komponente*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="0cdaf-114">See also [*database component*](vssgloss-d.md), [*file group component*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**Komponenten Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-115"><span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**component dependency**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-116">Eine Situation, in der eine von einem Writer verwaltete Komponente (und der von ihr festgelegte Komponenten Satz) unabhängig von den von anderen Writern verwalteten Komponenten nicht gesichert oder wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-116">A situation in which a component (and the component set it defines) managed by one writer cannot be backed up or restore independently of components managed by others writers.</span></span> <span data-ttu-id="0cdaf-117">Eine Abhängigkeit gibt keine bevorzugte Reihenfolge zwischen der Komponente und den dokumentierten Abhängigkeiten und den Komponenten an, von denen Sie abhängt: eine Abhängigkeit gibt lediglich an, dass die Komponente und die Komponenten, von denen Sie abhängt, immer gemeinsam gesichert oder wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-117">A dependency does not indicate an order of preference between the component with the documented dependencies and the components it depends on: a dependency merely indicates that the component and the components it depends on must always be backed up or restored together.</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**Komponenten Modus**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-118"><span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**component mode**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-119">Ein Modus, in dem ein Sicherungs-oder Wiederherstellungs Vorgang die Komponenten Informationen eines Writers nutzt.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-119">A mode in which a backup or restore operation makes use of a writer's component information.</span></span> <span data-ttu-id="0cdaf-120">Siehe auch [*auswählbare Komponente*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="0cdaf-120">See also [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**Komponenten Satz**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-121"><span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**component set**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-122">Eine Gruppe von Komponenten, bei der mindestens eine auswählbare Komponente (für die Sicherungs-oder Wiederherstellungs Komponente) und eine Reihe nicht auswählbarer Komponenten in einer Hierarchie durch ihre logischen Pfade organisiert sind.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-122">A group of components with at least one selectable (for either backup or restore) component and a number of nonselectable components organized in a hierarchy by their logical paths.</span></span> <span data-ttu-id="0cdaf-123">Die implizite Teilnahme an einem Sicherungs-oder Wiederherstellungs Vorgang hängt von der expliziten Einbindung der auswählbaren Komponente der obersten Ebene ab.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-123">The implicit participation in a backup or restore operation depends on the explicit inclusion of the top-level selectable component.</span></span> <span data-ttu-id="0cdaf-124">Im Dokument mit den Sicherungs Komponenten sind nur die Komponenten Informationen dieser auswählbaren Komponente enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-124">Only the component information of this selectable component is included in the Backup Components Document.</span></span> <span data-ttu-id="0cdaf-125">Ein Komponenten Satz kann auswählbare und nicht auswählbare unter Komponenten enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-125">A component set may include selectable and nonselectable subcomponents.</span></span> <span data-ttu-id="0cdaf-126">Siehe auch [*logischer Pfad*](vssgloss-l.md), [*auswählbare Komponente*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="0cdaf-126">See also [*logical path*](vssgloss-l.md), [*selectable component*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**Schatten Kopie beim Kopieren bei Schreibvorgang**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-127"><span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copy-on-write shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-128">Eine Schatten Kopie, die erstellt wird, indem nur die Unterschiede vom ursprünglichen Volume gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-128">A shadow copy created by saving only the differences from the original volume.</span></span>

</dd> <dt>

<span data-ttu-id="0cdaf-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**Status "Absturz konsistent"**</span><span class="sxs-lookup"><span data-stu-id="0cdaf-129"><span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**crash consistent state**</span></span>
</dt> <dd>

<span data-ttu-id="0cdaf-130">Der Status der Datenträger, die mit dem nach einem schwerwiegenden Fehler zu finden sind, der das System plötzlich heruntergefahren hat.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-130">The state of disks equivalent to what would be found following a catastrophic failure that abruptly shuts down the system.</span></span> <span data-ttu-id="0cdaf-131">Eine Wiederherstellung von einem solchen Schattenkopiesatz wäre äquivalent zu einem Neustart nach einem abrupten Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-131">A restore from such a shadow copy set would be equivalent to a reboot following an abrupt shutdown.</span></span> <span data-ttu-id="0cdaf-132">Dies ist der Standardzustand von Daten, die ohne Unterstützung von Writern als Schatten kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0cdaf-132">This is the default state of data that has been shadow copied without the support of writers.</span></span>

</dd> </dl>

 

 



