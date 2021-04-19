---
description: Während einer Windows Installer Installation kann das Installationsprogramm alle Festplattenlaufwerke nach einer Datei durchsuchen.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Suchen aller Festplattenlaufwerke nach einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350291"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="995ad-103">Suchen aller Festplattenlaufwerke nach einer Datei</span><span class="sxs-lookup"><span data-stu-id="995ad-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="995ad-104">**So durchsuchen Sie alle Festplattenlaufwerke nach einer Datei**</span><span class="sxs-lookup"><span data-stu-id="995ad-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="995ad-105">Geben Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)ein.</span><span class="sxs-lookup"><span data-stu-id="995ad-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="995ad-106">Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="995ad-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="995ad-107">[Signatur Tabelle](signature-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="995ad-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="995ad-108">Signatur</span><span class="sxs-lookup"><span data-stu-id="995ad-108">Signature</span></span>          | <span data-ttu-id="995ad-109">Dateiname</span><span class="sxs-lookup"><span data-stu-id="995ad-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="995ad-110">Appfile</span><span class="sxs-lookup"><span data-stu-id="995ad-110">AppFile</span></span><br/> | <span data-ttu-id="995ad-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="995ad-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="995ad-112">Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="995ad-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="995ad-113">AppSearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="995ad-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="995ad-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="995ad-114">Property</span></span>         | <span data-ttu-id="995ad-115">Signatur</span><span class="sxs-lookup"><span data-stu-id="995ad-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="995ad-116">MyApp</span><span class="sxs-lookup"><span data-stu-id="995ad-116">MYAPP</span></span><br/> | <span data-ttu-id="995ad-117">Appfile</span><span class="sxs-lookup"><span data-stu-id="995ad-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="995ad-118">Verwenden Sie die [drlocator-Tabelle](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="995ad-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="995ad-119">Lassen Sie die Felder für übergeordnetes und Pfad leer, um alle Festplattenlaufwerke des Benutzer Systems zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="995ad-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="995ad-120">Geben Sie in der Spalte Tiefe die Anzahl der zu durchsuchenden Unterverzeichnis Ebenen an.</span><span class="sxs-lookup"><span data-stu-id="995ad-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="995ad-121">Wenn Sie z. b. Tiefe auf 0 festlegen, wird c: \\MyApp.exe erkannt, aber die Datei wird nicht mit einer Tiefe von 2 erkannt, z. b.: c: \\ Program Files \\ myApps \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="995ad-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="995ad-122">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="995ad-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="995ad-123">Signatur</span><span class="sxs-lookup"><span data-stu-id="995ad-123">Signature</span></span>          | <span data-ttu-id="995ad-124">Parent</span><span class="sxs-lookup"><span data-stu-id="995ad-124">Parent</span></span> | <span data-ttu-id="995ad-125">Pfad</span><span class="sxs-lookup"><span data-stu-id="995ad-125">Path</span></span> | <span data-ttu-id="995ad-126">Tiefe</span><span class="sxs-lookup"><span data-stu-id="995ad-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="995ad-127">Appfile</span><span class="sxs-lookup"><span data-stu-id="995ad-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="995ad-128">3</span><span class="sxs-lookup"><span data-stu-id="995ad-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="995ad-129">Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein.</span><span class="sxs-lookup"><span data-stu-id="995ad-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="995ad-130">Wenn MyApp.exe installiert ist, legt das Installationsprogramm die Eigenschaft "MyApp" auf den Speicherort der Datei fest.</span><span class="sxs-lookup"><span data-stu-id="995ad-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="995ad-131">Wenn die Datei installiert ist, wertet MyApp den Wert true in einem bedingten Ausdruck aus.</span><span class="sxs-lookup"><span data-stu-id="995ad-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




