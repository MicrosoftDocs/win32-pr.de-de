---
description: Im Abschnitt Installieren einer INF-Datei werden die Schritte der Installationsprozedur definiert.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Beispiel für INF-Installations Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353619"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="0c9d0-103">Beispiel für INF-Installations Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0c9d0-103">INF Install Section Example</span></span>

<span data-ttu-id="0c9d0-104">Im Abschnitt **Installieren** einer INF-Datei werden die Schritte der Installationsprozedur definiert.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="0c9d0-105">Jede Zeile eines **Installations** Abschnitts besteht aus zwei Teilen.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="0c9d0-106">Auf der linken Seite des Gleichheitszeichens (=) ist der Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="0c9d0-107">Auf der rechten Seite ist eine Liste mit mindestens einem Abschnitts Titel.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="0c9d0-108">Der Schlüssel gibt den Typ der Abschnitte an, die auf der rechten Seite aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="0c9d0-109">Eine Beschreibung des Formats dieses Abschnitts finden Sie in den Abschnitten und Direktiven der INF-Datei des Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="0c9d0-110">Im folgenden finden Sie ein Beispiel für einen **Installations** Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="0c9d0-111">In diesem Beispiel wird der **CopyFiles** -Schlüssel auf die Werte "DATAFILES" und "Program Files" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="0c9d0-112">Dies gibt zwei Abschnitte zum **Kopieren von Dateien** in der INF-Datei an, die die Namen der Quelldateien enthalten, die bei Kopier Vorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="0c9d0-113">Das Ziel für die kopierten Dateien wird in einem **DestinationDirs** -Abschnitt in der INF-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="0c9d0-114">Der " **Delta files** "-Schlüssel erhält den Wert "oldfiles".</span><span class="sxs-lookup"><span data-stu-id="0c9d0-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="0c9d0-115">Dies gibt den Abschnitt **Dateien löschen** an, der Informationen enthält, die für Datei Löschvorgänge relevant sind.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="0c9d0-116">Der Schlüssel **UpdateInis** gibt die **Update-INI-Datei** Abschnitte an, die Informationen zum Aktualisieren von Einträgen in der INI-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c9d0-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="0c9d0-117">Die Schlüssel " **adressg** " und " **DelReg** " geben Abschnitte " **Registrierung hinzufügen** " und " **Löschen** " an, die Informationen zum Hinzufügen oder Löschen von Registrierungs</span><span class="sxs-lookup"><span data-stu-id="0c9d0-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



