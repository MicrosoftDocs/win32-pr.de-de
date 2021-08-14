---
description: Ein IAzApplicationGroup-Objekt stellt eine Gruppe von Benutzern dar. Rollen können dann dieser Gruppe von Benutzern zusammen zugewiesen werden. Ein IAzApplicationGroup-Objekt kann auch andere IAzApplicationGroup-Objekte als Member enthalten.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definieren von Benutzergruppen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6198d31a53dbd7d30100a8df56536cf0336c9c1e7ca5b78ad4e9e73e40da13cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913986"
---
# <a name="defining-groups-of-users-in-script"></a>Definieren von Benutzergruppen in Skripts

Im Autorisierungs-Manager stellt ein [**IAzApplicationGroup-Objekt**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) eine Gruppe von Benutzern dar. Rollen können dann dieser Gruppe von Benutzern zusammen zugewiesen werden. Ein **IAzApplicationGroup-Objekt** kann auch andere **IAzApplicationGroup-Objekte** als Member enthalten. Weitere Informationen zu Anwendungsgruppen finden Sie unter [Benutzer und Gruppen.](users-and-groups.md)

Eine Gruppe kann entweder durch explizite Listen von Mitgliedern und Nichtmitgliedern oder durch eine [*LDAP-Abfrage (Lightweight Directory Access Protocol)*](/windows/desktop/SecGloss/l-gly) definiert werden. In den folgenden Beispielen wird gezeigt, wie die einzelnen Anwendungsgruppentypen erstellt werden:

-   [Erstellen einer Basisgruppe](#creating-a-basic-group)
-   [Erstellen einer LDAP-Abfragegruppe](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Erstellen einer Basisgruppe

Eine einfache Anwendungsgruppe wird von den Mitgliedern definiert, die in den Eigenschaften [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) und [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) des [**IAzApplicationGroup-Objekts**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) enthalten sind, das die Gruppe darstellt. Benutzer und Gruppen, die in der **Eigenschaft Mitglieder** aufgeführt sind, sind in der Anwendungsgruppe enthalten, und Benutzer und Gruppen, die in der **NonMembers-Eigenschaft** aufgeführt sind, werden aus der Anwendungsgruppe ausgeschlossen. Die Liste in der **NonMembers-Eigenschaft** ersetzt die Liste in der **Members-Eigenschaft.**

Das folgende Beispiel zeigt, wie Sie eine einfache Anwendungsgruppe erstellen und alle lokalen Benutzer als Mitglieder dieser Gruppe hinzufügen. Im Beispiel wird davon ausgegangen, dass ein XML-Richtlinienspeicher mit dem Namen MyStore.xml Stammverzeichnis von Laufwerk C vorhanden ist.


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



## <a name="creating-an-ldap-query-group"></a>Erstellen einer LDAP-Abfragegruppe

Eine LDAP-Abfragegruppe verfügt über eine Mitgliedschaft, die durch die Abfrage definiert wird, die im Wert ihrer [**LdapQuery-Eigenschaft enthalten**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) ist.

Das folgende Beispiel zeigt, wie Sie eine LDAP-Abfrageanwendungsgruppe erstellen und alle Benutzer als Mitglieder dieser Gruppe hinzufügen. Im Beispiel wird davon ausgegangen, dass ein XML-Richtlinienspeicher mit dem Namen MyStore.xml Stammverzeichnis von Laufwerk C vorhanden ist.


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



 

 
