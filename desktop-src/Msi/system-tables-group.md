---
description: In den Tabellen der Gruppe Systemtabellen werden die Tabellen und Spalten der-Installations Datenbank nachverfolgt.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: System Tabellen Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130269"
---
# <a name="system-tables-group"></a><span data-ttu-id="3dbc5-103">System Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="3dbc5-103">System Tables Group</span></span>

<span data-ttu-id="3dbc5-104">In den Tabellen der Gruppe Systemtabellen werden die Tabellen und Spalten der-Installations Datenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="3dbc5-105">In der [ \_ Tabelle](-tables-table.md) Tabellen werden alle Tabellen in der-Datenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="3dbc5-106">Dies schließt Tabellen ein, die Sie möglicherweise für Ihre eigenen benutzerdefinierten Aktionen erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="3dbc5-107">Fragen Sie diese Tabelle ab, um herauszufinden, ob eine Tabelle vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="3dbc5-108">In der [ \_ Spalten Tabelle](-columns-table.md) werden die Spalten in der-Installations Datenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="3dbc5-109">Temporäre Spalten werden zurzeit von dieser Tabelle nicht nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="3dbc5-110">Fragen Sie diese Tabelle ab, um herauszufinden, ob eine bestimmte Spalte vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="3dbc5-111">In der [ \_ Tabelle Streams](-streams-table.md) werden eingebettete OLE-Datenströme aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="3dbc5-112">In der [ \_ Tabelle Storages](-storages-table.md) werden eingebettete OLE-Datenspeicher aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="3dbc5-113">Die [ \_ Validierungs Tabelle](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="3dbc5-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="3dbc5-114">\_In der Validierungs Tabelle werden die Typen und die zulässigen Bereiche aller Spalten in der Datenbank nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="3dbc5-115">Die \_ Validierungs Tabelle wird während des Daten Bank Überprüfungsprozesses verwendet, um sicherzustellen, dass alle Spalten berücksichtigt werden und die richtigen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="3dbc5-116">Diese Tabelle wird nicht mit der Installer-Datenbank ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="3dbc5-116">This table is not shipped with the installer database.</span></span>

 

 



