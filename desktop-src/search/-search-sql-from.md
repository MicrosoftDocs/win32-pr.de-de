---
description: Nach der SELECT-Anweisung verwenden Sie die from-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll.
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346281"
---
# <a name="from-clause"></a><span data-ttu-id="540fc-103">FROM-Klausel</span><span class="sxs-lookup"><span data-stu-id="540fc-103">FROM Clause</span></span>

<span data-ttu-id="540fc-104">Nach der SELECT-Anweisung verwenden Sie die from-Klausel, um anzugeben, wo nach übereinstimmenden Dokumenten gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="540fc-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="540fc-105">Im folgenden finden Sie die Syntax der from-Klausel für eine lokale Abfrage:</span><span class="sxs-lookup"><span data-stu-id="540fc-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="540fc-106">Derzeit unterstützt Windows Search nur einen Katalog, SystemIndex.</span><span class="sxs-lookup"><span data-stu-id="540fc-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="540fc-107">Um den lokalen Katalog eines Remote Computers abzufragen, müssen Sie den Computernamen vor dem Katalog und einen Universal Naming Convention (UNC)-Pfad auf dem Remote Computer in der Scope-oder Directory-Klausel einschließen.</span><span class="sxs-lookup"><span data-stu-id="540fc-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="540fc-108">Sie geben einen Gültigkeitsbereich als Einschränkung in der WHERE-Klausel an, wie im Thema [Geltungsbereich und Verzeichnis Prädikate](-search-sql-folderdepth.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="540fc-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="540fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="540fc-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="540fc-110">Im zweiten der vorangegangenen Beispiele ist die Abfrage auf einen Remote Computer mit dem Namen "zarascomputer" ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="540fc-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="540fc-111">Beachten Sie, dass dieser Computername in der from-Klausel und der Scope-Klausel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="540fc-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="540fc-112">Im dritten Beispiel zielt die Abfrage auf einen Freigabe Namen "Users" auf einem Server mit dem Namen "Server" (wobei der UNC-Pfad \\ \\ Server \\ Benutzer lauten würde).</span><span class="sxs-lookup"><span data-stu-id="540fc-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="540fc-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="540fc-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="540fc-114">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="540fc-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="540fc-115">Übersicht über die SQL-Such Syntax</span><span class="sxs-lookup"><span data-stu-id="540fc-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="540fc-116">SELECT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="540fc-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="540fc-117">WHERE-Klausel</span><span class="sxs-lookup"><span data-stu-id="540fc-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="540fc-118">Bereichs-und Verzeichnis Prädikate</span><span class="sxs-lookup"><span data-stu-id="540fc-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



