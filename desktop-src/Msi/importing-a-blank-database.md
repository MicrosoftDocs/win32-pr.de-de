---
description: Um das Beispiel zu reproduzieren, das Sie kopieren oder mit einem Software Tool erstellen müssen, eine Windows Installer Datenbankdatei.
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: Importieren einer leeren Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216938"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="79e98-103">Importieren einer leeren Datenbank</span><span class="sxs-lookup"><span data-stu-id="79e98-103">Importing a Blank Database</span></span>

<span data-ttu-id="79e98-104">Um das Beispiel zu reproduzieren, das Sie kopieren oder mit einem Software Tool erstellen müssen, eine Windows Installer Datenbankdatei.</span><span class="sxs-lookup"><span data-stu-id="79e98-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="79e98-105">Eine vollständig leere Installations Datenbank, Schema.msi, wird mit den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="79e98-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="79e98-106">Das SDK stellt außerdem eine teilweise leere Datenbank (uisample.msi) bereit, die die vorgeschlagenen Sequenz Tabellen und Daten enthält, die für eine einfache Benutzeroberfläche erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="79e98-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="79e98-107">Erstellen Sie eine Kopie von uisample.msi, und verschieben Sie Sie in das Verzeichnis, in dem sich der Ordner befindet, den Sie unter [Planen der Installation](planning-the-installation.md)erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="79e98-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="79e98-108">Benennen Sie die Datei MNP2000.msi um.</span><span class="sxs-lookup"><span data-stu-id="79e98-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="79e98-109">Die Installationsdaten Bank Datei und die Quelldateien müssen sich im Stammverzeichnis desselben Verzeichnisses befinden.</span><span class="sxs-lookup"><span data-stu-id="79e98-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="79e98-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="79e98-110">For example:</span></span>

<span data-ttu-id="79e98-111">C: \\ Beispiel \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="79e98-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="79e98-112">C: \\ Beispiel für \\ Notepad</span><span class="sxs-lookup"><span data-stu-id="79e98-112">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="79e98-113">Wenn Sie Uisample.msi nicht verwenden, müssen Sie eine leere Datenbank (z. b. Schema.msi) abrufen und Informationen für die Installation mithilfe eines Tools zur Datenbankbearbeitung, wie z. b. Orca, das mit dem SDK bereitgestellt wird, oder eines anderen Daten Bank Editors eingeben.</span><span class="sxs-lookup"><span data-stu-id="79e98-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="79e98-114">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="79e98-114">Continue</span></span>](specifying-directory-structure.md)

 

 



