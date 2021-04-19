---
description: Der Like-Operator bestimmt, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Like-Operator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355636"
---
# <a name="like-operator"></a><span data-ttu-id="a8aa9-103">Like-Operator</span><span class="sxs-lookup"><span data-stu-id="a8aa9-103">LIKE Operator</span></span>

<span data-ttu-id="a8aa9-104">Der Like-Operator bestimmt, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="a8aa9-105">Das angegebene Muster kann genau die Zeichen enthalten, die übereinstimmen müssen, oder es kann Meta-Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="a8aa9-106">Der Like-Operator gleicht die Teil Zeichenfolgen in der folgenden Tabelle mit den Platzhalter Zeichen ab.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="a8aa9-107">Zeichen</span><span class="sxs-lookup"><span data-stu-id="a8aa9-107">Character</span></span>       | <span data-ttu-id="a8aa9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8aa9-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8aa9-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="a8aa9-109">\[ \]</span></span>           | <span data-ttu-id="a8aa9-110">Ein beliebiges Zeichen innerhalb des angegebenen Bereichs ( \[ a-f \] ) oder Set ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="a8aa9-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="a8aa9-111">Ein beliebiges Zeichen, das nicht innerhalb des Bereichs ( \[ ^ a-f \] ) oder der festgelegten Menge ( \[ ^ abcdef \] ) liegt.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="a8aa9-112">Eine beliebige Zeichenfolge mit 0 (null) oder mehr Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="a8aa9-113">Im folgenden Beispiel werden alle-Instanzen gesucht, bei denen "Win" an einer beliebigen Stelle im Klassennamen gefunden wird: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="a8aa9-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="a8aa9-114">\_ (Unterstrich)</span><span class="sxs-lookup"><span data-stu-id="a8aa9-114">\_ (underscore)</span></span> | <span data-ttu-id="a8aa9-115">Ein beliebiges Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-115">Any one character.</span></span> <span data-ttu-id="a8aa9-116">Jeder Literale unterstrich, der in der Abfrage Zeichenfolge verwendet wird, muss mit Escapezeichen versehen werden \[ \] (eckige Klammern).</span><span class="sxs-lookup"><span data-stu-id="a8aa9-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="a8aa9-117">Beispielsweise ruft der folgende PowerShell-Code alle Instanzen der Win32- **\_ OperatingSystem** -Klasse ab, deren **Name** -Eigenschaft mit **FirstName** beginnt:</span><span class="sxs-lookup"><span data-stu-id="a8aa9-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="a8aa9-118">Da der Unterstrich ein Meta-Zeichen ist, muss die Escapezeichen, wenn das Abfrage Ziel einen Unterstrich aufweist, \[ \] umschließen.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="a8aa9-119">Beispielsweise können Sie alle Klassen Abfragen, die einen doppelten Unterstrich im Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="a8aa9-120">Wenn Sie alle Klassen mit einem doppelten Unterstrich im Namen suchen möchten, müssen Sie beide Unterstriche mit \[ \] (eckigen Klammern) versehen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="a8aa9-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="a8aa9-121">Sie können eine like-Anweisung mit Not negieren. Stellen Sie zu diesem Zweck sicher, dass nicht direkt vor dem Feldnamen steht.</span><span class="sxs-lookup"><span data-stu-id="a8aa9-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="a8aa9-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a8aa9-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="a8aa9-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8aa9-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8aa9-124">WQL-Operatoren</span><span class="sxs-lookup"><span data-stu-id="a8aa9-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



