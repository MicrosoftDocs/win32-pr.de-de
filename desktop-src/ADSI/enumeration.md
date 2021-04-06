---
title: Enumeration
description: Der Zugriff auf und die Bearbeitung von Daten mit ADSI bietet mehrere Beispiele für die-Enumeration. Sie können auch die untergeordneten Elemente von Container Objekten auflisten. Diese untergeordneten Elemente sind selbst Objekte und nicht nur Eigenschaften von Objekten.
ms.assetid: 1db19b00-8e43-4fc0-9099-1a1135219600
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Beispielcode Visual Basic, verwenden von IADsContainer zum Aufzählen von Objekten
- Container ADSI, verwenden von IADsContainer zum Aufzählen von untergeordneten Elementen des Containers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ba90e86282939486b79ee09cd17352841e733e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947348"
---
# <a name="enumeration"></a><span data-ttu-id="87592-107">Enumeration</span><span class="sxs-lookup"><span data-stu-id="87592-107">Enumeration</span></span>

<span data-ttu-id="87592-108">Der [Zugriff auf und die Bearbeitung von Daten mit ADSI](accessing-and-manipulating-data-with-adsi.md) bietet mehrere Beispiele für die-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="87592-108">[Accessing and Manipulating Data with ADSI](accessing-and-manipulating-data-with-adsi.md) provides several examples of enumeration.</span></span> <span data-ttu-id="87592-109">Sie können auch die untergeordneten Elemente von Container Objekten auflisten.</span><span class="sxs-lookup"><span data-stu-id="87592-109">You can also enumerate the children of container objects.</span></span> <span data-ttu-id="87592-110">Diese untergeordneten Elemente sind selbst Objekte und nicht nur Eigenschaften von Objekten.</span><span class="sxs-lookup"><span data-stu-id="87592-110">These children are objects themselves, rather than just properties on objects.</span></span>

<span data-ttu-id="87592-111">Im folgenden Beispiel wird die [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) -Schnittstelle verwendet, um die untergeordneten Elemente des Containers aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="87592-111">The following example uses the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface to enumerate the children of the container.</span></span>


```VB
Dim Container as IADsContainer
Dim Child as IADs

Set Container = GetObject("LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com")
 
For Each Child in Container
     Debug.Print Child.Name
Next Child
```



 

 




