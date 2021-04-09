---
title: Binden an Active Directory Domain Services
description: In Active Directory Domain Services wird das Zuordnen eines programmgesteuerten Objekts zu einem bestimmten Active Directory Domain Services Objekt als Bindung bezeichnet.
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- Bindung an Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory, binden an
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958211"
---
# <a name="binding-to-active-directory-domain-services"></a>Binden an Active Directory Domain Services

In Active Directory Domain Services wird das Zuordnen eines programmgesteuerten Objekts zu einem bestimmten Active Directory Domain Services Objekt als *Bindung* bezeichnet. Wenn ein Programm gesteuertes Objekt, z. b. ein [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -oder [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) -Objekt, einem bestimmten Verzeichnis Objekt zugeordnet ist, wird das programmgesteuerte Objekt als an das Verzeichnis Objekt *gebundene gebunden* .

## <a name="binding-functions-and-methods"></a>Bindungsfunktionen und-Methoden

Die Methode für die programmgesteuerte Bindung an ein Active Directory Objekt hängt von der verwendeten Programmier Technologie ab. Weitere Informationen zum Binden an Objekte in Active Directory Domain Services mit einer bestimmten Programmier Technologie finden Sie in den in der folgenden Tabelle aufgeführten Themen.



| Programmier Technologie                                                                       | Weitere Informationen finden Sie unter                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Binden an ein ADSI-Objekt](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Einrichten einer LDAP-Sitzung](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [Binden an Verzeichnisobjekte](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>Binden von Zeichen folgen

Alle Bindungsfunktionen und-Methoden erfordern eine Bindungs Zeichenfolge. Die Form der Bindungs Zeichenfolge hängt vom Anbieter ab. Active Directory Domain Services werden von den beiden Anbietern LDAP und WinNT unterstützt.

Ab Windows 2000 wird der LDAP-Anbieter für den Zugriff auf Active Directory Domain Services verwendet. Die LDAP-Bindungs Zeichenfolge kann eine der folgenden Formen annehmen:

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

In den obigen Beispielen gibt "LDAP:" den LDAP-Anbieter an. "GC:" verwendet den LDAP-Anbieter, um eine Bindung mit dem globalen Katalog Dienst herzustellen, um schnelle Abfragen auszuführen.

" &lt; Hostname &gt; " gibt den Server an, an den die Bindung erfolgen soll, und ist optional. Geben Sie nach Möglichkeit keinen Server an. Es ist auch möglich, eine Bindung an ein Objekt in einer anderen Domäne herzustellen. Übergeben Sie dazu den DNS-Namen (Domain Name System) der Zieldomäne für " &lt; Hostname &gt; ". Um z. b. an den Benutzer Container in der Domäne2-Domäne von fabrikam.com zu binden, ist die Bindungs Zeichenfolge "LDAP://domain2.fabrikam.com/cn=users,DC=domain2,DC=fabrikam,DC=com".

" &lt; Object Name &gt; " stellt ein bestimmtes Objekt in Active Directory Domain Services dar. Der Objektname kann ein definierter Name oder eine Objekt-GUID sein.

Weitere Informationen zu LDAP-Bindungs Zeichenfolgen finden Sie unter [LDAP ADsPath](/windows/desktop/ADSI/ldap-adspath).

Für Windows NT 4,0 wird der WinNT-Anbieter für den Zugriff auf Verzeichnis Daten wie z. b. Benutzer, Benutzergruppen, Computer, Dienste und andere Netzwerk Objekte in Windows 2000 verwendet. Der WinNT-Anbieter unter Windows 2000 und spätere Systeme verfügt im Vergleich zum LDAP-Anbieter über eingeschränkte Funktionalität. Weitere Informationen zu WinNT-Bindungs Zeichenfolgen finden Sie unter [Winnt ADsPath](/windows/desktop/ADSI/winnt-adspath).

Ein ADsPath-Element von "LDAP://" oder "GC://" kann verwendet werden, um eine Bindung zum Stammverzeichnis des Namespaces herzustellen. Wenn das angegebene Namespace Objekt an den Stamm des Namespaces gebunden ist, enthält es keine Eigenschaften und enthält das Domänen Objekt für LDAP und ein Container Objekt, das ein partielles Replikat aller Domänen in der Gesamtstruktur für GC enthält.

Weitere Informationen zum Binden in Active Directory Domain Services finden Sie unter:

-   [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md)
-   [Binden an den globalen Katalog](binding-to-the-global-catalog.md)
-   [Verwenden von objectGUID für die Bindung an ein Objekt](using-objectguid-to-bind-to-an-object.md)
-   [Binden an Well-Known Objekte mithilfe von wkguid](binding-to-well-known-objects-using-wkguid.md)
-   [Binden an ein Objekt mithilfe einer sid](binding-to-an-object-using-a-sid.md)
-   [Aktivieren der Rename-Safe Bindung mit der otherWellKnownObjects-Eigenschaft](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [Authentifizierung](authentication.md)

 

 
