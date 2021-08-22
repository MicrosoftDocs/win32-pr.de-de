---
title: Aktivieren Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft
description: Objekte der Container-Klasse verfügen über ein anderesWellKnownObjects-Attribut, mit dem Sie eine GUID dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuordnen können.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects-Eigenschaft
- otherWellKnownObjects-Eigenschaft, mithilfe von für umbenennungssichere Bindung
- Active Directory, verwenden, binden, umbenennensichere Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446f669adc9a59f9f8aba93e852546fe3991952857469d6f37978d9cf91a7666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695319"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Aktivieren Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft

Objekte der Container-Klasse verfügen über ein **anderesWellKnownObjects-Attribut,** mit dem Sie eine GUID dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuordnen können. Wenn das untergeordnete Objekt verschoben oder umbenannt wird, aktualisiert der Active Directory-Server den DN im **anderenWellKnownObjects-Wert** für dieses untergeordnete Objekt. Dies ermöglicht die Verwendung der WKGUID-Bindungsfunktion zum Binden an das untergeordnete Objekt mithilfe der GUID und des DN des Containers anstelle des DN des untergeordneten Objekts.

Das **otherWellKnownObjects-Attribut** entspricht dem **wellKnownObjects-Attribut,** außer dass Anwendungen und Dienste einen **anderenWellKnownObjects-Wert** schreiben können, aber nur das System **kann wellKnownObjects** schreiben.

Die Verwendung **des otherWellKnownObjects-Attributs** und der WKGUID-Bindung ist in den folgenden Situationen von Vorteil, in denen eine umbenennungssichere Bindung in Bezug auf ein bestimmtes Containerobjekt erforderlich ist.

Wenn ein Containerobjekt andere wichtige Objekte enthält oder wenn wichtige Objekte umbenannt oder verschoben werden können.

Wenn die wichtigen Objekte für jede Instanz des Containerobjekts vorhanden sind. Beispielsweise verwendet das System das **wellKnownObjects-Attribut** jedes **domainDNS-Objekts,** um einen Wert für den Container Users zu speichern, der in jeder Instanz eines **domainDNS-Objekts** vorhanden ist. Dadurch können Anwendungen auf umbenennungssichere Weise an den Container Users gebunden werden, indem die bekannte GUID und der DN des **DomainDNS-Containers** angegeben werden. Anwendungen können das **otherWellKnownObjects-Attribut** eines Containers auf ähnliche Weise verwenden.

Wenn Sie eine umbenennungssichere Bindung und/oder Suchfunktion für die wichtigen Objekte benötigen.

**So fügen Sie umbenennende sichere Bindungs- und Suchfunktionen hinzu**

1.  Fügen Sie der **otherWellKnownObjects-Eigenschaft** des Containerobjekts einen Wert hinzu, wenn das wichtige Objekt in diesem Container erstellt wird. Der Wert enthält die GUID, die das bekannte Objekt darstellt. Beachten Sie, dass dies nicht **objectGUID** und **distinguishedName** für dieses Objekt sind.
2.  Verwenden Sie die WKGUID-Bindungsfunktion, um das wichtige Objekt zu binden oder zu durchsuchen.

Das **otherWellKnownObjects-Attribut** kann mehrere Werte aufweisen und enthält die GUID/DN-Tupel bekannter Objekte in den Containern, für die sie festgelegt sind. Das **otherWellKnownObjects-Attribut** verfügt über die DNWithBinary-Syntax, in der Werte die folgende Form aufweisen:


```C++
B:<char count>:<well known GUID>:<object DN>
```



In diesem Beispiel &lt; ist "char &gt; count" die Anzahl der Hexadezimalziffern in &lt; "well known GUID", &gt; die 32 (Anzahl der hexadezimalen Ziffern in einer GUID) für **die beiden anderenWellKnownObjects** und **wellKnownObjects beträgt.** "well &lt; known &gt; GUID" ist die Hexadezimalzifferndarstellung der bekannten GUID. "Object &lt; &gt; DN" ist der Distinguished Name des Objekts, das durch diesen WKO-Wert dargestellt wird. Der Server verwaltet den ObjectDN-Teil jedes **wellKnownObjects-** und **anderenWellKnownObjects-Werts** so, dass er den aktuellen Distinguished Name des Objekts enthält, das ursprünglich beim Erstellen des Werts angegeben wurde.

Wenn {df447b5e-aa5b-11d2-8d53-00c04f79ab81} beispielsweise die bekannte GUID des MyObject-Objekts im MyContainer-Container in der domäne Fabrikam.com ist, würde der **otherWellKnownObjects-Wert** die bekannte GUID und den DN von MyObject angeben:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Verwenden Sie zum Binden an dieses Objekt die folgende WKGUID-Bindungszeichenfolge, die die bekannte GUID des Objekts und den DN des Containers angibt:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Nach der Bindung an dieses Objekt können Sie die ADSI-COM-Schnittstellen verwenden, um das Objekt zu suchen, zu lesen, zu ändern oder zu löschen.

Weitere Informationen und ein Codebeispiel, das zeigt, wie sie dem **otherWellKnownObjects-Attribut** ein Objekt hinzufügen, finden Sie unter [Beispielcode zum Erstellen eines Containerobjekts.](example-code-for-creating-a-container-object.md)

 

 




