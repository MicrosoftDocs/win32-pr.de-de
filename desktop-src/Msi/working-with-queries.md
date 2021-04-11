---
description: Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Erstellen von Structured Query Language (SQL)-Abfragen an die Datenbank. Im folgenden Verfahren wird beschrieben, wie Sie SQL zum Abfragen einer Datenbank verwenden.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Arbeiten mit Abfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959976"
---
# <a name="working-with-queries"></a><span data-ttu-id="b2c33-104">Arbeiten mit Abfragen</span><span class="sxs-lookup"><span data-stu-id="b2c33-104">Working with Queries</span></span>

<span data-ttu-id="b2c33-105">Da das Installationsprogramm eine relationale Datenbank verwendet, gibt es Funktionen zum Erstellen von Structured Query Language (SQL)-Abfragen an die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b2c33-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="b2c33-106">Im folgenden Verfahren wird beschrieben, wie Sie SQL zum Abfragen einer Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="b2c33-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="b2c33-107">**So Fragen Sie eine Datenbank mit SQL ab**</span><span class="sxs-lookup"><span data-stu-id="b2c33-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="b2c33-108">Öffnen Sie das [**View**](view-object.md) -Objekt mit der entsprechenden SQL-Anweisung, indem Sie die [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="b2c33-109">Ein [**View**](view-object.md) -Objekt ist die logische Tabelle, die durch Anwenden einer Abfrage auf einen Tabellen Satz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c33-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="b2c33-110">SQL-Abfragen müssen der vom Installationsprogramm bereitgestellten [SQL-Syntax](sql-syntax.md) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="b2c33-111">Diese SQL-Anweisung kann Parameter Markierungen enthalten, die nicht angegeben sind, bis das **View** -Objekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b2c33-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="b2c33-112">Führen Sie das [**View**](view-object.md) -Objekt aus, indem Sie die [**msiviewexecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="b2c33-113">Rufen Sie den nächsten Datensatz aus einem [**Ansichts**](view-object.md) Objekt ab, indem Sie die [**msiviewfetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="b2c33-114">Ändern Sie das [**Ansichts**](view-object.md) Objekt, indem Sie die [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="b2c33-115">Sie können auch Daten mit [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) validieren, indem Sie die entsprechenden Flags übergeben.</span><span class="sxs-lookup"><span data-stu-id="b2c33-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="b2c33-116">Wenn **msiviewmodify** \_ ungültige \_ Daten aus einer Validierungs Anforderung zurückgibt, sind die zugrunde liegenden Daten beschädigt.</span><span class="sxs-lookup"><span data-stu-id="b2c33-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="b2c33-117">Rufen Sie ausführliche Fehlerinformationen zum [**View**](view-object.md) -Objekt ab, indem Sie die [**msiviewgeterror**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="b2c33-118">Schließen Sie das [**Ansichts**](view-object.md) Objekt, indem Sie die [**msiviewclose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b2c33-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="b2c33-119">Weitere Informationen finden Sie unter [Beispiele für Datenbankabfragen mit SQL und Skript](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="b2c33-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



