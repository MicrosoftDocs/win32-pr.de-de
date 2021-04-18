---
description: 'Das folgende Beispiel zeigt die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage:'
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344263"
---
# <a name="select-statement"></a><span data-ttu-id="567bc-103">SELECT-Anweisung</span><span class="sxs-lookup"><span data-stu-id="567bc-103">SELECT Statement</span></span>

<span data-ttu-id="567bc-104">Das folgende Beispiel zeigt die grundlegende Syntax der SELECT-Anweisung für eine lokale Abfrage:</span><span class="sxs-lookup"><span data-stu-id="567bc-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="567bc-105">Das folgende Beispiel zeigt den Spalten Teil der Syntax der SELECT-Anweisung:</span><span class="sxs-lookup"><span data-stu-id="567bc-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="567bc-106">Die Spalten Spezifizierer müssen gültige Eigenschaftsnamen Spalten sein, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="567bc-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="567bc-107">Gültige Spaltennamen sind registrierte Eigenschafts Beschreibungen oder werden durch das Eigenschafts System Schema der Shell definiert.</span><span class="sxs-lookup"><span data-stu-id="567bc-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="567bc-108">Sie können nur die Spalten auswählen, die im Schema des Eigenschaften Systems als abrufbar gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="567bc-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="567bc-109">Wenn Sie gemischte Schreibweise verwenden, um Eigenschaften zu identifizieren, bei denen es sich nicht um System definierte Eigenschaften handelt, müssen Sie den Spaltenspezifizierer in doppelte Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="567bc-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="567bc-110">System definierte Eigenschaftsnamen enthalten alle Eigenschaften, die mit "System" beginnen (z. b. System. Contact. FirstName), und erfordern keine Anführungszeichen.</span><span class="sxs-lookup"><span data-stu-id="567bc-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="567bc-111">Sie können für die Lesbarkeit auch System definierte Eigenschaftsnamen in doppelte Anführungszeichen einschließen.</span><span class="sxs-lookup"><span data-stu-id="567bc-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="567bc-112">Dies hat keine Auswirkung auf die Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="567bc-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="567bc-113">Wenn die Abfrage ein Dokument zurückgibt, das nicht die angeforderte Spalte enthält, ist der Wert dieser Spalte für das Dokument **null**.</span><span class="sxs-lookup"><span data-stu-id="567bc-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="567bc-114">Sie müssen mindestens einen Spaltennamen in einer SELECT-Anweisung angeben.</span><span class="sxs-lookup"><span data-stu-id="567bc-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="567bc-115">In der Structured Query Language (SQL)-Abfrage dürfen Sie das Sternchen () verwenden, \* um anzugeben, dass alle Spalten in einer Tabelle zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="567bc-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="567bc-116">Allerdings gelten für alle Dokumente keine definierten und festgelegten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="567bc-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="567bc-117">Aus diesem Grund ist das SQL-Sternchen im <columns> Spezifizierer der SELECT-Anweisung nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="567bc-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="567bc-118">Erzielen der Top-n-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="567bc-118">Getting the Top n Results</span></span>

<span data-ttu-id="567bc-119">Sie können mit der Top-Syntax eine maximale Anzahl von Ergebnissen angeben, die zurückgegeben werden sollen:</span><span class="sxs-lookup"><span data-stu-id="567bc-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="567bc-120">Umwandeln von Spaltendatentypen</span><span class="sxs-lookup"><span data-stu-id="567bc-120">Casting Column Data Types</span></span>

<span data-ttu-id="567bc-121">Manchmal müssen Sie Zeichen folgen Daten, die aus Dokumenten extrahiert werden, als einen anderen Datentyp umwandeln, damit ein entsprechender Vergleich erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="567bc-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="567bc-122">Weitere Informationen finden Sie unter umwandeln [des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="567bc-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="567bc-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="567bc-123">Examples</span></span>

<span data-ttu-id="567bc-124">In den folgenden Beispielen werden der Name und die URL der übereinstimmenden Dokumente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="567bc-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="567bc-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="567bc-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="567bc-126">**Licher**</span><span class="sxs-lookup"><span data-stu-id="567bc-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="567bc-127">Umwandeln des Datentyps einer Spalte</span><span class="sxs-lookup"><span data-stu-id="567bc-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="567bc-128">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="567bc-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="567bc-129">[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="567bc-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



