---
description: Der Installer speichert Informationen zur Installationsverzeichnis Struktur in der Verzeichnis Tabelle.
ms.assetid: 31390138-b1d0-4f0b-9304-6e7c69e6a736
title: Angeben der Verzeichnisstruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a87880921799158559e28fed2c6dde97c9a331
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862908"
---
# <a name="specifying-directory-structure"></a><span data-ttu-id="2c132-103">Angeben der Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="2c132-103">Specifying Directory Structure</span></span>

<span data-ttu-id="2c132-104">Der Installer speichert Informationen zur Installationsverzeichnis Struktur in der [Verzeichnis Tabelle](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c132-104">The installer keeps information about the installation directory structure in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="2c132-105">Weitere Informationen finden Sie in der [Gruppe der Kern Tabellen](core-tables-group.md)</span><span class="sxs-lookup"><span data-stu-id="2c132-105">See the [Core Tables Group](core-tables-group.md).</span></span> <span data-ttu-id="2c132-106">In diesem Abschnitt fügen Sie der leeren Datenbank, die Sie unter [Importieren einer leeren Datenbank](importing-a-blank-database.md)erstellt haben, Verzeichnisstruktur Informationen für das Notepad-Beispiel hinzu.</span><span class="sxs-lookup"><span data-stu-id="2c132-106">In this section you add directory structure information for the Notepad sample to the empty database you created in [Importing a Blank Database](importing-a-blank-database.md).</span></span> <span data-ttu-id="2c132-107">Verwenden Sie den Datenbank-Editor, der mit dem SDK bereitgestellt wird, oder einen anderen Editor, um die Verzeichnis Tabelle in MNP2000.msi zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2c132-107">Use the database editor Orca that is provided with the SDK, or another editor, to open the Directory Table in MNP2000.msi.</span></span> <span data-ttu-id="2c132-108">Verwenden Sie den Editor, um die folgenden Daten in die leere Verzeichnis Tabelle einzugeben.</span><span class="sxs-lookup"><span data-stu-id="2c132-108">Use the editor to enter the following data into the blank Directory table.</span></span>

[<span data-ttu-id="2c132-109">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="2c132-109">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="2c132-110">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="2c132-110">Directory</span></span>                                        | <span data-ttu-id="2c132-111">Über \_ geordnetes Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="2c132-111">Directory\_Parent</span></span>                                | <span data-ttu-id="2c132-112">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="2c132-112">DefaultDir</span></span>        |
|--------------------------------------------------|--------------------------------------------------|-------------------|
| [<span data-ttu-id="2c132-113">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="2c132-113">**TARGETDIR**</span></span>](targetdir.md)                   |                                                  | <span data-ttu-id="2c132-114">SourceDir</span><span class="sxs-lookup"><span data-stu-id="2c132-114">SourceDir</span></span>         |
| [<span data-ttu-id="2c132-115">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="2c132-115">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | [<span data-ttu-id="2c132-116">**TARGETDIR**</span><span class="sxs-lookup"><span data-stu-id="2c132-116">**TARGETDIR**</span></span>](targetdir.md)                   | <span data-ttu-id="2c132-117">.</span><span class="sxs-lookup"><span data-stu-id="2c132-117">.</span></span>                 |
| <span data-ttu-id="2c132-118">Argsdir</span><span class="sxs-lookup"><span data-stu-id="2c132-118">ARTSDIR</span></span>                                          | <span data-ttu-id="2c132-119">Notepaddir</span><span class="sxs-lookup"><span data-stu-id="2c132-119">NOTEPADDIR</span></span>                                       | <span data-ttu-id="2c132-120">Kunst: Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2c132-120">Arts:Events</span></span>       |
| <span data-ttu-id="2c132-121">Holdir</span><span class="sxs-lookup"><span data-stu-id="2c132-121">HOLDIR</span></span>                                           | <span data-ttu-id="2c132-122">Mondir</span><span class="sxs-lookup"><span data-stu-id="2c132-122">MONDIR</span></span>                                           | <span data-ttu-id="2c132-123">.: Feiertage</span><span class="sxs-lookup"><span data-stu-id="2c132-123">.:Holidays</span></span>        |
| <span data-ttu-id="2c132-124">Menudir</span><span class="sxs-lookup"><span data-stu-id="2c132-124">MENUDIR</span></span>                                          | <span data-ttu-id="2c132-125">Notepaddir</span><span class="sxs-lookup"><span data-stu-id="2c132-125">NOTEPADDIR</span></span>                                       | <span data-ttu-id="2c132-126">Menü</span><span class="sxs-lookup"><span data-stu-id="2c132-126">Menu</span></span>              |
| <span data-ttu-id="2c132-127">Mondir</span><span class="sxs-lookup"><span data-stu-id="2c132-127">MONDIR</span></span>                                           | <span data-ttu-id="2c132-128">Notepaddir</span><span class="sxs-lookup"><span data-stu-id="2c132-128">NOTEPADDIR</span></span>                                       | <span data-ttu-id="2c132-129">Tors</span><span class="sxs-lookup"><span data-stu-id="2c132-129">Gate</span></span>              |
| <span data-ttu-id="2c132-130">Notepaddir</span><span class="sxs-lookup"><span data-stu-id="2c132-130">NOTEPADDIR</span></span>                                       | [<span data-ttu-id="2c132-131">**ProgramFilesFolder**</span><span class="sxs-lookup"><span data-stu-id="2c132-131">**ProgramFilesFolder**</span></span>](programfilesfolder.md) | <span data-ttu-id="2c132-132">Roter \_ Park: Notepad</span><span class="sxs-lookup"><span data-stu-id="2c132-132">Red\_Park:Notepad</span></span> |
| <span data-ttu-id="2c132-133">Sportdir</span><span class="sxs-lookup"><span data-stu-id="2c132-133">SPORTDIR</span></span>                                         | <span data-ttu-id="2c132-134">Notepaddir</span><span class="sxs-lookup"><span data-stu-id="2c132-134">NOTEPADDIR</span></span>                                       | <span data-ttu-id="2c132-135">Sport: Ereignisse</span><span class="sxs-lookup"><span data-stu-id="2c132-135">Sports:Events</span></span>     |



 

<span data-ttu-id="2c132-136">Wenn Sie diese Daten in die Verzeichnis Tabelle eingeben, werden die Quell-und Zielverzeichnis Strukturen angegeben.</span><span class="sxs-lookup"><span data-stu-id="2c132-136">Entering this data into the Directory table specifies the source and target directory structures.</span></span> <span data-ttu-id="2c132-137">Informationen finden Sie in der [Verzeichnis Tabelle](directory-table.md) und in den Themen zu [den Verzeichnis Tabellen](using-the-directory-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2c132-137">See the [Directory Table](directory-table.md) and [Using the Directory Table](using-the-directory-table.md) topics.</span></span> <span data-ttu-id="2c132-138">Beachten Sie, dass es sich bei der [**TARGETDIR**](targetdir.md) -Eigenschaft um den Namen eines Stamms in der Verzeichnis Tabelle jeder Installation handeln muss.</span><span class="sxs-lookup"><span data-stu-id="2c132-138">Note that the [**TARGETDIR**](targetdir.md) property must be the name of one root in the Directory table of every installation.</span></span>

[<span data-ttu-id="2c132-139">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="2c132-139">Continue</span></span>](specifying-components.md)

 

 



