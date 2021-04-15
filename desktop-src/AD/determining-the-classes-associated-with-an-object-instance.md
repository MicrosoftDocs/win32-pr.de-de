---
title: Bestimmen der Klassen, die einer Objektinstanz zugeordnet sind
description: Jedes Objekt in Active Directory Domain Services verfügt über zwei Attribute, deren Werte die Hierarchie von Objektklassen identifizieren, für die das Objekt eine Instanz ist.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470932"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a><span data-ttu-id="56b42-103">Bestimmen der Klassen, die einer Objektinstanz zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="56b42-103">Determining the Classes Associated With an Object Instance</span></span>

<span data-ttu-id="56b42-104">Jedes Objekt in Active Directory Domain Services verfügt über zwei Attribute, deren Werte die Hierarchie von Objektklassen identifizieren, für die das Objekt eine Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="56b42-104">Every object in Active Directory Domain Services has two attributes whose values identify the hierarchy of object classes of which the object is an instance.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56b42-105">Attribut</span><span class="sxs-lookup"><span data-stu-id="56b42-105">Attribute</span></span></th>
<th><span data-ttu-id="56b42-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="56b42-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="56b42-107"><strong>StructuralObjectClass</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-107"><strong>structuralObjectClass</strong></span></span></td>
<td><span data-ttu-id="56b42-108">Identifiziert die strukturellen und abstrakten Klassen, für die das-Objekt eine-Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="56b42-108">Identifies the structural and abstract classes of which the object is an instance.</span></span> <span data-ttu-id="56b42-109">Beispielsweise können die Werte für ein Benutzerobjekt wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="56b42-109">For example, the values for a user object can be:</span></span>
<ul>
<li><span data-ttu-id="56b42-110"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-110"><strong>top</strong></span></span></li>
<li><span data-ttu-id="56b42-111"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-111"><strong>person</strong></span></span></li>
<li><span data-ttu-id="56b42-112"><strong>OrganizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-112"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="56b42-113"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-113"><strong>user</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="56b42-114"><strong>objectClass</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-114"><strong>objectClass</strong></span></span></td>
<td><span data-ttu-id="56b42-115">Identifiziert die Klassen, die in <strong>StructuralObjectClass</strong>enthalten sind, sowie alle neben Klassen, die dynamisch angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="56b42-115">Identifies the classes included in <strong>structuralObjectClass</strong>, plus any auxiliary classes that are dynamically attached.</span></span> <span data-ttu-id="56b42-116">Wenn z. b. eine &quot; Vehicle- &quot; Hilfsklasse an ein Benutzerobjekt angefügt ist, können die folgenden Werte lauten:</span><span class="sxs-lookup"><span data-stu-id="56b42-116">For example, if a &quot;vehicle&quot; auxiliary class is attached to a user object, the values can be:</span></span>
<ul>
<li><span data-ttu-id="56b42-117"><strong>top</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-117"><strong>top</strong></span></span></li>
<li><span data-ttu-id="56b42-118"><strong>Elektro</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-118"><strong>vehicle</strong></span></span></li>
<li><span data-ttu-id="56b42-119"><strong>person</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-119"><strong>person</strong></span></span></li>
<li><span data-ttu-id="56b42-120"><strong>OrganizationalPerson</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-120"><strong>organizationalPerson</strong></span></span></li>
<li><span data-ttu-id="56b42-121"><strong>user</strong></span><span class="sxs-lookup"><span data-stu-id="56b42-121"><strong>user</strong></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="56b42-122">Beachten Sie, dass keines dieser Attribute Erweiterungs Klassen enthält, die statisch mit den Objektklassen verknüpft sind, für die das Objekt eine Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="56b42-122">Be aware that neither of these attributes include auxiliary classes that are statically linked with the object classes of which the object is an instance.</span></span> <span data-ttu-id="56b42-123">Beispielsweise ist die **SecurityPrincipal** -Erweiterungs Klasse statisch mit der **User** -Klasse verknüpft, da Sie in den **systemAuxiliaryClass** -Werten des User **classSchema** -Objekts enthalten ist. Sie ist nicht in den Attributen " **objectClass** " oder " **StructuralObjectClass** " von Instanzen der Benutzerklasse enthalten.</span><span class="sxs-lookup"><span data-stu-id="56b42-123">For example, the **securityPrincipal** auxiliary class is statically linked with the **user** class because it is included in the **systemAuxiliaryClass** values of the user **classSchema** object; it is not included in either the **objectClass** or **structuralObjectClass** attributes of instances of the user class.</span></span>

 

 




