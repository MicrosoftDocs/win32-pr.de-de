---
description: Die Funktionen "SetNamedSecurityInfo" und "setsecurityinfo" unterstützen die Automatische Propagierung von vererbbaren Zugriffs Steuerungs Einträgen (ACEs).
ms.assetid: 0aa49b9b-13e3-4ef9-921d-ea47a013e5a1
title: Automatische Propagierung von vererbbaren ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fab03c73a1c926468e46a0d0492e512dab42af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218832"
---
# <a name="automatic-propagation-of-inheritable-aces"></a>Automatische Propagierung von vererbbaren ACEs

Die Funktionen " [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) " und " [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) " unterstützen die Automatische Propagierung von vererbbaren [*Zugriffs Steuerungs Einträgen*](/windows/desktop/SecGloss/a-gly) (ACEs). Wenn Sie z. b. diese Funktionen zum Hinzufügen eines vererbbaren ACE zu einem Verzeichnis in einem NTFS verwenden, wendet das System den ACE entsprechend den [*Zugriffs Steuerungs Listen (Access Control Lists*](/windows/desktop/SecGloss/a-gly) , ACLs) aller vorhandenen Unterverzeichnisse oder Dateien an.

Direkt angewendete ACEs haben Vorrang vor geerbten ACEs. Das System implementiert diese Rangfolge, indem direkt angewendete ACEs in einer freigegebenen [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) vor geerbten ACEs platziert werden. Wenn Sie die Funktionen [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) und [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) aufrufen, um die Sicherheitsinformationen eines Objekts festzulegen, erzwingt das System das aktuelle Vererbungs Modell für die ACLs aller Objekte in der Hierarchie unterhalb des Zielobjekts. Für Objekte, die in das aktuelle Vererbungs Modell konvertiert wurden, werden die automatisch geerbten SE \_ DACL-Werte für \_ automatisch \_ geerbte und SE \_ SACL \_ \_ im Steuerelement Feld der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) des Objekts festgelegt.

Wenn Sie eine neue Sicherheits Beschreibung erstellen, die das aktuelle Vererbungs Modell widerspiegelt, wird die Semantik der Sicherheits Beschreibung nicht geändert. Daher werden allow-und deny-ACEs niemals in Beziehung zueinander verschoben. Wenn eine solche Verschiebung erforderlich ist (z. b. um alle nicht geerbten ACEs vor einer ACL zu platzieren), wird die ACL als geschützt gekennzeichnet, um die semantische Änderung zu verhindern.

Das System verwendet die folgenden Regeln, wenn geerbte ACEs an untergeordnete Objekte weitergegeben werden:

-   Wenn ein untergeordnetes Objekt ohne DACL einen ACE erbt, ist das Ergebnis ein untergeordnetes Objekt mit einer DACL, die nur den geerbten ACE enthält.
-   Wenn ein untergeordnetes Objekt mit einer leeren DACL einen ACE erbt, ist das Ergebnis ein untergeordnetes Objekt mit einer DACL, die nur den geerbten ACE enthält.
-   Wenn Sie einen vererbbaren ACE aus einem übergeordneten Objekt entfernen, entfernt die automatische Vererbung alle Kopien des ACE, die von untergeordneten Objekten geerbt wurden.
-   Wenn die automatische Vererbung dazu führt, dass alle ACEs aus der DACL eines untergeordneten Objekts entfernt werden, hat das untergeordnete Objekt eine leere DACL und keine DACL.

Diese Regeln können das unerwartete Ergebnis der Typumwandlung eines Objekts ohne DACL in ein Objekt mit einer leeren DACL haben. Ein Objekt ohne DACL ermöglicht den Vollzugriff, aber ein Objekt mit einer leeren DACL lässt keinen Zugriff zu. Als Beispiel dafür, wie diese Regeln eine leere DACL erstellen können, nehmen Sie an, dass Sie dem Stamm Objekt einer Struktur von Objekten einen vererbbaren ACE hinzufügen. Die automatische Vererbung gibt den vererbbaren ACE an alle Objekte in der Struktur weiter. Untergeordnete Objekte, die ohne DACL gestartet wurden, verfügen jetzt über eine DACL mit dem geerbten ACE. Wenn Sie den vererbbaren ACE aus dem Stamm Objekt entfernen, gibt das System die Änderung automatisch an die untergeordneten Objekte weiter. Untergeordnete Objekte, die ohne DACL gestartet werden (Vollzugriff zulassen), verfügen nun über eine leere DACL (ohne Zugriff).

Um sicherzustellen, dass ein untergeordnetes Objekt ohne DACL von vererbbaren ACEs nicht betroffen ist, legen Sie das SE \_ DACL \_ Protected-Flag in der Sicherheits Beschreibung des-Objekts fest.

Informationen dazu, wie Sie eine DACL ordnungsgemäß erstellen, finden Sie unter [Erstellen einer DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
