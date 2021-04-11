---
title: Verschieben vorhandener Benutzer in die Organisationseinheit
description: Wenn der Enterprise-Administrator Joe der die Windows NT 4,0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzer Containern in der Fabrikam-Domäne migriert.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Verschieben vorhandener Benutzer in die Organisationseinheit AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206240"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="cf13d-104">Verschieben vorhandener Benutzer in die Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="cf13d-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="cf13d-105">Wenn der Enterprise-Administrator Joe der die Windows NT 4,0-Domäne auf Active Directory aktualisiert, werden alle Benutzer und Gruppen zu den Benutzer Containern in der Fabrikam-Domäne migriert.</span><span class="sxs-lookup"><span data-stu-id="cf13d-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="cf13d-106">Joe kann nun diese Benutzer und Gruppen in die entsprechenden Organisationseinheiten verschieben.</span><span class="sxs-lookup"><span data-stu-id="cf13d-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="cf13d-107">Ein Objekt kann auch mithilfe von ADSI zwischen verwandten Windows 2000-Domänen verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="cf13d-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="cf13d-108">Im folgenden Codebeispiel verschiebt Joe "JeffSmith" in die Vertriebsorganisation.</span><span class="sxs-lookup"><span data-stu-id="cf13d-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="cf13d-109">Die [**IADsContainer. muvehere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) -Methode nimmt den ADsPath des zu verschiebenden Objekts und den neuen Objektnamen (RDN).</span><span class="sxs-lookup"><span data-stu-id="cf13d-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="cf13d-110">Wenn Sie den gleichen Namen beibehalten möchten, können Sie **null** (**vbNullString**) für den *bstrinnewname* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="cf13d-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="cf13d-111">Um das Objekt umzubenennen, wenn es verschoben wird, geben Sie den neuen relativen Distinguished Name für den *bstrinnewname* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="cf13d-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="cf13d-112">Wenn Sie z. b. JeffSmith in die Vertriebsorganisation verschieben und das "JeffSmith"-Objekt \_ im gleichen Vorgang in "Jeff Smith" umbenennen, würde Joe den folgenden Code ausführen:</span><span class="sxs-lookup"><span data-stu-id="cf13d-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="cf13d-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cf13d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf13d-114">Erstellen neuer Benutzer in der Organisationseinheit</span><span class="sxs-lookup"><span data-stu-id="cf13d-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




