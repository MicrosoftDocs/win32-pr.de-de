---
description: Ein iazapplicationgroup-Objekt stellt eine Gruppe von Benutzern dar. Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden. Ein iazapplicationgroup-Objekt kann auch andere iazapplicationgroup-Objekte als Member enthalten.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definieren von Benutzergruppen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348938"
---
# <a name="defining-groups-of-users-in-script"></a>Definieren von Benutzergruppen in Skripts

Im Autorisierungs-Manager stellt ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt eine Gruppe von Benutzern dar. Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden. Ein **iazapplicationgroup** -Objekt kann auch andere **iazapplicationgroup** -Objekte als Member enthalten. Weitere Informationen zu Anwendungs Gruppen finden Sie unter [Benutzer und Gruppen](users-and-groups.md).

Eine Gruppe kann entweder durch explizite Listen von Membern und nicht-Membern oder durch eine LDAP-Abfrage ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ) definiert werden. In den folgenden Beispielen wird gezeigt, wie die einzelnen Anwendungs Gruppen Typen erstellt werden:

-   [Erstellen einer einfachen Gruppe](#creating-a-basic-group)
-   [Erstellen einer LDAP-Abfrage Gruppe](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Erstellen einer einfachen Gruppe

Eine einfache Anwendungs Gruppe wird durch die Elemente definiert [**, die in**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) den Membern und [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) -Eigenschaften des [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekts enthalten sind, das die Gruppe darstellt. Benutzer und Gruppen, die in der Eigenschaft **Members** aufgeführt sind, sind in der Anwendungs Gruppe enthalten, und Benutzer und Gruppen, die in der Eigenschaft **nonmembers** aufgeführt sind, werden aus der Anwendungs Gruppe ausgeschlossen. Das Auflisten in der **nonmembers** -Eigenschaft ersetzt das Auflisten in der **Members** -Eigenschaft.

Im folgenden Beispiel wird gezeigt, wie eine einfache Anwendungs Gruppe erstellt und alle lokalen Benutzer als Mitglieder dieser Gruppe hinzugefügt werden. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Erstellen einer LDAP-Abfrage Gruppe

Eine LDAP-Abfrage Gruppe verfügt über eine-Mitgliedschaft, die durch die Abfrage definiert ist, die im Wert Ihrer [**ldapquery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) -Eigenschaft enthalten ist.

Im folgenden Beispiel wird gezeigt, wie eine LDAP-Abfrage Anwendungs Gruppe erstellt und alle Benutzer als Mitglieder dieser Gruppe hinzugefügt werden. Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
