---
description: ICE06 prüft jede Tabelle, um zu überprüfen, ob alle in der \_ Validierungs Tabelle aufgeführten Spalten in der Tabelle vorhanden sind. Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungs Einträge für diese Tabelle ignoriert.
ms.assetid: 0c3f21ae-49ea-4cfe-b465-6fdc2b19cbb9
title: ICE06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9442d9b2c4089b88299106de875074bd7b0625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960044"
---
# <a name="ice06"></a><span data-ttu-id="92d6d-104">ICE06</span><span class="sxs-lookup"><span data-stu-id="92d6d-104">ICE06</span></span>

<span data-ttu-id="92d6d-105">ICE06 prüft jede Tabelle, um zu überprüfen, ob alle in der [ \_ Validierungs Tabelle](-validation-table.md) aufgeführten Spalten in der Tabelle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="92d6d-105">ICE06 checks every table to validate that all the columns listed in the [\_Validation table](-validation-table.md) are present in the table.</span></span> <span data-ttu-id="92d6d-106">Wenn keine Tabelle vorhanden ist, werden alle \_ Validierungs Einträge für diese Tabelle ignoriert.</span><span class="sxs-lookup"><span data-stu-id="92d6d-106">If a table does not exist, any \_Validation entries for that table are ignored.</span></span>

<span data-ttu-id="92d6d-107">Der Zweck von ICE06 besteht darin, Instanzen zu erkennen, in denen ein Autor versucht, eine neue \_ Validierungs Tabelle zu verwenden, die eine Schema Änderung mit einer alten Datenbank widerspiegelt, die noch nicht aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="92d6d-107">The purpose of ICE06 is to detect instances in which an author tries to use a new \_Validation table that reflects a schema change with an old database that has not been updated.</span></span> <span data-ttu-id="92d6d-108">ICE06 erkennt auch den umgekehrten Fall einer alten \_ Validierungs Tabelle, die mit einer geänderten Datenbank verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="92d6d-108">ICE06 also detects the reverse case of an old \_Validation table being used with an altered database.</span></span>

<span data-ttu-id="92d6d-109">Beachten Sie, dass die von [ICE03](ice03.md) durchgeführte interne Validierung die Instanz einer Tabellenspalte abfängt, die in der \_ im Columns-Katalog aufgelisteten Überprüfungs Tabelle nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="92d6d-109">Note that the internal validation performed by [ICE03](ice03.md) catches the instance of a table column not defined in the \_Validation table being listed in the columns catalog.</span></span> <span data-ttu-id="92d6d-110">Durch die Verwendung von "ICE03" und "ICE06" wird sichergestellt, dass jede Spalte in der Datenbank getestet wird.</span><span class="sxs-lookup"><span data-stu-id="92d6d-110">The use of both ICE03 and ICE06 therefore ensures every column in the database is tested.</span></span>

## <a name="result"></a><span data-ttu-id="92d6d-111">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="92d6d-111">Result</span></span>

<span data-ttu-id="92d6d-112">ICE06 gibt einen Fehler aus, wenn eine Tabellenspalte in der \_ Validierungs Tabelle definiert ist, die nicht in der \_ Spalten Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="92d6d-112">ICE06 posts an error when there is a table column defined in the \_Validation table that is not listed in the \_Columns table.</span></span>

## <a name="example"></a><span data-ttu-id="92d6d-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="92d6d-113">Example</span></span>

<span data-ttu-id="92d6d-114">Im folgenden Beispiel wird die Nachricht von ICE06 gepostet.</span><span class="sxs-lookup"><span data-stu-id="92d6d-114">For the following example ICE06 posts the message</span></span>

<span data-ttu-id="92d6d-115">Column: Version der Tabelle: ModuleSignature ist nicht in der Datenbank definiert.</span><span class="sxs-lookup"><span data-stu-id="92d6d-115">Column: Version of Table: ModuleSignature is not defined in database.</span></span>

<span data-ttu-id="92d6d-116">[ \_ Validierungs Tabelle](-validation-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="92d6d-116">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="92d6d-117">Tabelle</span><span class="sxs-lookup"><span data-stu-id="92d6d-117">Table</span></span>           | <span data-ttu-id="92d6d-118">Spalte</span><span class="sxs-lookup"><span data-stu-id="92d6d-118">Column</span></span>   |
|-----------------|----------|
| <span data-ttu-id="92d6d-119">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="92d6d-119">ModuleSignature</span></span> | <span data-ttu-id="92d6d-120">ModuleID</span><span class="sxs-lookup"><span data-stu-id="92d6d-120">ModuleID</span></span> |
| <span data-ttu-id="92d6d-121">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="92d6d-121">ModuleSignature</span></span> | <span data-ttu-id="92d6d-122">Version</span><span class="sxs-lookup"><span data-stu-id="92d6d-122">Version</span></span>  |



 

<span data-ttu-id="92d6d-123">[ \_ Columns-Tabelle](-columns-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="92d6d-123">[\_Columns Table](-columns-table.md) (partial)</span></span>



| <span data-ttu-id="92d6d-124">Tabelle</span><span class="sxs-lookup"><span data-stu-id="92d6d-124">Table</span></span>           | <span data-ttu-id="92d6d-125">number</span><span class="sxs-lookup"><span data-stu-id="92d6d-125">Number</span></span> | <span data-ttu-id="92d6d-126">name</span><span class="sxs-lookup"><span data-stu-id="92d6d-126">Name</span></span>     |
|-----------------|--------|----------|
| <span data-ttu-id="92d6d-127">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="92d6d-127">ModuleSignature</span></span> | <span data-ttu-id="92d6d-128">1</span><span class="sxs-lookup"><span data-stu-id="92d6d-128">1</span></span>      | <span data-ttu-id="92d6d-129">ModuleID</span><span class="sxs-lookup"><span data-stu-id="92d6d-129">ModuleID</span></span> |



 

<span data-ttu-id="92d6d-130">Die Spalte Version der Tabelle ModuleSignature ist nicht in der Datenbank oder in der \_ Tabelle Columns aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="92d6d-130">The Version column of the ModuleSignature table is not in the database or listed in the \_Columns table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92d6d-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92d6d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92d6d-132">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="92d6d-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



