---
description: ICE98 überprüft das Beschreibungsfeld der ODBCDatasource-Tabelle für eine ODBC-Datenquelle. Er verwendet die sqlvaliddsn-Funktion, um zu überprüfen, ob nur gültige Zeichen verwendet werden, und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.
ms.assetid: ed78db96-10a1-4e42-9147-2309c9ca9c6e
title: ICE98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf06e97341bd8f15502b1ea1fe43a975dc9cde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216568"
---
# <a name="ice98"></a><span data-ttu-id="19527-104">ICE98</span><span class="sxs-lookup"><span data-stu-id="19527-104">ICE98</span></span>

<span data-ttu-id="19527-105">ICE98 überprüft das Beschreibungsfeld der [ODBCDatasource-Tabelle](odbcdatasource-table.md) für eine ODBC-Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="19527-105">ICE98 verifies the description field of the [ODBCDataSource Table](odbcdatasource-table.md) for an ODBC data source.</span></span> <span data-ttu-id="19527-106">Er verwendet die **sqlvaliddsn** -Funktion, um zu überprüfen, ob nur gültige Zeichen verwendet werden, und dass die Beschreibung die maximal zulässige Länge nicht überschreitet.</span><span class="sxs-lookup"><span data-stu-id="19527-106">It uses the **SQLValidDSN** function to check that only valid characters are used, and that the description does not exceed the maximum allowed length.</span></span>

## <a name="result"></a><span data-ttu-id="19527-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="19527-107">Result</span></span>

<span data-ttu-id="19527-108">ICE98 gibt die folgenden Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="19527-108">ICE98 posts the following warnings.</span></span>



| <span data-ttu-id="19527-109">ICE98-Warnung</span><span class="sxs-lookup"><span data-stu-id="19527-109">ICE98 warning</span></span>                    | <span data-ttu-id="19527-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19527-110">Description</span></span>                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19527-111">Der Datenquellen Name ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="19527-111">The data source name is invalid.</span></span> | <span data-ttu-id="19527-112">Der Wert in der Spalte "Beschreibung" der [Tabelle "ODBCDatasource](odbcdatasource-table.md) " enthält entweder ungültige Zeichen oder ist zu lang. Dies bedeutet, dass die maximale SQL- \_ \_ DSN- \_ Länge von 32 überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="19527-112">The value in the Description column of the [ODBCDataSource Table](odbcdatasource-table.md) either contains invalid characters or is too long, which means that it exceeds the SQL\_MAX\_DSN\_LENGTH of 32.</span></span> |



 

## <a name="example"></a><span data-ttu-id="19527-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="19527-113">Example</span></span>

<span data-ttu-id="19527-114">ICE98 meldet die folgenden Warnungen für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="19527-114">ICE98 reports the following warnings for the example:</span></span>

``` syntax
The data source name is invalid: !
The data source name is invalid: <String of length > 32>
```

<span data-ttu-id="19527-115">[ODBCDatasource-Tabelle](odbcdatasource-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="19527-115">[ODBCDataSource Table](odbcdatasource-table.md) (partial)</span></span>



| <span data-ttu-id="19527-116">DataSource</span><span class="sxs-lookup"><span data-stu-id="19527-116">DataSource</span></span> | <span data-ttu-id="19527-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="19527-117">Description</span></span>                      |
|------------|----------------------------------|
| <span data-ttu-id="19527-118">Badchar</span><span class="sxs-lookup"><span data-stu-id="19527-118">BadChar</span></span>    | <span data-ttu-id="19527-119">!</span><span class="sxs-lookup"><span data-stu-id="19527-119">!</span></span>                                |
| <span data-ttu-id="19527-120">Toolong</span><span class="sxs-lookup"><span data-stu-id="19527-120">TooLong</span></span>    | <span data-ttu-id="19527-121"><String of length > 32></span><span class="sxs-lookup"><span data-stu-id="19527-121"><String of length > 32></span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="19527-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19527-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19527-123">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="19527-123">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="19527-124">ODBCDatasource-Tabelle</span><span class="sxs-lookup"><span data-stu-id="19527-124">ODBCDataSource Table</span></span>](odbcdatasource-table.md)
</dt> </dl>

 

 



