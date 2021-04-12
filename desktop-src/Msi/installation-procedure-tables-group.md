---
description: Die Tabellen in der Installationsprozedur Gruppe steuern Tasks, die während der Installation durch Standard Aktionen und benutzerdefinierte Aktionen ausgeführt werden.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppe "Installationsprozedur Tabellen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349758"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="cd03b-103">Gruppe "Installationsprozedur Tabellen"</span><span class="sxs-lookup"><span data-stu-id="cd03b-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="cd03b-104">Die Tabellen in der Installationsprozedur Gruppe steuern Tasks, die während der Installation durch [Standard Aktionen](standard-actions.md) und [benutzerdefinierte Aktionen](custom-actions.md)ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cd03b-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="cd03b-105">Einige der Tabellen in dieser Gruppe steuern eine auf hoher Ebene durch Bereitstellung einer Aktions Sequenz.</span><span class="sxs-lookup"><span data-stu-id="cd03b-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="cd03b-106">Jede der folgenden Sequenz Tabellen steuert einen Teil einer Aktion auf hoher Ebene.</span><span class="sxs-lookup"><span data-stu-id="cd03b-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="cd03b-107">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="cd03b-108">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="cd03b-109">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="cd03b-110">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="cd03b-111">Advtuisequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="cd03b-112">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd03b-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="cd03b-113">Es kann Situationen geben, in denen eine Installation etwas durchführen muss, das nur [Standard Aktionen](standard-actions.md)verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd03b-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="cd03b-114">Um das höchste Maß an Flexibilität zu bieten, bietet das Installationsprogramm Setup Autoren die Möglichkeit, eigene benutzerdefinierte Aktionen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd03b-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="cd03b-115">Wenn Sie über benutzerdefinierte Aktionen verfügen, sollten Sie diese beim Installer registrieren, indem Sie die Tabelle CustomAction auffüllen.</span><span class="sxs-lookup"><span data-stu-id="cd03b-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="cd03b-116">Die [Tabelle CustomAction](customaction-table.md) bietet die Möglichkeit, benutzerdefinierten Code und Daten in den Installationsprozess zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="cd03b-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="cd03b-117">Der Code, der ausgeführt wird, kann ein in der Datenbank enthaltener Stream, eine zuletzt installierte Datei oder eine vorhandene ausführbare Datei sein.</span><span class="sxs-lookup"><span data-stu-id="cd03b-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="cd03b-118">In den folgenden Tabellen werden die Funktionen des Installers zum Bearbeiten von Dateien und Ordnern während der Installation erweitert.</span><span class="sxs-lookup"><span data-stu-id="cd03b-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="cd03b-119">Die [Tabelle RemoveFile](removefile-table.md) enthält eine Liste von Dateien, die während der Installation entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cd03b-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="cd03b-120">Die [removeinifile-Tabelle](removeinifile-table.md) enthält die Informationen, die eine Anwendung aus INI-Dateien entfernen muss.</span><span class="sxs-lookup"><span data-stu-id="cd03b-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="cd03b-121">Die [removeregistry-Tabelle](removeregistry-table.md) enthält die Informationen, die aus der Systemregistrierung gelöscht werden, wenn die entsprechende Komponente für die Installation ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cd03b-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="cd03b-122">In der Tabelle "| [atefolder](createfolder-table.md) " sind die Ordner aufgelistet, die während der Installation erstellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cd03b-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="cd03b-123">Obwohl das Installationsprogramm Ordner erstellt, wenn Sie benötigt werden, werden diese entfernt, sobald Sie leer sind.</span><span class="sxs-lookup"><span data-stu-id="cd03b-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="cd03b-124">Die Ordnerliste in der Tabelle "upatefolder" wird erst gelöscht, wenn die Komponente deinstalliert wurde.</span><span class="sxs-lookup"><span data-stu-id="cd03b-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="cd03b-125">Die [Tabelle "muvefile](movefile-table.md) " enthält eine Liste der Dateien, die aus einem angegebenen Quellverzeichnis auf dem Computer des Benutzers in ein Zielverzeichnis verschoben oder kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd03b-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="cd03b-126">Es ist nicht erforderlich, die Tabelle "muvefile" zu verwenden, um die Dateien zu beschreiben, die den Komponenten zugeordnet sind, die Sie installieren.</span><span class="sxs-lookup"><span data-stu-id="cd03b-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="cd03b-127">Um die erforderlichen Bedingungen einzurichten, die erfüllt sein müssen, um die Installation zu initiieren, füllen Sie die LaunchCondition-Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="cd03b-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="cd03b-128">Die [LaunchCondition-Tabelle](launchcondition-table.md) enthält eine Liste mit Bedingungen, die alle erfüllt sein müssen, damit die Aktion erfolgreich ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd03b-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 



