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
# <a name="object-specific-aces"></a>Objektspezifische ACEs

Objektspezifische [*ACEs*](/windows/desktop/SecGloss/a-gly) werden für Verzeichnisdienst Objekte (DS) unterstützt. Ein Objekt spezifischer ACE enthält ein paar von GUIDs, die die Möglichkeiten erweitern, mit denen der ACE ein Objekt schützen kann.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ObjectType</strong></td>
<td>Gibt einen der folgenden an:
<ul>
<li>Ein Typ eines untergeordneten Objekts. Der ACE steuert das Recht, einen angegebenen Typ eines untergeordneten Objekts zu erstellen. Weitere Informationen finden Sie unter <a href="controlling-child-object-creation-in-c--.md">Steuern der Erstellung von untergeordneten Objekten in C++</a>.</li>
<li>Ein Eigenschaften Satz oder eine Eigenschaft. Der ACE steuert das Recht, die Eigenschaft oder den Eigenschaften Satz zu lesen oder zu schreiben. Weitere Informationen finden Sie unter <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts</a>.</li>
<li>Ein erweitertes Recht. Der ACE steuert das Recht, den Vorgang auszuführen, der mit dem erweiterten Recht verknüpft ist.</li>
<li>Ein validierter Schreibvorgang. Der ACE steuert das Recht, bestimmte Schreibvorgänge auszuführen. Diese validierten Schreibberechtigungen, die im ACL-Editor definiert und verfügbar gemacht wurden, stellen Berechtigungen für validierte Schreibvorgänge von Eigenschaften bereit, anstatt überprüfte Schreibberechtigungen auf niedriger Ebene eines beliebigen Werts in eine Eigenschaft, die mit einer Berechtigung zum Schreiben von Eigenschaften erteilt wird &quot; &quot; .</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Ereritedobjecttype</strong></td>
<td>Gibt den Typ des untergeordneten Objekts an, das den ACE erben kann. Die Vererbung wird auch von den Vererbungsflags in der <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong>ACE_HEADER</strong></a>gesteuert sowie durch jeglichen Schutz vor Vererbung für die untergeordneten Objekte. Weitere Informationen finden Sie unter <a href="ace-inheritance.md">ACE-Vererbung</a>.</td>
</tr>
</tbody>
</table>



 

Es werden drei Typen von Objekt spezifischen ACEs unterstützt.

> [!Note]  
> System-Wecker-Objekt-ACEs werden zurzeit nicht unterstützt.

 



| type                      | BESCHREIBUNG                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Objekt-Ace "Zugriff verweigert"  | Wird in einer DACL verwendet, um einem Vertrauens nehmer den Zugriff auf eine Eigenschaft oder Eigenschaft zu verweigern, die für das Objekt festgelegt wurde, oder um die ACE-Vererbung auf einen angegebenen Typ eines untergeordneten Objekts Verwendet die ACE-Struktur des [**Access \_ denied- \_ \_ Objekts**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace) .         |
| Zugriffs zulässiger Objekt-ACE | Wird in einer DACL verwendet, um einem Vertrauens nehmer den Zugriff auf eine Eigenschaft oder Eigenschaft zu ermöglichen, die für das Objekt festgelegt wurde, oder um die ACE-Vererbung auf einen angegebenen Typ von untergeordneten Objekten Verwendet die ACE-Struktur des [**Access \_ Allowed- \_ \_ Objekts**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace) .      |
| System Überwachungs Objekt-ACE   | Wird in einer SACL zum Protokollieren der Versuche eines Vertrauens nehmers zum Zugreifen auf eine Eigenschaft oder Eigenschaft, die für das Objekt festgelegt wurde, oder zum Einschränken der ACE-Vererbung auf einen angegebenen Typ von untergeordneten Objekten verwendet Verwendet die [**\_ \_ \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) -Struktur des System Überwachungs Objekts. |



 

Jede ACL, die einen Objekt spezifischen ACE enthält, muss die Revisions-ACL- \_ Revision verwenden \_ .

 

 
