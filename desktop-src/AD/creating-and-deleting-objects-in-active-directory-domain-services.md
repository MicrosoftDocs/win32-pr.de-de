---
title: Erstellen und Löschen von Objekten in Active Directory Domain Services
description: Die Prozedur, die verwendet wird, um Objekte in Active Directory Domain Services Programm gesteuert zu erstellen und zu löschen, hängt von der verwendeten Programmier Technologie ab.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Erstellen und Löschen von Active Directory Objekten Active Directory
- Active Directory Domain Services Active Directory mit erstellen und Löschen von Objekten
- Objekte Active Directory, erstellen und Löschen von Active Directory Domain Services Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472620"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Erstellen und Löschen von Objekten in Active Directory Domain Services

Die Prozedur, die verwendet wird, um Objekte in Active Directory Domain Services Programm gesteuert zu erstellen und zu löschen, hängt von der verwendeten Programmier Technologie ab. Weitere Informationen zum Erstellen und Löschen von Objekten in Active Directory Domain Services mit einer bestimmten Programmier Technologie finden Sie in den in der folgenden Tabelle aufgeführten Themen.



| Programmier Technologie                                                                       | Weitere Informationen finden Sie unter                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Active Directory Service Interfaces](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Erstellen und Löschen von Objekten](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Lightweight Directory Access Protocol](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Ändern eines Verzeichniseintrags](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Erstellen, löschen, umbenennen und Verschieben von Objekten](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Erstellen eines Objekts

Im Allgemeinen sind die einzigen Attribute, die für die Erstellung eines Objekts erforderlich sind, das **CN** -Attribut und das **objectClass** -Attribut. Wenn Sie nur ein Objekt erstellen, wird es nicht notwendigerweise zu einem funktionalen Objekt. Bestimmte Objekttypen, z. b. Benutzer und Gruppen, verfügen über zusätzliche erforderliche Attribute, damit Sie funktionsfähig sind. Weitere Informationen zum Erstellen bestimmter Objekttypen finden Sie unter [Erstellen eines Benutzers](creating-a-user.md) und [Erstellen von Gruppen in einer Domäne](creating-groups-in-a-domain.md).

**Windows Server 2003:** Wenn ein Objekt der [**Benutzer**](/windows/desktop/ADSchema/c-user)-, [**Gruppen**](/windows/desktop/ADSchema/c-group)-oder [**Computer**](/windows/desktop/ADSchema/c-computer) Klasse auf einem Domänen Controller erstellt wird, der auf wwindows Server 2003 oder höher ausgeführt wird, legt der Domänen Controller automatisch das [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) -Attribut für das Objekt auf eine eindeutige Zeichenfolge fest, sofern nicht angegeben.

## <a name="deleting-an-object"></a>Löschen eines Objekts

Der Active Directory Server führt die folgenden Aktionen aus, wenn ein Objekt gelöscht wird:

-   Das **isDeleted** -Attribut des gelöschten Objekts ist auf " **true**" festgelegt. Objekte, deren **isDeleted** -Attribut Wert auf **true** festgelegt ist, werden als [*Tombstones*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))bezeichnet.
-   Das gelöschte Objekt wird für den namens Kontext in den Container für gelöschte Objekte verschoben. Wenn die Object **systemFlags** -Eigenschaft das 0x02000000-Flag enthält, wird das Objekt nicht in den Container für gelöschte Objekte verschoben. Weitere Informationen zum Binden und Auflisten der Inhalte des Containers für gelöschte Objekte finden Sie unter [Abrufen gelöschter Objekte](retrieving-deleted-objects.md).
-   Der Container "Gelöschte Objekte" ist flach, sodass sich alle Objekte im Container "Gelöschte Objekte" auf derselben Ebene befinden. Daher wird der Relative Distinguished Name des gelöschten Objekts geändert, um sicherzustellen, dass der Name innerhalb des gelöschten Objekte Containers eindeutig ist. Wenn der ursprüngliche Name länger als 75 Zeichen ist, wird er auf 75 Zeichen gekürzt. Anschließend werden die folgenden an den neuen Namen angehängt:
    1.  Ein 0x0A-Zeichen
    2.  Die Zeichenfolge "del:"
    3.  Die Zeichen folgen Form einer eindeutigen GUID, z. b. "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Ein Beispiel für einen gelöschten Objektnamen lautet:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   Die meisten Attributwerte für das gelöschte Objekt werden entfernt. Die folgenden Attribute werden automatisch beibehalten:

    -   **AttributeID**
    -   **attributeSyntax**
    -   **"distinguishedName"**
    -   **dnreferenceupdate**
    -   **flatname**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-kreatorsid**
    -   **msmqownerid**
    -   **name**
    -   **NCName**
    -   **objectClass**
    -   **objectGUID**
    -   **objectSID**
    -   **oMSyntax**
    -   **proxiedobjectname**
    -   **replpropertymetadata**
    -   **sAMAccountName**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustatus Tributes**
    -   **Trust Direction**
    -   **Trust Partner**
    -   **trustType**
    -   **userAccountControl**
    -   **nicht geändert**
    -   **uSNCreated**
    -   **whenCreated**

    Andere Attribute, die über einen **searchFlags** -Attribut Wert verfügen, der 0x00000008 enthält, werden ebenfalls beibehalten.

    Die folgenden Attributwerte werden immer aus einem gelöschten Objekt entfernt:

    -   **objectCategory**
    -   **samAccountType**

