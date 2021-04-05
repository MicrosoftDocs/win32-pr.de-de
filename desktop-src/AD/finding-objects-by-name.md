---
title: Suchen nach Objekten nach Namen
description: Die meisten Objekte in Active Directory Domain Services die CN-Eigenschaft als Benennungs Attribut verwenden.
ms.assetid: c5df7403-23bc-440e-8cd6-215ab8037aed
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, suchen, nach Namen
- Objekt-AD, Suche nach Name
- Suchen nach Objekten nach Namen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914faa443402a1d20698aabaf0bf4a112279a322
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707619"
---
# <a name="finding-objects-by-name"></a><span data-ttu-id="1ffe0-106">Suchen nach Objekten nach Namen</span><span class="sxs-lookup"><span data-stu-id="1ffe0-106">Finding Objects by Name</span></span>

<span data-ttu-id="1ffe0-107">Die meisten Objekte in Active Directory Domain Services die **CN** -Eigenschaft als Benennungs Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-107">Most objects in Active Directory Domain Services use the **cn** property as their naming attribute.</span></span> <span data-ttu-id="1ffe0-108">Einige Objekte verwenden jedoch ein anderes Namensattribut als **CN**.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-108">Some objects, however, use a naming attribute other than **cn**.</span></span> <span data-ttu-id="1ffe0-109">Ein Domänen Controller verwendet beispielsweise die **domainDns** -Eigenschaft für das Naming-Attribut, und eine Organisationseinheit verwendet die **OrganizationalUnit** -Eigenschaft für das Naming-Attribut.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-109">For example, a domain controller uses the **domainDNS** property for the naming attribute and an organizational unit uses the **organizationalUnit** property for the naming attribute.</span></span> <span data-ttu-id="1ffe0-110">Um zu vermeiden, dass ein anderes Naming-Attribut für verschiedene Objekttypen verwendet werden muss, sollte die **Name** -Eigenschaft, die den relativen Distinguished Name des Objekts enthält, für die Suche nach Objekten nach Namen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-110">To avoid having to use a different naming attribute for different object types, the **name** property, which contains the relative distinguished name of the object, should be used to search for objects by name.</span></span>

## <a name="examples"></a><span data-ttu-id="1ffe0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ffe0-111">Examples</span></span>

<span data-ttu-id="1ffe0-112">Die folgenden Codebeispiele zeigen verschiedene Abfrage Zeichenfolgen, die verwendet werden können, um Objekte nach Namen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-112">The following code examples show different query strings that can be used to find objects by name.</span></span>

<span data-ttu-id="1ffe0-113">Die folgende Abfrage Zeichenfolge findet alle Objekte mit einem Namen, der mit "Jeff" beginnt.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-113">The following query string finds all objects with a name that begins with "Jeff".</span></span>


```C++
(name=Jeff*)
```



<span data-ttu-id="1ffe0-114">Die folgende Abfrage Zeichenfolge findet alle Computer Objekte mit einem Namen, der mit "geleast" oder "Corp" beginnt.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-114">The following query string finds all computer objects with a name that begins with "leased" or "corp".</span></span>


```C++
(&(objectCategory=computer)(|(name=leased*)(name=corp*)))
```



<span data-ttu-id="1ffe0-115">Die folgende Abfrage Zeichenfolge findet alle Benutzer und mit einem Namen, der mit "Karen" oder "Jeff" beginnt.</span><span class="sxs-lookup"><span data-stu-id="1ffe0-115">The following query string finds all users and with a name that begins with "Karen" or "Jeff".</span></span>


```C++
(&(&(objectClass=user)(objectCategory=person))(|(name=Karen*)(name=Jeff*)))
```



 

 




