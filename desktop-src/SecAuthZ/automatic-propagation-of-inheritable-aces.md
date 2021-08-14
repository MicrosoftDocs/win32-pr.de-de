---
description: Die Funktionen SetNamedSecurityInfo und SetSecurityInfo unterstützen die automatische Weitergabe von vererbbaren Zugriffssteuerungseinträgen (ACEs).
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Automatische Weitergabe vererbbarer ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3257c038174549eebb8d960f8f4bc0601f95a928478e2a783f93f4a1444a22d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783717"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Automatische Weitergabe vererbbarer ACEs

Die [**Funktionen SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) und [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) unterstützen die automatische Weitergabe von vererbbaren Zugriffssteuerungseinträgen (ACEs). [](/windows/desktop/SecGloss/a-gly) Wenn Sie diese Funktionen beispielsweise verwenden, um einem Verzeichnis in einem NTFS-Verzeichnis einen vererbten ACE hinzuzufügen, wendet das System den ACE entsprechend den Zugriffssteuerungslisten [](/windows/desktop/SecGloss/a-gly) (ACLs) aller vorhandenen Unterverzeichnisse oder Dateien an.

Direkt angewendete ACEs haben Vorrang vor geerbten ACEs. Das System implementiert diese Rangfolge, indem direkt angewendete ACEs vor geerbten ACEs in einer DACL [*(Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) platziert werden. Wenn Sie die [**Funktionen SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) und [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) aufrufen, um die Sicherheitsinformationen eines Objekts festlegen, erzwingt das System das aktuelle Vererbungsmodell für die ACLs aller Objekte in der Hierarchie unterhalb des Zielobjekts. Für Objekte, die in das aktuelle Vererbungsmodell konvertiert wurden, werden die SE \_ DACL \_ AUTO INHERITED- und \_ SE \_ SACL AUTO \_ \_ INHERITED-Bits [](/windows/desktop/SecGloss/s-gly) im Steuerelementfeld der Sicherheitsbeschreibung des Objekts festgelegt.

Wenn Sie eine neue Sicherheitsbeschreibung erstellen, die das aktuelle Vererbungsmodell widerspiegelt, wird darauf achten, die Semantik der Sicherheitsbeschreibung nicht zu ändern. Daher werden AcEs zum Zulassen und Verweigern nie in Beziehung zueinander verschoben. Wenn eine solche Bewegung erforderlich ist (z. B. um alle nicht-inheritierten ACEs am Anfang einer ACL zu platzieren), wird die ACL als geschützt markiert, um die semantische Änderung zu verhindern.

Das System verwendet die folgenden Regeln, wenn geerbte ACEs an untergeordnete Objekte übermittelt werden:

-   Wenn ein untergeordnetes Objekt ohne DACL einen ACE erbt, ist das Ergebnis ein untergeordnetes Objekt mit einer DACL, das nur den geerbten ACE enthält.
-   Wenn ein untergeordnetes Objekt mit einer leeren DACL einen ACE erbt, ist das Ergebnis ein untergeordnetes Objekt mit einer DACL, das nur den geerbten ACE enthält.
-   Wenn Sie einen vererbbaren ACE aus einem übergeordneten Objekt entfernen, entfernt die automatische Vererbung alle Kopien des ACE, die von untergeordneten Objekten geerbt wurden.
-   Wenn die automatische Vererbung zum Entfernen aller ACEs aus der DACL eines untergeordneten Objekts führt, verfügt das untergeordnete Objekt über eine leere DACL anstatt über keine DACL.

Diese Regeln können das unerwartete Ergebnis der Konvertierung eines Objekts ohne DACL in ein Objekt mit einer leeren DACL haben. Ein Objekt ohne DACL ermöglicht vollzugriff, aber ein Objekt mit einer leeren DACL lässt keinen Zugriff zu. Als Beispiel dafür, wie diese Regeln eine leere DACL erstellen können, fügen Sie dem Stammobjekt einer Objektstruktur einen vererbbaren ACE hinzu. Die automatische Vererbung gibt den vererbbaren ACE an alle Objekte in der Struktur weiter. Untergeordnete Objekte, die ohne DACL gestartet wurden, verfügen jetzt über eine DACL mit dem geerbten ACE. Wenn Sie den vererbbaren ACE aus dem Stammobjekt entfernen, gibt das System die Änderung automatisch an die untergeordneten Objekte weiter. Untergeordnete Objekte, die ohne DACL gestartet wurden (vollzugriff zulassen), verfügen jetzt über eine leere DACL (die keinen Zugriff zu lässt).

Um sicherzustellen, dass ein untergeordnetes Objekt ohne DACL nicht von vererbten ACEs betroffen ist, legen Sie das SE DACL PROTECTED-Flag in der Sicherheitsbeschreibung des Objekts \_ \_ fest.

Informationen zum ordnungsgemäßen Erstellen einer DACL finden Sie unter [Erstellen einer DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

 