-   Die Sicherheits Beschreibung des gelöschten Objekts wird beibehalten, und vererbbare Zugriffs Steuerungs Einträge werden nicht weitergegeben. Die Sicherheits Beschreibung wird unverändert aufbewahrt, wenn das Objekt gelöscht wird.
-   Links zu und aus dem gelöschten Objekt werden gelöscht. Dies wird im Hintergrund ausgeführt, nachdem das Objekt gelöscht wurde. Wenn das gelöschte Objekt wieder hergestellt wird, bevor alle Links gelöscht wurden, wird ein Fehler empfangen.
-   Wenn das Objekt auf einem Windows Server 2003-Domänen Controller gelöscht wird, wird das **lastKnownParent** -Attribut des gelöschten Objekts auf den Distinguished Name des Containers festgelegt, in dem das Objekt enthalten war, als es gelöscht wurde.

Das gelöschte Objekt verbleibt für einen Zeitraum, der als *Tombstone-Lebensdauer* bezeichnet wird, im Container für gelöschte Objekte. Standardmäßig beträgt die Tombstone-Lebensdauer 60 Tage, dieser Wert kann jedoch vom Systemadministrator geändert werden. Nachdem die Tombstone-Lebensdauer abgelaufen ist, wird das Objekt dauerhaft aus dem Verzeichnisdienst entfernt. Um zu vermeiden, dass ein Löschvorgang fehlt, muss eine Anwendung Inkrementelle Synchronisierung häufiger als die Tombstone-Lebensdauer ausführen.

Windows Server 2003 bietet die Möglichkeit, gelöschte Objekte wiederherzustellen. Weitere Informationen zur Wiederherstellung gelöschter Objekte finden Sie unter [Wiederherstellen gelöschter Objekte](restoring-deleted-objects.md).

Wenn ein Element gelöscht wird, kann keines der Attribute des Objekts geändert werden. In Windows Server 2003 ist es möglich, die Sicherheits Beschreibung (das **ntSecurityDescriptor** -Attribut) für ein gelöschtes Objekt zu ändern. Dies ermöglicht die Wiederherstellung von Objekten, wenn die Person, die das Objekt wiederherstellt, nicht über Schreibberechtigungen für obligatorische Attribute verfügt. Um die Sicherheits Beschreibung für ein gelöschtes Objekt zu aktualisieren, muss der Aufrufer zusätzlich zu regulärem **Schreib \_** Zugriff und Schreibzugriff auf den **\_ Besitzer** über das Steuerelement Zugriff mit dem reanimieren von Tombstones verfügen. Selbst wenn die Sicherheits Beschreibung restriktiv ist, kann der Administrator zuerst den Besitz des Objekts übernehmen, vorausgesetzt, der Administrator hat die Berechtigung zum Akzeptieren des **\_ \_ Besitz \_ namens** , und anschließend wird die Sicherheits Beschreibung geändert. Verwenden Sie hierzu die LDAP-Funktion zum [**\_ Ändern von \_ Ext \_**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) mit dem [**LDAP-Server " \_ \_ \_ gelöschtes \_ OID**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) -Steuerelement anzeigen". Die Änderungsliste muss eine einzelne Attribut Ersetzung für das **ntSecurityDescriptor** -Attribut enthalten.

 

 