---
description: Weitere Informationen finden Sie unter Verwenden der Extensible Storage-Engine
title: Verwenden der Extensible Storage-Engine
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349110"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="f34da-103">Verwenden der Extensible Storage-Engine</span><span class="sxs-lookup"><span data-stu-id="f34da-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="f34da-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f34da-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="f34da-105">Verwenden der Extensible Storage-Engine</span><span class="sxs-lookup"><span data-stu-id="f34da-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="f34da-106">Dieser Abschnitt enthält allgemeine Informationen zur Verwendung der folgenden Teile der ESE-API.</span><span class="sxs-lookup"><span data-stu-id="f34da-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="f34da-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="f34da-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="f34da-108">Indizierung in der Tabelle</span><span class="sxs-lookup"><span data-stu-id="f34da-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="f34da-109">Erstellen von Datenbanken</span><span class="sxs-lookup"><span data-stu-id="f34da-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="f34da-110">Transaktionen</span><span class="sxs-lookup"><span data-stu-id="f34da-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="f34da-111">ESE-Fehler</span><span class="sxs-lookup"><span data-stu-id="f34da-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="f34da-112">ESE-Dateien</span><span class="sxs-lookup"><span data-stu-id="f34da-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="f34da-113">Die Programm Quelldateien sollten die Header Datei "ESENT. h" enthalten, um auf Funktionsprototypen und Strukturdefinitionen für die erweiterbare Speicher-Engine-API zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f34da-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="f34da-114">Entwickler können die Bibliothek Datei ESENT. lib verwenden, um Anwendungen zu erstellen, die die erweiterbare Speicher-Engine-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="f34da-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="f34da-115">Zur Laufzeit verknüpfen Anwendungen mit dem esent.dll.</span><span class="sxs-lookup"><span data-stu-id="f34da-115">At runtime, applications link to the esent.dll.</span></span>
