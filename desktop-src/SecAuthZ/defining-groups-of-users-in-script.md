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
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="1a8ce-105">Definieren von Benutzergruppen in Skripts</span><span class="sxs-lookup"><span data-stu-id="1a8ce-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="1a8ce-106">Im Autorisierungs-Manager stellt ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt eine Gruppe von Benutzern dar.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="1a8ce-107">Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="1a8ce-108">Ein **iazapplicationgroup** -Objekt kann auch andere **iazapplicationgroup** -Objekte als Member enthalten.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="1a8ce-109">Weitere Informationen zu Anwendungs Gruppen finden Sie unter [Benutzer und Gruppen](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="1a8ce-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="1a8ce-110">Eine Gruppe kann entweder durch explizite Listen von Membern und nicht-Membern oder durch eine LDAP-Abfrage ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ) definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="1a8ce-111">In den folgenden Beispielen wird gezeigt, wie die einzelnen Anwendungs Gruppen Typen erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="1a8ce-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="1a8ce-112">Erstellen einer einfachen Gruppe</span><span class="sxs-lookup"><span data-stu-id="1a8ce-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="1a8ce-113">Erstellen einer LDAP-Abfrage Gruppe</span><span class="sxs-lookup"><span data-stu-id="1a8ce-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="1a8ce-114">Erstellen einer einfachen Gruppe</span><span class="sxs-lookup"><span data-stu-id="1a8ce-114">Creating a Basic Group</span></span>

<span data-ttu-id="1a8ce-115">Eine einfache Anwendungs Gruppe wird durch die Elemente definiert [**, die in**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) den Membern und [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) -Eigenschaften des [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekts enthalten sind, das die Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="1a8ce-116">Benutzer und Gruppen, die in der Eigenschaft **Members** aufgeführt sind, sind in der Anwendungs Gruppe enthalten, und Benutzer und Gruppen, die in der Eigenschaft **nonmembers** aufgeführt sind, werden aus der Anwendungs Gruppe ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="1a8ce-117">Das Auflisten in der **nonmembers** -Eigenschaft ersetzt das Auflisten in der **Members** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="1a8ce-118">Im folgenden Beispiel wird gezeigt, wie eine einfache Anwendungs Gruppe erstellt und alle lokalen Benutzer als Mitglieder dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="1a8ce-119">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="1a8ce-120">Erstellen einer LDAP-Abfrage Gruppe</span><span class="sxs-lookup"><span data-stu-id="1a8ce-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="1a8ce-121">Eine LDAP-Abfrage Gruppe verfügt über eine-Mitgliedschaft, die durch die Abfrage definiert ist, die im Wert Ihrer [**ldapquery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) -Eigenschaft enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="1a8ce-122">Im folgenden Beispiel wird gezeigt, wie eine LDAP-Abfrage Anwendungs Gruppe erstellt und alle Benutzer als Mitglieder dieser Gruppe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="1a8ce-123">Im Beispiel wird davon ausgegangen, dass ein vorhandener XML-Richtlinien Speicher namens MyStore.xml im Stammverzeichnis des Laufwerks C vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a8ce-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



 

 
