---
description: Befolgen Sie diese Richtlinien, um die Lokalisierung von Windows Installer Paketen zu vereinfachen.
ms.assetid: f00b44b4-e8ec-46d2-b329-00728a83275b
title: Vorbereiten eines Windows Installer Pakets für die Lokalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa46af5259b880398aa84dc817eb201bd63456eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344242"
---
# <a name="preparing-a-windows-installer-package-for-localization"></a><span data-ttu-id="359f6-103">Vorbereiten eines Windows Installer Pakets für die Lokalisierung</span><span class="sxs-lookup"><span data-stu-id="359f6-103">Preparing a Windows Installer Package for Localization</span></span>

<span data-ttu-id="359f6-104">Die Lokalisierung eines Windows Installer Pakets in mehrere Sprachen kann durch folgende Aktionen deutlich vereinfacht werden:</span><span class="sxs-lookup"><span data-stu-id="359f6-104">Localization of a Windows Installer package into multiple languages can be greatly facilitated by doing the following:</span></span>

-   <span data-ttu-id="359f6-105">Erstellen Sie eine Basis-Installations Datenbank, die Code Page neutral ist.</span><span class="sxs-lookup"><span data-stu-id="359f6-105">Author a base installation database that is code page neutral.</span></span> <span data-ttu-id="359f6-106">Weitere Informationen finden Sie [unter Erstellen einer Datenbank mit einer neutralen Codepage](creating-a-database-with-a-neutral-code-page.md).</span><span class="sxs-lookup"><span data-stu-id="359f6-106">See [Creating a database with a neutral code page](creating-a-database-with-a-neutral-code-page.md).</span></span> <span data-ttu-id="359f6-107">Die Codepage der lokalisierten Datenbank kann dann festgelegt werden, indem eine Textarchiv Tabelle mit einer nicht neutralen Codepage in die Basisdatenbank importiert wird.</span><span class="sxs-lookup"><span data-stu-id="359f6-107">The code page of the localized database can then be set by importing a text archive table with a non-neutral code page into the base database.</span></span> <span data-ttu-id="359f6-108">Siehe [Festlegen der Codepage einer Datenbank](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="359f6-108">See [Setting the code page of a database](setting-the-code-page-of-a-database.md).</span></span>
-   <span data-ttu-id="359f6-109">Organisieren Sie Dateien, die eine Lokalisierung in separate Komponenten erfordern, und installieren Sie diese Dateien in separaten Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="359f6-109">Organize files requiring localization into separate components and install these files into separate directories.</span></span> <span data-ttu-id="359f6-110">Dadurch wird sichergestellt, dass zwei lokalisierte Pakete niemals Dateien mit identischem Namen im selben Verzeichnis installieren.</span><span class="sxs-lookup"><span data-stu-id="359f6-110">This ensures that two localized packages never install identically named files into the same directory.</span></span>

<span data-ttu-id="359f6-111">Beispielsweise kann eine weltweite Anwendung, die die folgenden Ressourcen verwendet, drei Komponenten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="359f6-111">For example, a worldwide application using the following resources may have three components.</span></span>



| <span data-ttu-id="359f6-112">Komponente</span><span class="sxs-lookup"><span data-stu-id="359f6-112">Component</span></span> | <span data-ttu-id="359f6-113">Resource</span><span class="sxs-lookup"><span data-stu-id="359f6-113">Resource</span></span>                   |
|-----------|----------------------------|
| <span data-ttu-id="359f6-114">World</span><span class="sxs-lookup"><span data-stu-id="359f6-114">WORLD</span></span>     | <span data-ttu-id="359f6-115">worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="359f6-115">worldwide.exe</span></span>              |
| <span data-ttu-id="359f6-116">World</span><span class="sxs-lookup"><span data-stu-id="359f6-116">WORLD</span></span>     | <span data-ttu-id="359f6-117">weltweite Registrierungseinträge</span><span class="sxs-lookup"><span data-stu-id="359f6-117">worldwide registry entries</span></span> |
| <span data-ttu-id="359f6-118">World</span><span class="sxs-lookup"><span data-stu-id="359f6-118">WORLD</span></span>     | <span data-ttu-id="359f6-119">weltweite Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="359f6-119">worldwide shortcut</span></span>         |
| <span data-ttu-id="359f6-120">DE</span><span class="sxs-lookup"><span data-stu-id="359f6-120">ENG</span></span>       | <span data-ttu-id="359f6-121">engui.dll</span><span class="sxs-lookup"><span data-stu-id="359f6-121">engui.dll</span></span>                  |
| <span data-ttu-id="359f6-122">DE</span><span class="sxs-lookup"><span data-stu-id="359f6-122">ENG</span></span>       | <span data-ttu-id="359f6-123">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="359f6-123">readme.txt</span></span>                 |
| <span data-ttu-id="359f6-124">FRA</span><span class="sxs-lookup"><span data-stu-id="359f6-124">FRA</span></span>       | <span data-ttu-id="359f6-125">fraui.dll</span><span class="sxs-lookup"><span data-stu-id="359f6-125">fraui.dll</span></span>                  |
| <span data-ttu-id="359f6-126">FRA</span><span class="sxs-lookup"><span data-stu-id="359f6-126">FRA</span></span>       | <span data-ttu-id="359f6-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="359f6-127">readme.txt</span></span>                 |



 

<span data-ttu-id="359f6-128">Die Dateien, die lokalisiert werden müssen, können in den folgenden Verzeichnis Speicherorten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="359f6-128">The files that need to be localized may be installed into the following directory locations:</span></span>

-   <span data-ttu-id="359f6-129">\[ProgramFilesFolder \] \\ World \\worldwide.exe</span><span class="sxs-lookup"><span data-stu-id="359f6-129">\[ProgramFilesFolder\]\\World\\worldwide.exe</span></span>
-   <span data-ttu-id="359f6-130">\[ProgramFilesFolder \] \\ World \\ English \\engui.dll</span><span class="sxs-lookup"><span data-stu-id="359f6-130">\[ProgramFilesFolder\]\\World\\English\\engui.dll</span></span>
-   <span data-ttu-id="359f6-131">\[ProgramFilesFolder \] \\ World \\ English \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="359f6-131">\[ProgramFilesFolder\]\\World\\English\\readme.txt</span></span>
-   <span data-ttu-id="359f6-132">\[ProgramFilesFolder \] \\ World \\ French \\fraui.dll</span><span class="sxs-lookup"><span data-stu-id="359f6-132">\[ProgramFilesFolder\]\\World\\French\\fraui.dll</span></span>
-   <span data-ttu-id="359f6-133">\[ProgramFilesFolder \] \\ World \\ French \\readme.txt</span><span class="sxs-lookup"><span data-stu-id="359f6-133">\[ProgramFilesFolder\]\\World\\French\\readme.txt</span></span>

 

 



