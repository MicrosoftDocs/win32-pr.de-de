---
description: Während einer Windows Installer Installation kann das Installationsprogramm nach einer Datei an einem bestimmten Speicherort im System des Benutzers suchen.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Suchen nach einer Datei an einem bestimmten Speicherort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529498"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="db32e-103">Suchen nach einer Datei an einem bestimmten Speicherort</span><span class="sxs-lookup"><span data-stu-id="db32e-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="db32e-104">**So suchen Sie nach einer Datei an einem bestimmten Speicherort auf einem Benutzersystem**</span><span class="sxs-lookup"><span data-stu-id="db32e-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="db32e-105">Listen Sie die Datei Signatur und den Namen in der [Signatur Tabelle](signature-table.md)auf.</span><span class="sxs-lookup"><span data-stu-id="db32e-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="db32e-106">Die verbleibenden Felder in diesem Datensatz können NULL sein, um nach einer beliebigen Version von MyApp.exe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="db32e-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="db32e-107">Signatur Tabelle</span><span class="sxs-lookup"><span data-stu-id="db32e-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="db32e-108">Signatur</span><span class="sxs-lookup"><span data-stu-id="db32e-108">Signature</span></span>          | <span data-ttu-id="db32e-109">Dateiname</span><span class="sxs-lookup"><span data-stu-id="db32e-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="db32e-110">Appfile</span><span class="sxs-lookup"><span data-stu-id="db32e-110">AppFile</span></span><br/> | <span data-ttu-id="db32e-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="db32e-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="db32e-112">Geben Sie die Eigenschaft ein, die vom Installationsprogramm festgelegt werden soll, wenn MyApp.exe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="db32e-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="db32e-113">[AppSearch-Tabelle](appsearch-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="db32e-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="db32e-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="db32e-114">Property</span></span>         | <span data-ttu-id="db32e-115">Signatur</span><span class="sxs-lookup"><span data-stu-id="db32e-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="db32e-116">MyApp</span><span class="sxs-lookup"><span data-stu-id="db32e-116">MYAPP</span></span><br/> | <span data-ttu-id="db32e-117">Appfile</span><span class="sxs-lookup"><span data-stu-id="db32e-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="db32e-118">Verwenden Sie die [drlocator-Tabelle](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="db32e-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="db32e-119">Geben Sie im Feld Pfad den vollständigen Pfad zur Datei auf dem Benutzersystem ein.</span><span class="sxs-lookup"><span data-stu-id="db32e-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="db32e-120">Geben Sie in der Spalte Tiefe den Wert 0 ein, um den Ordner bin zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="db32e-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="db32e-121">Drlocator-Tabelle</span><span class="sxs-lookup"><span data-stu-id="db32e-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="db32e-122">Signatur</span><span class="sxs-lookup"><span data-stu-id="db32e-122">Signature</span></span>          | <span data-ttu-id="db32e-123">Parent</span><span class="sxs-lookup"><span data-stu-id="db32e-123">Parent</span></span> | <span data-ttu-id="db32e-124">Pfad</span><span class="sxs-lookup"><span data-stu-id="db32e-124">Path</span></span>                                                    | <span data-ttu-id="db32e-125">Tiefe</span><span class="sxs-lookup"><span data-stu-id="db32e-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="db32e-126">Appfile</span><span class="sxs-lookup"><span data-stu-id="db32e-126">AppFile</span></span><br/> |        | <span data-ttu-id="db32e-127">C: \\ Programmdateien \\ myProducts- \\ Projekte \\ bin</span><span class="sxs-lookup"><span data-stu-id="db32e-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="db32e-128">0</span><span class="sxs-lookup"><span data-stu-id="db32e-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="db32e-129">Fügen Sie die Aktion AppSearch in die Aktions Sequenz ein.</span><span class="sxs-lookup"><span data-stu-id="db32e-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="db32e-130">Wenn MyApp.exe im Ordner "C: \\ Programme \\ myProducts Projects" installiert ist \\ \\ , legt das Installationsprogramm die Eigenschaft "MyApp" auf den Speicherort der Datei fest.</span><span class="sxs-lookup"><span data-stu-id="db32e-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




