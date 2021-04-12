---
title: Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft
description: Objekte der Container Klasse verfügen über ein OtherWellKnownObjects-Attribut, das Sie verwenden können, um eine GUID mit dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuzuordnen.
ms.assetid: 54f7468b-03e5-46b9-8b43-e3571dccdceb
ms.tgt_platform: multiple
keywords:
- otherWellKnownObjects (Eigenschaft)
- otherWellKnownObjects-Eigenschaft, Verwendung für Umbenennungs sichere Bindung
- Active Directory, verwenden, Bindung, Umbenennungs sichere Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7114fa6dfb44625433d8da1c57491a13aefa7cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206274"
---
# <a name="enabling-rename-safe-binding-with-the-otherwellknownobjects-property"></a>Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft

Objekte der Container Klasse verfügen über ein **otherWellKnownObjects** -Attribut, das Sie verwenden können, um eine GUID mit dem Distinguished Name (DN) eines untergeordneten Objekts im Container zuzuordnen. Wenn das untergeordnete Objekt verschoben oder umbenannt wird, aktualisiert der Active Directory Server den DN im **otherWellKnownObjects** -Wert für dieses untergeordnete Objekt. Dies ermöglicht die Verwendung des wkguid-Bindungs Features zum Binden an das untergeordnete Objekt mit der GUID und dem DN des Containers anstelle des DN des untergeordneten Objekts.

Das **otherWellKnownObjects** -Attribut entspricht dem **wellKnownObjects** -Attribut, mit dem Unterschied, dass Anwendungen und Dienste einen **otherWellKnownObjects** -Wert schreiben können, aber nur das System kann **wellKnownObjects** schreiben.

Die Verwendung des **otherWellKnownObjects** -Attributs und der wkguid-Bindung ist in den folgenden Situationen vorteilhaft, in denen eine Umbenennungs sichere Bindung in Bezug auf ein bestimmtes Container Objekt erforderlich ist.

, Wenn ein Container Objekt andere wichtige Objekte enthält, oder, wenn wichtige Objekte umbenannt oder verschoben werden können.

, Wenn die wichtigen Objekte für jede Instanz des Container Objekts vorhanden sind. Beispielsweise verwendet das System das **wellKnownObjects** -Attribut jedes **domainDns** -Objekts, um einen Wert für den Benutzer Container zu speichern, der in jeder Instanz eines **domainDns** -Objekts vorhanden ist. Dadurch können Anwendungen auf Umbenennungs sichere Weise eine Bindung an den Benutzer Container herstellen, indem Sie die bekannte GUID und den DN des **domainDns** -Containers angeben. Anwendungen können das **otherWellKnownObjects** -Attribut eines Containers ähnlich verwenden.

Wenn Sie für die wichtigen Objekte eine Umbenennungs sichere Bindung und/oder Suchfunktion benötigen.

**So fügen Sie Umbenennungs sichere Bindungs-und Suchfunktionen hinzu**

1.  Fügen Sie der **otherWellKnownObjects** -Eigenschaft des Container Objekts einen Wert hinzu, wenn das wichtige Objekt in diesem Container erstellt wird. Der Wert enthält die GUID, die das bekannte Objekt darstellt. Beachten Sie, dass es sich hierbei nicht um die **objectGUID** und den **unterscheidbaren Namen** für dieses Objekt handelt.
2.  Verwenden Sie das Bindungs Feature von wkguid, um das wichtige Objekt zu binden oder zu durchsuchen.

Das **otherWellKnownObjects** -Attribut kann mehrere Werte aufweisen und die GUID/DN-Tupel bekannter Objekte in den Containern enthalten, für die Sie festgelegt sind. Das **otherWellKnownObjects** -Attribut verfügt über die DNWithBinary-Syntax, in der die Werte die folgende Form aufweisen:


```C++
B:<char count>:<well known GUID>:<object DN>
```



In diesem Beispiel ist " &lt; char Count &gt; " die Anzahl von hexadezimalen Ziffern in " &lt; well known GUID &gt; 32" (Anzahl der hexadezimalen Ziffern in einer GUID) für " **otherWellKnownObjects** " und " **wellKnownObjects**". " &lt; well known GUID &gt; " ist die hexadezimale Ziffern Darstellung der bekannten GUID. " &lt; Object DN &gt; " ist der Distinguished Name des Objekts, das durch diesen WKO-Wert dargestellt wird. Der Server verwaltet den objectdn-Teil jedes **wellKnownObjects** -und **otherWellKnownObjects** -Werts, sodass er den aktuellen Distinguished Name des Objekts enthält, das ursprünglich beim Erstellen des Werts angegeben wurde.

Wenn {df447b5e-aa5b-11d2-8d53-00c04f79ab81} z. b. die bekannte GUID des MyObject-Objekts im Container MyContainer in der Fabrikam.com-Domäne ist, würde der **otherWellKnownObjects** -Wert die bekannte GUID und den DN von MyObject angeben:


```C++
B:32:df447b5eaa5b11d28d5300c04f79ab81:cn=MyObject,cn=MyContainer,dc=Fabrikam,dc=com
```



Um an dieses Objekt zu binden, verwenden Sie die folgende wkguid-Bindungs Zeichenfolge, die die bekannte GUID des Objekts und den DN des Containers angibt:


```C++
LDAP://<WKGUID=df447b5eaa5b11d28d5300c04f79ab81,cn=MyContainer,dc=Fabrikam,dc=com>
```



Nachdem Sie an dieses Objekt gebunden haben, können Sie die ADSI-COM-Schnittstellen verwenden, um das Objekt zu suchen, zu lesen, zu ändern oder zu löschen.

Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Objekt zum **otherWellKnownObjects** -Attribut hinzugefügt wird, finden Sie unter [Beispielcode zum Erstellen eines Container Objekts](example-code-for-creating-a-container-object.md).

 

 




