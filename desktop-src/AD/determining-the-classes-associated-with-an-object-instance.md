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
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Bestimmen der Klassen, die einer Objektinstanz zugeordnet sind

Jedes Objekt in Active Directory Domain Services verfügt über zwei Attribute, deren Werte die Hierarchie von Objektklassen identifizieren, für die das Objekt eine Instanz ist.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>StructuralObjectClass</strong></td>
<td>Identifiziert die strukturellen und abstrakten Klassen, für die das-Objekt eine-Instanz ist. Beispielsweise können die Werte für ein Benutzerobjekt wie folgt lauten:
<ul>
<li><strong>top</strong></li>
<li><strong>person</strong></li>
<li><strong>OrganizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifiziert die Klassen, die in <strong>StructuralObjectClass</strong>enthalten sind, sowie alle neben Klassen, die dynamisch angefügt werden. Wenn z. b. eine &quot; Vehicle- &quot; Hilfsklasse an ein Benutzerobjekt angefügt ist, können die folgenden Werte lauten:
<ul>
<li><strong>top</strong></li>
<li><strong>Elektro</strong></li>
<li><strong>person</strong></li>
<li><strong>OrganizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Beachten Sie, dass keines dieser Attribute Erweiterungs Klassen enthält, die statisch mit den Objektklassen verknüpft sind, für die das Objekt eine Instanz ist. Beispielsweise ist die **SecurityPrincipal** -Erweiterungs Klasse statisch mit der **User** -Klasse verknüpft, da Sie in den **systemAuxiliaryClass** -Werten des User **classSchema** -Objekts enthalten ist. Sie ist nicht in den Attributen " **objectClass** " oder " **StructuralObjectClass** " von Instanzen der Benutzerklasse enthalten.

 

 




