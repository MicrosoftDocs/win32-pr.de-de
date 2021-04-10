---
description: Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird. Windows Installer verfügt über viele integrierte Standard Aktionen. Entwickler von Installationspaketen können auch eigene benutzerdefinierte Aktionen erstellen.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Standard Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215562"
---
# <a name="standard-actions"></a><span data-ttu-id="54fd8-105">Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="54fd8-105">Standard Actions</span></span>

<span data-ttu-id="54fd8-106">Eine Aktion kapselt eine typische Funktion, die während der Installation oder Wartung einer Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54fd8-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="54fd8-107">Windows Installer verfügt über viele integrierte Standard Aktionen.</span><span class="sxs-lookup"><span data-stu-id="54fd8-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="54fd8-108">Entwickler von Installationspaketen können auch eigene [benutzerdefinierte Aktionen](custom-actions.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="54fd8-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="54fd8-109">Beispiele für Standard Aktionen für den Installer sind:</span><span class="sxs-lookup"><span data-stu-id="54fd8-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="54fd8-110">[Aktion "kreateshortcuts](createshortcuts-action.md)": verwaltet die Erstellung von Verknüpfungen zu Dateien, die mit der aktuellen Anwendung installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="54fd8-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="54fd8-111">Diese Aktion verwendet die Verknüpfungs [Tabelle](shortcut-table.md) für Ihre Daten.</span><span class="sxs-lookup"><span data-stu-id="54fd8-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="54fd8-112">[InstallFiles-Aktion](installfiles-action.md): Kopiert ausgewählte Dateien aus dem Quellverzeichnis in das Zielverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="54fd8-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="54fd8-113">Bei dieser Aktion wird die [Dateitabelle](file-table.md) für die Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="54fd8-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="54fd8-114">[Aktion "schreiteregistryvalues](writeregistryvalues-action.md)": richtet Registrierungsinformationen ein, die die Anwendung in der Registrierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="54fd8-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="54fd8-115">Diese Aktion verwendet die- [Registrierungs Tabelle](registry-table.md) für Ihre Daten.</span><span class="sxs-lookup"><span data-stu-id="54fd8-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="54fd8-116">In den folgenden Abschnitten werden Standard Aktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="54fd8-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="54fd8-117">Informationen zu Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="54fd8-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="54fd8-118">Verwenden von Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="54fd8-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="54fd8-119">Referenz zu Standard Aktionen</span><span class="sxs-lookup"><span data-stu-id="54fd8-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



