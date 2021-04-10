---
description: Objektspezifische ACEs werden für Verzeichnisdienst Objekte (DS) unterstützt. Ein Objekt spezifischer ACE enthält ein paar von GUIDs, die die Möglichkeiten erweitern, mit denen der ACE ein Objekt schützen kann.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: Objektspezifische ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40760e5cd06af97e93f74c6ff8daff89cd5962f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042607"
---
# <a name="object-specific-aces"></a><span data-ttu-id="dd563-104">Objektspezifische ACEs</span><span class="sxs-lookup"><span data-stu-id="dd563-104">Object-specific ACEs</span></span>

<span data-ttu-id="dd563-105">Objektspezifische [*ACEs*](/windows/desktop/SecGloss/a-gly) werden für Verzeichnisdienst Objekte (DS) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd563-105">Object-specific [*ACEs*](/windows/desktop/SecGloss/a-gly) are supported for directory service (DS) objects.</span></span> <span data-ttu-id="dd563-106">Ein Objekt spezifischer ACE enthält ein paar von GUIDs, die die Möglichkeiten erweitern, mit denen der ACE ein Objekt schützen kann.</span><span class="sxs-lookup"><span data-stu-id="dd563-106">An object-specific ACE contains a pair of GUIDs that expand the ways in which the ACE can protect an object.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd563-107">GUID</span><span class="sxs-lookup"><span data-stu-id="dd563-107">GUID</span></span></th>
<th><span data-ttu-id="dd563-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd563-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd563-109"><strong>ObjectType</strong></span><span class="sxs-lookup"><span data-stu-id="dd563-109"><strong>ObjectType</strong></span></span></td>
<td><span data-ttu-id="dd563-110">Gibt einen der folgenden an:</span><span class="sxs-lookup"><span data-stu-id="dd563-110">Identifies one of the following:</span></span>
<ul>
<li><span data-ttu-id="dd563-111">Ein Typ eines untergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd563-111">A type of child object.</span></span> <span data-ttu-id="dd563-112">Der ACE steuert das Recht, einen angegebenen Typ eines untergeordneten Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dd563-112">The ACE controls the right to create a specified type of child object.</span></span> <span data-ttu-id="dd563-113">Weitere Informationen finden Sie unter <a href="controlling-child-object-creation-in-c--.md">Steuern der Erstellung von untergeordneten Objekten in C++</a>.</span><span class="sxs-lookup"><span data-stu-id="dd563-113">For more information, see <a href="controlling-child-object-creation-in-c--.md">Controlling Child Object Creation in C++</a>.</span></span></li>
<li><span data-ttu-id="dd563-114">Ein Eigenschaften Satz oder eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dd563-114">A property set or property.</span></span> <span data-ttu-id="dd563-115">Der ACE steuert das Recht, die Eigenschaft oder den Eigenschaften Satz zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="dd563-115">The ACE controls the right to read or write the property or property set.</span></span> <span data-ttu-id="dd563-116">Weitere Informationen finden Sie unter <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts</a>.</span><span class="sxs-lookup"><span data-stu-id="dd563-116">For more information, see <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs to Control Access to an Object's Properties</a>.</span></span></li>
<li><span data-ttu-id="dd563-117">Ein erweitertes Recht.</span><span class="sxs-lookup"><span data-stu-id="dd563-117">An extended right.</span></span> <span data-ttu-id="dd563-118">Der ACE steuert das Recht, den Vorgang auszuführen, der mit dem erweiterten Recht verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dd563-118">The ACE controls the right to perform the operation associated with the extended right.</span></span></li>
<li><span data-ttu-id="dd563-119">Ein validierter Schreibvorgang.</span><span class="sxs-lookup"><span data-stu-id="dd563-119">A validated write.</span></span> <span data-ttu-id="dd563-120">Der ACE steuert das Recht, bestimmte Schreibvorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dd563-120">The ACE controls the right to perform certain write operations.</span></span> <span data-ttu-id="dd563-121">Diese validierten Schreibberechtigungen, die im ACL-Editor definiert und verfügbar gemacht wurden, stellen Berechtigungen für validierte Schreibvorgänge von Eigenschaften bereit, anstatt überprüfte Schreibberechtigungen auf niedriger Ebene eines beliebigen Werts in eine Eigenschaft, die mit einer Berechtigung zum Schreiben von Eigenschaften erteilt wird &quot; &quot; .</span><span class="sxs-lookup"><span data-stu-id="dd563-121">These validated write permissions, defined and exposed in the ACL Editor, provide permissions for validated writes of properties rather than unchecked low-level writes of any value to a property that is granted with a &quot;write property&quot; permission.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd563-122"><strong>Ereritedobjecttype</strong></span><span class="sxs-lookup"><span data-stu-id="dd563-122"><strong>InheritedObjectType</strong></span></span></td>
<td><span data-ttu-id="dd563-123">Gibt den Typ des untergeordneten Objekts an, das den ACE erben kann.</span><span class="sxs-lookup"><span data-stu-id="dd563-123">Indicates the type of child object that can inherit the ACE.</span></span> <span data-ttu-id="dd563-124">Die Vererbung wird auch von den Vererbungsflags in der <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>gesteuert sowie durch jeglichen Schutz vor Vererbung für die untergeordneten Objekte.</span><span class="sxs-lookup"><span data-stu-id="dd563-124">Inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>, as well as by any protection against inheritance placed on the child objects.</span></span> <span data-ttu-id="dd563-125">Weitere Informationen finden Sie unter <a href="ace-inheritance.md">ACE-Vererbung</a>.</span><span class="sxs-lookup"><span data-stu-id="dd563-125">For more information, see <a href="ace-inheritance.md">ACE Inheritance</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="dd563-126">Es werden drei Typen von Objekt spezifischen ACEs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd563-126">Three types of object-specific ACEs are supported.</span></span>

