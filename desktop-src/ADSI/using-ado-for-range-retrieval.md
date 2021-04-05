---
title: Verwenden von ADO für den Bereichs Abruf
description: Wenn eine Automatisierungs Sprache verwendet wird, sollte die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden. Wenn ADO für den Bereichs Abruf verwendet wird, besteht ein Problem, das speziell behandelt werden muss.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Verwenden von ADO für den Bereichs Abruf (ADSI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707367"
---
# <a name="using-ado-for-range-retrieval"></a><span data-ttu-id="d0bcd-104">Verwenden von ADO für den Bereichs Abruf</span><span class="sxs-lookup"><span data-stu-id="d0bcd-104">Using ADO for Range Retrieval</span></span>

<span data-ttu-id="d0bcd-105">Wenn eine Automatisierungs Sprache verwendet wird, sollte die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-105">If an automation language is used, the ActiveX Directory Objects (ADO) should be used to retrieve a range of property values.</span></span>

<span data-ttu-id="d0bcd-106">Wenn ADO für den Bereichs Abruf verwendet wird, besteht ein Problem, das speziell behandelt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-106">When using ADO for range retrieval, there is one problem that must be specifically addressed.</span></span> <span data-ttu-id="d0bcd-107">Beim Abfragen der endgültigen Gruppe von Eigenschafts Werten Ruft das ADO-Objekt NULL-Objekte ab, auch wenn mehr übrig sind.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-107">When querying for the final group of property values, the ADO object will retrieve zero objects, even though more remain.</span></span> <span data-ttu-id="d0bcd-108">Um die restlichen Werte abzurufen, verwenden Sie den Bereichs Platzhalter " \* ".</span><span class="sxs-lookup"><span data-stu-id="d0bcd-108">To retrieve the remaining values, use the range wildcard '\*'.</span></span> <span data-ttu-id="d0bcd-109">Wenn eine Gruppe z. b. 150 Mitglieder enthält, können die Mitglieds Werte 0-100 normalerweise mithilfe des Bereichs Abrufs abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-109">For example, if a group contains 150 members, member values 0-100 can be retrieved normally using ranged retrieval.</span></span> <span data-ttu-id="d0bcd-110">Wenn der Bereich 101-200 dann angefordert wird, gibt das ADO-Objekt NULL-Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-110">If range 101-200 is then requested, the ADO object will return zero objects.</span></span> <span data-ttu-id="d0bcd-111">An diesem Punkt ist es erforderlich, die Abfrage in den Anforderungs Bereich 101-zu ändern \* .</span><span class="sxs-lookup"><span data-stu-id="d0bcd-111">At this point, it is necessary to modify the query to request range 101-\*.</span></span> <span data-ttu-id="d0bcd-112">Dadurch werden Werte von 101 zu 150 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d0bcd-112">This will retrieve values from 101 to 150.</span></span> <span data-ttu-id="d0bcd-113">Weitere Informationen und ein Codebeispiel finden Sie unter [Beispielcode für die Verwendung von Bereichen zum Abrufen von Mitgliedern einer Gruppe](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span><span class="sxs-lookup"><span data-stu-id="d0bcd-113">For more information and a code example, see [Example Code for Using Ranging to Retrieve Members of a Group](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).</span></span>

<span data-ttu-id="d0bcd-114">Weitere Informationen zur Verwendung von ADO für den Bereichs Abruf finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d0bcd-114">For more information about using ADO for range retrieval, see:</span></span>

-   [<span data-ttu-id="d0bcd-115">ADO LDAP-Bereich-Dialekt</span><span class="sxs-lookup"><span data-stu-id="d0bcd-115">ADO LDAP Ranging Dialect</span></span>](ado-ldap-ranging-dialect.md)
-   [<span data-ttu-id="d0bcd-116">ADO-SQL-Bereich-Dialekt</span><span class="sxs-lookup"><span data-stu-id="d0bcd-116">ADO SQL Ranging Dialect</span></span>](ado-sql-ranging-dialect.md)
-   [<span data-ttu-id="d0bcd-117">Beispiel Code für die Verwendung von Bereichen zum Abrufen von Mitgliedern einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="d0bcd-117">Example Code for Using Ranging to Retrieve Members of a Group</span></span>](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




