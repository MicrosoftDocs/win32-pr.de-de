---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einer Datei suchen und eine Eigenschaft mit dem Pfad der Datei erstellen.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866064"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="d39f6-103">Suchen nach einer Datei und Erstellen einer Eigenschaft mit dem Pfad der Datei</span><span class="sxs-lookup"><span data-stu-id="d39f6-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="d39f6-104">**So suchen Sie nach einer Datei und erstellen eine Eigenschaft, die den Pfad der Datei enthält**</span><span class="sxs-lookup"><span data-stu-id="d39f6-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="d39f6-105">Suchen Sie zuerst nach der Datei, indem Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)auflisten.</span><span class="sxs-lookup"><span data-stu-id="d39f6-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="d39f6-106">Die restlichen Felder dieses Datensatzes können leer gelassen werden, um eine Suche nach einer beliebigen Version von MyApp.exe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d39f6-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="d39f6-107">[Signatur Tabelle](signature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d39f6-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="d39f6-108">Signatur</span><span class="sxs-lookup"><span data-stu-id="d39f6-108">Signature</span></span>          | <span data-ttu-id="d39f6-109">Dateiname</span><span class="sxs-lookup"><span data-stu-id="d39f6-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="d39f6-110">Appfile</span><span class="sxs-lookup"><span data-stu-id="d39f6-110">AppFile</span></span><br/> | <span data-ttu-id="d39f6-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="d39f6-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="d39f6-112">Geben Sie als nächstes den Pfad der Datei an, nach der in der [drlocator-Tabelle](drlocator-table.md)gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="d39f6-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="d39f6-113">Da appfolder nicht in der [Signatur Tabelle](signature-table.md)aufgeführt ist, stellt das Installationsprogramm fest, dass appfolder ein Ordner und keine Datei ist.</span><span class="sxs-lookup"><span data-stu-id="d39f6-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="d39f6-114">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d39f6-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="d39f6-115">Signatur</span><span class="sxs-lookup"><span data-stu-id="d39f6-115">Signature</span></span>            | <span data-ttu-id="d39f6-116">Parent</span><span class="sxs-lookup"><span data-stu-id="d39f6-116">Parent</span></span>             | <span data-ttu-id="d39f6-117">Pfad</span><span class="sxs-lookup"><span data-stu-id="d39f6-117">Path</span></span> | <span data-ttu-id="d39f6-118">Tiefe</span><span class="sxs-lookup"><span data-stu-id="d39f6-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="d39f6-119">Appfile</span><span class="sxs-lookup"><span data-stu-id="d39f6-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="d39f6-120">Appfolder</span><span class="sxs-lookup"><span data-stu-id="d39f6-120">AppFolder</span></span><br/> | <span data-ttu-id="d39f6-121">Appfile</span><span class="sxs-lookup"><span data-stu-id="d39f6-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="d39f6-122">Füllen Sie schließlich die [AppSearch-Tabelle](appsearch-table.md) auf, damit die [AppSearch-Aktion](appsearch-action.md) den Pfad von appfolder zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d39f6-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="d39f6-123">Nachdem das Installationsprogramm die AppSearch-Aktion ausgeführt hat, ist der Wert von "MyFolder" der vollständige Pfad von "appfolder".</span><span class="sxs-lookup"><span data-stu-id="d39f6-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="d39f6-124">[AppSearch-Tabelle](appsearch-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d39f6-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="d39f6-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d39f6-125">Property</span></span>            | <span data-ttu-id="d39f6-126">Signatur</span><span class="sxs-lookup"><span data-stu-id="d39f6-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="d39f6-127">MYFOLDER</span><span class="sxs-lookup"><span data-stu-id="d39f6-127">MYFOLDER</span></span><br/> | <span data-ttu-id="d39f6-128">Appfolder</span><span class="sxs-lookup"><span data-stu-id="d39f6-128">AppFolder</span></span><br/> |

    

     

 

 