> [!Note]  
> <span data-ttu-id="dd563-127">System-Wecker-Objekt-ACEs werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dd563-127">System-alarm object ACEs are not currently supported.</span></span>

 



| <span data-ttu-id="dd563-128">type</span><span class="sxs-lookup"><span data-stu-id="dd563-128">Type</span></span>                      | <span data-ttu-id="dd563-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd563-129">Description</span></span>                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd563-130">Objekt-Ace "Zugriff verweigert"</span><span class="sxs-lookup"><span data-stu-id="dd563-130">Access-denied object ACE</span></span>  | <span data-ttu-id="dd563-131">Wird in einer DACL verwendet, um einem Vertrauens nehmer den Zugriff auf eine Eigenschaft oder Eigenschaft zu verweigern, die für das Objekt festgelegt wurde, oder um die ACE-Vererbung auf einen angegebenen Typ eines untergeordneten Objekts</span><span class="sxs-lookup"><span data-stu-id="dd563-131">Used in a DACL to deny a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="dd563-132">Verwendet die ACE-Struktur des [**Access \_ denied- \_ \_ Objekts**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="dd563-132">Uses the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) structure.</span></span>         |
| <span data-ttu-id="dd563-133">Zugriffs zulässiger Objekt-ACE</span><span class="sxs-lookup"><span data-stu-id="dd563-133">Access-allowed object ACE</span></span> | <span data-ttu-id="dd563-134">Wird in einer DACL verwendet, um einem Vertrauens nehmer den Zugriff auf eine Eigenschaft oder Eigenschaft zu ermöglichen, die für das Objekt festgelegt wurde, oder um die ACE-Vererbung auf einen angegebenen Typ von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="dd563-134">Used in a DACL to allow a trustee access to a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="dd563-135">Verwendet die ACE-Struktur des [**Access \_ Allowed- \_ \_ Objekts**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .</span><span class="sxs-lookup"><span data-stu-id="dd563-135">Uses the [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) structure.</span></span>      |
| <span data-ttu-id="dd563-136">System Überwachungs Objekt-ACE</span><span class="sxs-lookup"><span data-stu-id="dd563-136">System-audit object ACE</span></span>   | <span data-ttu-id="dd563-137">Wird in einer SACL zum Protokollieren der Versuche eines Vertrauens nehmers zum Zugreifen auf eine Eigenschaft oder Eigenschaft, die für das Objekt festgelegt wurde, oder zum Einschränken der ACE-Vererbung auf einen angegebenen Typ von untergeordneten Objekten verwendet</span><span class="sxs-lookup"><span data-stu-id="dd563-137">Used in a SACL to log a trustee's attempts to access a property or property set on the object, or to limit ACE inheritance to a specified type of child object.</span></span> <span data-ttu-id="dd563-138">Verwendet die [**\_ \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) -Struktur des System Überwachungs Objekts.</span><span class="sxs-lookup"><span data-stu-id="dd563-138">Uses the [**SYSTEM\_AUDIT\_OBJECT\_ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) structure.</span></span> |



 

<span data-ttu-id="dd563-139">Jede ACL, die einen Objekt spezifischen ACE enthält, muss die Revisions-ACL- \_ Revision verwenden \_ .</span><span class="sxs-lookup"><span data-stu-id="dd563-139">Any ACL that contains an object-specific ACE must use the revision ACL\_REVISION\_DS.</span></span>

 

 
