---
description: Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Abrufen eines Daten Bank Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130440"
---
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="72d00-103">Abrufen eines Daten Bank Handles</span><span class="sxs-lookup"><span data-stu-id="72d00-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="72d00-104">Bevor Sie mit einer Datenbank arbeiten, müssen Sie zunächst ein Handle dafür abrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="72d00-105">**So greifen Sie auf Informationen zu einer Installer-Datenbank zu**</span><span class="sxs-lookup"><span data-stu-id="72d00-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="72d00-106">Abrufen eines Handles für die Datenbank auf eine von zwei Arten:</span><span class="sxs-lookup"><span data-stu-id="72d00-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="72d00-107">Wenn eine Installation ausgeführt wird, rufen Sie ein Handle für die aktive Datenbank ab, indem Sie die [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="72d00-108">Wenn eine Installation nicht ausgeführt wird, öffnen Sie eine beliebige Datenbank, indem Sie die [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="72d00-109">Nachdem die Datenbank geöffnet wurde, können Sie Funktionen zum Abrufen von Informationen über die Datenbank oder zum Bearbeiten der Datenbank abrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="72d00-110">Erstellen Sie ein **View** -Objekt, und geben Sie eine SQL-Abfrage der geöffneten Datenbank an, indem Sie die [**msidatabaseopenview**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="72d00-111">Rufen Sie einen Datensatz ab, der alle Primärschlüssel einer angegebenen Tabelle in der geöffneten Datenbank enthält, indem Sie die [**msidatabasegetprimarykeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="72d00-112">Überprüfen Sie den aktuellen Status einer geöffneten Datenbank, indem Sie die [**msigetdatabasestate**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="72d00-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="72d00-113">Mit der **msigetdatabasestate** -Funktion können Sie den Lese-/Schreibstatus für eine Datenbank festlegen oder, wenn das Handle gültig ist.</span><span class="sxs-lookup"><span data-stu-id="72d00-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



