---
description: Beginnen Sie, das Upgradepaket zu erstellen, indem Sie das Installationspaket und die Quellverzeichnis Struktur des ursprünglichen Produkts kopieren.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importieren der ursprünglichen Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373160"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="48e36-103">Importieren der ursprünglichen Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="48e36-103">Importing Original Installation Database</span></span>

<span data-ttu-id="48e36-104">Beginnen Sie, das Upgradepaket zu erstellen, indem Sie das Installationspaket und die Quellverzeichnis Struktur des ursprünglichen Produkts kopieren.</span><span class="sxs-lookup"><span data-stu-id="48e36-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="48e36-105">Anweisungen zum Erstellen des Installationspakets für MNP2000 sind in [einem Installations Beispiel](an-installation-example.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="48e36-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="48e36-106">Kopieren Sie die Inhalte der folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="48e36-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="48e36-107">C: \\ Beispiel \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="48e36-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="48e36-108">C: \\ Beispiel für \\ Notepad</span><span class="sxs-lookup"><span data-stu-id="48e36-108">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="48e36-109">C: \\ Beispiel \\ Binär</span><span class="sxs-lookup"><span data-stu-id="48e36-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="48e36-110">C: \\ Beispiel \\ Symbol</span><span class="sxs-lookup"><span data-stu-id="48e36-110">C:\\Sample\\Icon</span></span>\\

<span data-ttu-id="48e36-111">Aktualisieren Sie den Inhalt des Ordners Notepad, damit Sie mit der unter [Planen eines größeren Upgrades](planning-a-major-upgrade.md)beschriebenen Quelle identisch sind.</span><span class="sxs-lookup"><span data-stu-id="48e36-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="48e36-112">Entfernen Sie alle veralteten Quelldateien, z. b. Baseball.txt, und ersetzen Sie durch die aktualisierten Dateien, z. b. Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="48e36-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="48e36-113">Fügen Sie die zusätzlichen neuen, vom Upgrade bereitgestellten Dateien hinzu, z. b. Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="48e36-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="48e36-114">Benennen Sie MNP2000.msi in MNP2001.msi um.</span><span class="sxs-lookup"><span data-stu-id="48e36-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="48e36-115">In den nachfolgenden Schritten verwenden Sie einen Tabellen-Editor, um diese Datenbank für das Upgrade in die MSI-Datei zu ändern.</span><span class="sxs-lookup"><span data-stu-id="48e36-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="48e36-116">Datenbanktabellen, die nicht explizit in den nachfolgenden Abschnitten geändert werden, sind identisch mit den Tabellen in der Datenbank des ursprünglichen Produkts, MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="48e36-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="48e36-117">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="48e36-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



