---
title: Delegieren von Organisationseinheiten
description: Das Fabrikam-Unternehmen beauftragt zwei Administratoren, Mike und Paul, um die Organisationseinheiten "Ost" und "Europa, Westen" zu verwalten.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337137"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="f192d-103">Delegieren von Organisationseinheiten</span><span class="sxs-lookup"><span data-stu-id="f192d-103">Delegating Organizational Units</span></span>

<span data-ttu-id="f192d-104">Das Fabrikam-Unternehmen beauftragt zwei Administratoren, Mike und Paul, um die Organisationseinheiten "Ost" und "Europa, Westen" zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f192d-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="f192d-105">Joe delegiert seine administrativen Zuständigkeiten an Sie, damit Sie Benutzer in den jeweiligen Organisationseinheiten erstellen und löschen können.</span><span class="sxs-lookup"><span data-stu-id="f192d-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="f192d-106">Bevor Sie sehen, wie Sie diese Organisationseinheiten unter Mike und Paul einrichten, müssen Sie wissen, wie Sie den Zugriff auf Objekte in Active Directory einrichten.</span><span class="sxs-lookup"><span data-stu-id="f192d-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="f192d-107">Jedes Objekt in Active Directory verfügt über eine Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="f192d-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="f192d-108">Mit der Sicherheits Beschreibung können Sie Berechtigungen für das Objekt ändern, Berechtigungen weitergeben, die Überwachung aktivieren usw.</span><span class="sxs-lookup"><span data-stu-id="f192d-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="f192d-109">Die Sicherheits Beschreibung selbst verfügt über zwei Zugriffs Steuerungs Listen (Access Control Lists, ACLs): eine freigegebene ACL (DACL) und eine System-ACL (SACL).</span><span class="sxs-lookup"><span data-stu-id="f192d-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="f192d-110">Jede ACL kann Zugriffs Steuerungs Einträge (Access Control Entries, ACEs) enthalten.</span><span class="sxs-lookup"><span data-stu-id="f192d-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="f192d-111">Mit einem ACE können Sie den zulässigen oder verweigerten Zugriff für ein Objekt festlegen.</span><span class="sxs-lookup"><span data-stu-id="f192d-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="f192d-112">Außerdem können Sie bestimmte Aktionen angeben, die Sie zulassen oder verweigern möchten.</span><span class="sxs-lookup"><span data-stu-id="f192d-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="f192d-113">Beispiele für Aktionen sind das Erstellen von untergeordneten Elementen, das Löschen von untergeordneten Elementen, Leseeigenschaften und Schreib Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f192d-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="f192d-114">Diese Rechte werden mit der [**AccessMask**](iadsaccesscontrolentry-property-methods.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="f192d-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="f192d-115">Als nächstes können Sie die Klassen oder Attribute angeben, denen dieser ACE zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f192d-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="f192d-116">Im folgenden Beispiel für Fabrikam wählt Joe die Benutzerklasse aus, sodass jeder Administrator dem Systembenutzer hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="f192d-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="f192d-117">Als nächstes müssen Sie die folgende Frage beantworten: "Wer wird der Empfänger dieses ACE sein?"</span><span class="sxs-lookup"><span data-stu-id="f192d-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="f192d-118">Joe legt Mike fest.</span><span class="sxs-lookup"><span data-stu-id="f192d-118">Joe will specify Mike.</span></span>

<span data-ttu-id="f192d-119">Schließlich können Sie das Verhalten der ACE-Vererbung festlegen – beispielsweise kann ACEs angegeben werden, um die Hierarchie nach unten zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="f192d-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="f192d-120">Zusammenfassend führt das vorherige Beispiel dazu, dass Mike in der Lage ist, Benutzer Objekte unter der Organisationseinheit "Ost Sales" zu erstellen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f192d-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="f192d-121">Joe verwendet das folgende Codebeispiel, um die ACEs und ACLs für die Region "Osten" einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f192d-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="f192d-122">In der folgenden Abbildung wird das Menü Active Directory **neue Ansicht erstellen** nach dem Ausführen des Codes angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f192d-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="f192d-123">Wenn sich Joe, der Administrator, anmeldet, sieht er verschiedene Klassen, die er erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="f192d-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="f192d-124">Wenn Mike sich jedoch anmeldet, kann er nur Benutzer Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="f192d-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![Optionsmenü "neue Ansicht erstellen"](images/adadsi5.png)

<span data-ttu-id="f192d-126">Weitere Informationen finden Sie unter [ADSI Security Model](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="f192d-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




