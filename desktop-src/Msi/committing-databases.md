---
description: Änderungen an der Installations Datenbank werden erst dann in die Datenbank geschrieben, wenn Sie msidatabasecommit aufgerufen haben.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Commit für Datenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866724"
---
# <a name="committing-databases"></a><span data-ttu-id="d4a99-103">Commit für Datenbanken</span><span class="sxs-lookup"><span data-stu-id="d4a99-103">Committing Databases</span></span>

<span data-ttu-id="d4a99-104">Änderungen an der Installations Datenbank werden erst dann in die Datenbank geschrieben, wenn Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="d4a99-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="d4a99-105">**So stellen Sie sicher, dass in einer Datenbank vorgenommene Änderungen abgeschlossen werden**</span><span class="sxs-lookup"><span data-stu-id="d4a99-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="d4a99-106">Überprüfen Sie, ob eine Tabelle geschrieben wird, wenn Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) aufrufen, indem Sie [**msidatabaseistablepersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="d4a99-107">Ruft die [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) -Funktion auf, um Änderungen an der Datenbank abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="d4a99-108">Änderungen, die in einer Datenbank vorgenommen werden, werden akkumuliert und nicht in der eigentlichen Datenbank wiedergegeben, bis Sie [**msidatabasecommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="d4a99-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="d4a99-109">Für temporäre Spalten oder Zeilen wird kein Commit an die Datenbank ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a99-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="d4a99-110">Wenn eine Datenbank geschlossen wird, wird für alle seit dem letzten **msidatabasecommit** vorgenommenen Änderungen automatisch ein Rollback ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a99-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



