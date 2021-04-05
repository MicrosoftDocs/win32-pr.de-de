---
title: Löschen von Access Control und Objekten
description: Mit Active Directory können Sie ein Objekt löschen, wenn Sie über Lösch Zugriff auf das Objekt verfügen, oder wenn Sie über einen unter \_ \_ \_ \_ geordneten Zugriff auf den Objekttyp des übergeordneten Containers verfügen.
ms.assetid: 87027c25-e3c9-4bad-8df3-cb6205e40ef6
ms.tgt_platform: multiple
keywords:
- AD-Access Control und Objekt Löschung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bddcd2b563e144743689f2a26c17bd417db14ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724376"
---
# <a name="access-control-and-object-deletion"></a><span data-ttu-id="489b9-104">Löschen von Access Control und Objekten</span><span class="sxs-lookup"><span data-stu-id="489b9-104">Access Control and Object Deletion</span></span>

<span data-ttu-id="489b9-105">Active Directory Domain Services können Sie ein Objekt löschen, wenn Sie über eine der folgenden Zugriffsrechte verfügen:</span><span class="sxs-lookup"><span data-stu-id="489b9-105">Active Directory Domain Services enable you to delete an object if you have one of the following access rights:</span></span>

-   <span data-ttu-id="489b9-106">Löschen Sie den Zugriff auf das Objekt selbst.</span><span class="sxs-lookup"><span data-stu-id="489b9-106">DELETE access to the object itself</span></span>
-   <span data-ttu-id="489b9-107">ADS \_ right \_ DS \_ Löschen \_ des untergeordneten Zugriffs für diesen Objekttyp für den übergeordneten Container</span><span class="sxs-lookup"><span data-stu-id="489b9-107">ADS\_RIGHT\_DS\_DELETE\_CHILD access for that object type on the parent container</span></span>

<span data-ttu-id="489b9-108">Beachten Sie, dass das System die Sicherheits Beschreibung für das Objekt und dessen übergeordnetes Element überprüft, bevor der Löschvorgang verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="489b9-108">Be aware that the system verifies the security descriptor for both the object and its parent before denying the deletion.</span></span> <span data-ttu-id="489b9-109">Dies bedeutet, dass ein ACE, der den Lösch Zugriff für einen Benutzer explizit verweigert, keine Auswirkung hat, wenn der Benutzer \_ Zugriff auf das übergeordnete Element untergeordneter Elemente hat.</span><span class="sxs-lookup"><span data-stu-id="489b9-109">This means that an ACE that explicitly denies DELETE access to a user has no effect if the user has DELETE\_CHILD access on the parent.</span></span> <span data-ttu-id="489b9-110">Ebenso kann ein ACE, der \_ den Zugriff auf das übergeordnete Element löschen verweigert, überschrieben werden, wenn für das Objekt selbst der Lösch Zugriff zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="489b9-110">Similarly, an ACE that denies DELETE\_CHILD access on the parent can be overridden if DELETE access is allowed on the object itself.</span></span>

<span data-ttu-id="489b9-111">Zum Ausführen eines Struktur-DELETE-Vorgangs (z. b. mit der [**iadsdeleteops::D eleteobject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) -Methode) benötigen Sie ADS, die den \_ \_ \_ \_ Zugriff auf das Objekt mit der rechten DS-Berechtigung "Löschen" haben.</span><span class="sxs-lookup"><span data-stu-id="489b9-111">To perform a tree-delete operation, for example using the [**IADsDeleteOps::DeleteObject**](/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject) method, you must have ADS\_RIGHT\_DS\_DELETE\_TREE access to the object.</span></span> <span data-ttu-id="489b9-112">Wenn Sie über dieses Zugriffsrecht verfügen, können Sie das Objekt und alle untergeordneten Objekte unabhängig von den Schutzmaßnahmen für die untergeordneten Objekte löschen.</span><span class="sxs-lookup"><span data-stu-id="489b9-112">If you have this access right, you can delete the object and any child objects regardless of the protections on the child objects.</span></span> <span data-ttu-id="489b9-113">Um eine Struktur zu löschen, wenn Sie nicht über Werbeeinblendungen zum \_ \_ Löschen der Struktur verfügen \_ \_ , müssen Sie die Struktur rekursiv durchlaufen und die einzelnen Objekte einzeln löschen.</span><span class="sxs-lookup"><span data-stu-id="489b9-113">To delete a tree if you do not have ADS\_RIGHT\_DS\_DELETE\_TREE access, you must recursively traverse the tree, deleting each object individually.</span></span> <span data-ttu-id="489b9-114">In diesem Fall müssen Sie \_ für jedes Objekt in der Struktur über den erforderlichen untergeordneten Zugriff zum Löschen oder Löschen verfügen.</span><span class="sxs-lookup"><span data-stu-id="489b9-114">In this case, you must have the necessary DELETE or DELETE\_CHILD access for each object in the tree.</span></span>

> [!WARNING]
> <span data-ttu-id="489b9-115">Wenn Benutzer über ADS verfügen, die über die Berechtigung zum \_ \_ \_ Löschen \_ von Struktur Zugriff für ein Objekt verfügen, können Sie dadurch eine gesamte Unterstruktur löschen, einschließlich aller untergeordneten Objekte.</span><span class="sxs-lookup"><span data-stu-id="489b9-115">If users have ADS\_RIGHT\_DS\_DELETE\_TREE access for an object, this gives them the ability to delete a whole subtree, including all child objects.</span></span> <span data-ttu-id="489b9-116">Aus diesem Grund können Sie das Aufheben der Zugriffsberechtigung "Unterstruktur löschen" für alle Benutzer eines übergeordneten Containers in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="489b9-116">For this reason, you may consider revoking "Delete Subtree" access permission for all users on a parent container.</span></span>

 

 

 