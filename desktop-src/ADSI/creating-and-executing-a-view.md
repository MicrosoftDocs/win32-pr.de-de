---
title: Erstellen und Ausführen einer Ansicht
description: Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden. Beachten Sie, dass nur die Sicht Definition in SQL Server und nicht im eigentlichen Resultset gespeichert wird. Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387964"
---
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="275b4-105">Erstellen und Ausführen einer Ansicht</span><span class="sxs-lookup"><span data-stu-id="275b4-105">Creating and Executing a View</span></span>

<span data-ttu-id="275b4-106">Sie können eine Ansicht für Daten erstellen, die aus Active Directory abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="275b4-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="275b4-107">Beachten Sie, dass nur die Sicht Definition in SQL Server und nicht im eigentlichen Resultset gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="275b4-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="275b4-108">Daher erhalten Sie möglicherweise ein anderes Ergebnis, wenn Sie die Ansicht zu einem späteren Zeitpunkt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="275b4-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="275b4-109">Im folgenden Codebeispiel wird gezeigt, wie eine Sicht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="275b4-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="275b4-110">Verwenden Sie den folgenden Code, um eine Ansicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="275b4-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="275b4-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="275b4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="275b4-112">Erstellen eines heterogenen Joins zwischen SQL Server und Active Directory</span><span class="sxs-lookup"><span data-stu-id="275b4-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




