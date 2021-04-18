---
description: Eine CAB-Datei ist eine einzelne Datei, in der Regel mit der Erweiterung ". cab", die komprimierte Dateien in einer Datei Bibliothek speichert.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: CAB-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343850"
---
# <a name="cabinet-files"></a><span data-ttu-id="305d8-103">CAB-Dateien</span><span class="sxs-lookup"><span data-stu-id="305d8-103">Cabinet Files</span></span>

<span data-ttu-id="305d8-104">Eine CAB-Datei ist eine einzelne Datei, in der Regel mit der Erweiterung ". cab", die komprimierte Dateien in einer Datei Bibliothek speichert.</span><span class="sxs-lookup"><span data-stu-id="305d8-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="305d8-105">Das CAB-Format stellt eine effiziente Möglichkeit zum Packen mehrerer Dateien dar, da die Komprimierung über Dateigrenzen hinweg durchgeführt wird, was das Komprimierungs Verhältnis erheblich verbessert.</span><span class="sxs-lookup"><span data-stu-id="305d8-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="305d8-106">Entwickler können mithilfe eines Tools zum Erstellen von CAB-Dateien wie Makecab.exe CAB-Dateien für die Verwendung mit Installer-Paketen verwenden.</span><span class="sxs-lookup"><span data-stu-id="305d8-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="305d8-107">Das Makecab.exe-Hilfsprogramm ist in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="305d8-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="305d8-108">Entwickler können auch ein Tool zum Erstellen von CAB-Dateien wie Cabarc.exe verwenden, um CAB-Dateien für die Verwendung mit Installer-Paketen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="305d8-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="305d8-109">Dieses Tool schreibt in die Diamant-CAB-Struktur.</span><span class="sxs-lookup"><span data-stu-id="305d8-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="305d8-110">Die Datei Schlüssel der Dateien, die in einer CAB-Datei gespeichert sind, müssen mit den Einträgen in der File-Spalte der [Dateitabelle](file-table.md) identisch sein, und die Sequenz der Dateien in der CAB-Datei muss mit der in der Sequence-Spalte angegebenen Datei Sequenz identisch sein.</span><span class="sxs-lookup"><span data-stu-id="305d8-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="305d8-111">Weitere Informationen finden Sie unter [Verwenden von Schränken und komprimierten Quellen](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="305d8-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="305d8-112">Große Dateien können zwischen zwei oder mehr CAB-Dateien aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="305d8-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="305d8-113">In einer CAB-Datei, die sich auf die nächste CAB-Datei erstreckt, dürfen nicht mehr als 15 Dateien vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="305d8-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="305d8-114">Wenn Sie z. b. drei CAB-Dateien haben, kann die erste CAB-Datei 15 Dateien enthalten, die sich in der zweiten CAB-Datei befinden, und die zweite CAB-Datei kann 15 Dateien enthalten, die für die dritte CAB-Datei spannen.</span><span class="sxs-lookup"><span data-stu-id="305d8-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="305d8-115">Das Installationsprogramm extrahiert Dateien aus einer CAB-Datei, da Sie von der Installation benötigt werden, und installiert Sie in derselben Reihenfolge, in der Sie in der CAB-Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="305d8-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="305d8-116">Die Speicherplatzanforderungen für die Installation einer Datei, die in einer CAB-Datei gespeichert ist, unterscheiden sich nicht von der Installation unkomprimierter Dateien</span><span class="sxs-lookup"><span data-stu-id="305d8-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="305d8-117">Eine CAB-Datei kann sich innerhalb oder außerhalb der MSI-Datei befinden.</span><span class="sxs-lookup"><span data-stu-id="305d8-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="305d8-118">Ab Windows Installer 5,0, die unter Windows 7 oder Windows Server 2008 R2 ausgeführt wird, speichert das Installationsprogramm alle Schränke, die in die MSI-Datei eingebettet sind, bevor das Installationspaket zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="305d8-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="305d8-119">**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Um Speicherplatz zu sparen, entfernt das Installationsprogramm immer alle Schränke, die in die MSI-Datei eingebettet sind, bevor das Installationspaket auf dem Computer des Benutzers zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="305d8-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



