---
description: Objektspezifische ACEs werden für Verzeichnisdienstobjekte (Directory Service, DS) unterstützt. Ein objektspezifischer ACE enthält ein Paar von GUIDs, die die Möglichkeiten erweitern, mit denen der ACE ein Objekt schützen kann.
ms.assetid: 37d353c0-ac22-430f-b5f3-15deb69be24b
title: Objektspezifische ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4212a0f7fe4eff7e38b41fe2636643c457cfeb51
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469577"
---
# <a name="object-specific-aces"></a>Objektspezifische ACEs

Objektspezifische [*ACEs werden*](/windows/desktop/SecGloss/a-gly) für Verzeichnisdienstobjekte (Directory Service, DS) unterstützt. Ein objektspezifischer ACE enthält ein Paar von GUIDs, die die Möglichkeiten erweitern, mit denen der ACE ein Objekt schützen kann.




| GUID | Beschreibung | 
|------|-------------|
| <strong>ObjectType</strong> | Identifiziert eine der folgenden:<ul><li>Ein Typ des untergeordneten Objekts. Der ACE steuert das Recht, einen angegebenen Typ von untergeordnetem Objekt zu erstellen. Weitere Informationen finden Sie unter <a href="controlling-child-object-creation-in-c--.md">Steuern der Erstellung untergeordneter Objekte in C++.</a></li><li>Ein Eigenschaftensatz oder eine Eigenschaft. Der ACE steuert das Recht, die Eigenschaft oder den Eigenschaftensatz zu lesen oder zu schreiben. Weitere Informationen finden Sie unter <a href="aces-to-control-access-to-an-object-s-properties.md">ACEs zum Steuern des Zugriffs auf die Eigenschaften eines Objekts.</a></li><li>Ein erweitertes Recht. Der ACE steuert das Recht, den vorgang durchzuführen, der dem erweiterten Recht zugeordnet ist.</li><li>Ein überprüfter Schreibzugriff. Der ACE steuert das Recht, bestimmte Schreibvorgänge durchzuführen. Diese überprüften Schreibberechtigungen, die im ACL-Editor definiert und verfügbar gemacht werden, bieten Berechtigungen für überprüfte Schreibvorgänge von Eigenschaften anstelle von nicht aktivierten Schreibvorgängen auf niedriger Ebene eines beliebigen Werts in eine Eigenschaft, die mit der Berechtigung "write property" erteilt wird.</li></ul> | 
| <strong>Inheritedobjecttype</strong> | Gibt den Typ des untergeordneten Objekts an, das den ACE erben kann. Die Vererbung wird auch durch <a href="/windows/desktop/api/Winnt/ns-winnt-ace_header"><strong></strong></a>die Vererbungsflags in der ACE_HEADER sowie durch jeglichen Schutz vor Vererbung gesteuert, die auf den untergeordneten Objekten platziert wird. Weitere Informationen finden Sie unter <a href="ace-inheritance.md">ACE-Vererbung.</a> | 




 

Drei Typen von objektspezifischen ACEs werden unterstützt.

> [!Note]  
> Systemalarmobjekt-ACEs werden derzeit nicht unterstützt.

 



| type                      | BESCHREIBUNG                                                                                                                                                                                                                                       |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Access-denied object ACE  | Wird in einer DACL verwendet, um einem Vertrauenshänder den Zugriff auf eine Eigenschaft oder eine Eigenschaft zu verweigern, die für das Objekt festgelegt ist, oder um die ACE-Vererbung auf einen angegebenen Typ von untergeordnetem Objekt zu beschränken. Verwendet die [**ACCESS \_ DENIED \_ OBJECT \_ ACE-Struktur.**](/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace)         |
| Access-allowed object ACE | Wird in einer DACL verwendet, um einem Vertrauenshänder Zugriff auf eine Eigenschaft oder eine Eigenschaft zu ermöglichen, die für das Objekt festgelegt ist, oder um die ACE-Vererbung auf einen angegebenen Typ von untergeordnetem Objekt zu beschränken. Verwendet die [**ACCESS \_ ALLOWED OBJECT \_ \_ ACE-Struktur.**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace)      |
| Ace für Systemüberwachungsobjekt   | Wird in einer SACL verwendet, um die Versuche eines Vertrauenshänders zu protokollieren, auf eine Eigenschaft oder einen Eigenschaftensatz für das Objekt zu zugreifen, oder um die ACE-Vererbung auf einen angegebenen Typ von untergeordnetem Objekt zu beschränken. Verwendet die [**\_ ACE-Struktur von SYSTEM AUDIT \_ OBJECT. \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace) |



 

Jede ACL, die einen objektspezifischen ACE enthält, muss die Revision ACL \_ REVISION \_ DS verwenden.

 

 
