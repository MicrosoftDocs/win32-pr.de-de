---
description: 'Weitere Informationen finden Sie unter: Order By-Klausel.'
ms.assetid: e720cf0d-b034-48e2-a13e-e97dd23b2beb
title: ORDER BY-Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eaa3c834ca2fe04222ef2ae452a0119bf391b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128536"
---
# <a name="order-by-clause"></a><span data-ttu-id="2cb1f-103">ORDER BY-Klausel</span><span class="sxs-lookup"><span data-stu-id="2cb1f-103">ORDER BY Clause</span></span>

<span data-ttu-id="2cb1f-104">Die Order By-Klausel sortiert die Ergebnisse basierend auf dem Wert einer oder mehrerer Spalten, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-104">The ORDER BY clause sorts the results based on the value of one or more columns you specify.</span></span> <span data-ttu-id="2cb1f-105">Im folgenden finden Sie die Syntax der ORDER BY-Klausel:</span><span class="sxs-lookup"><span data-stu-id="2cb1f-105">Following is the syntax of the ORDER BY clause:</span></span>


```
ORDER BY <column> [<direction>] [,<column> [<direction>]]
```



<span data-ttu-id="2cb1f-106">Der Spaltenspezifizierer muss eine gültige Spalte sein.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-106">The column specifier must be a valid column.</span></span> <span data-ttu-id="2cb1f-107">Sie können den Spalten Bezeichner verwenden, um auf Spalten in der Reihenfolge zu verweisen, in der Sie in der Abfrage angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-107">You can use the column specifier to refer to columns by the order that they appear in the query.</span></span> <span data-ttu-id="2cb1f-108">Die erste Spalte in der Abfrage wird mit 1 nummeriert.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-108">The first column in the query is numbered 1.</span></span> <span data-ttu-id="2cb1f-109">Sie können mehr als eine Spalte in der ORDER BY-Klausel einschließen, getrennt durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-109">You can include more than one column in the ORDER BY clause, separated by commas.</span></span>

<span data-ttu-id="2cb1f-110">Der optionale richtungsspezifizierer kann entweder "ASC" für aufsteigend (niedrig zu hoch) oder "absteigend" (hoch bis niedrig) sein.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-110">The optional direction specifier can be either "ASC" for ascending (low to high) or "DESC" for descending (high to low).</span></span> <span data-ttu-id="2cb1f-111">Wenn Sie keinen richtungsspezifizierer angeben, wird der Standardwert aufsteigend verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-111">If you do not provide a direction specifier, the default, ascending, is used.</span></span> <span data-ttu-id="2cb1f-112">Wenn Sie mehr als eine Spalte angeben, aber nicht alle Richtungen angeben, wird die von Ihnen angegebene Richtung auf jede Spalte angewendet, bis Sie die Richtung explizit ändern.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-112">If you specify more than one column, but do not specify all directions, the direction you specify last is applied to each column until you explicitly change the direction.</span></span>

<span data-ttu-id="2cb1f-113">In der folgenden Order By-Klausel werden z. B. die Spalten A, B, C und G in aufsteigender Reihenfolge sortiert, während die Spalten D, E und F in absteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="2cb1f-113">For example, in the following ORDER BY clause, the columns A, B, C, and G are sorted in ascending order, while columns D, E, and F are sorted in descending order.</span></span>


```
ORDER BY A ASC, B, C, D DESC, E, F, G ASC
```



## <a name="related-topics"></a><span data-ttu-id="2cb1f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2cb1f-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2cb1f-115">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="2cb1f-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2cb1f-116">FROM-Klausel</span><span class="sxs-lookup"><span data-stu-id="2cb1f-116">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="2cb1f-117">Rank by-Klausel</span><span class="sxs-lookup"><span data-stu-id="2cb1f-117">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

[<span data-ttu-id="2cb1f-118">SELECT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="2cb1f-118">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

<span data-ttu-id="2cb1f-119">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2cb1f-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2cb1f-120">Voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="2cb1f-120">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="2cb1f-121">Nicht-voll Text Prädikate</span><span class="sxs-lookup"><span data-stu-id="2cb1f-121">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



