---
description: Im folgenden Beispiel wird veranschaulicht, wie am Ende einer-Installation eine HTML-Datei gestartet wird.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216931"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="a951d-103">Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation</span><span class="sxs-lookup"><span data-stu-id="a951d-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="a951d-104">Im folgenden Beispiel wird veranschaulicht, wie am Ende einer-Installation eine HTML-Datei gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a951d-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="a951d-105">Das Installationsprogramm installiert die Komponente, die die Datei enthält, und veröffentlicht dann am Ende der Installation ein Steuerungs Ereignis, um eine benutzerdefinierte Aktion auszuführen, mit der die Datei geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="a951d-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="a951d-106">Diese Vorgehensweise kann verwendet werden, um am Ende der ersten Installation einer Anwendung ein Hilfe-Tutorial zu starten.</span><span class="sxs-lookup"><span data-stu-id="a951d-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="a951d-107">Das Beispiel muss die folgenden Spezifikationen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="a951d-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="a951d-108">Der Installer führt die benutzerdefinierte Aktion nur aus, wenn die [*vollständige Benutzer*](f-gly.md) Oberflächenebene zum Installieren einer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a951d-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="a951d-109">Das Installationsprogramm führt die benutzerdefinierte Aktion nur aus, wenn die Komponente, die die HTML-Datei enthält, für die lokale Ausführung auf dem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="a951d-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="a951d-110">Die benutzerdefinierte Aktion wird nur bei der ersten Installation der Anwendung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a951d-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="a951d-111">Wenn die benutzerdefinierte Aktion fehlschlägt, schlägt die Installation fehl.</span><span class="sxs-lookup"><span data-stu-id="a951d-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="a951d-112">Das Beispiel enthält eine hypothetische Komponente mit dem Namen Tutorial, mit der mindestens eine Ressource, eine Datei mit dem Namen tutorial.htm, gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="a951d-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="a951d-113">Der Bezeichner für diese Datei in der Spalte Datei der Dateitabelle ist Tutorial.</span><span class="sxs-lookup"><span data-stu-id="a951d-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="a951d-114">In der folgenden Erläuterung wird davon ausgegangen, dass Sie bereits die für das Lernprogramm erforderlichen Ressourcen erstellt und alle erforderlichen Einträge in den Tabellen [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)und [FeatureComponents](featurecomponents-table.md) vorgenommen haben, um diese Komponente zu installieren.</span><span class="sxs-lookup"><span data-stu-id="a951d-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="a951d-115">Weitere Informationen finden Sie unter [einem Installations Beispiel](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="a951d-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="a951d-116">Die folgenden Themen enthalten Informationen zum Erstellen erforderlicher benutzerdefinierter Aktionen und zum Hinzufügen zu einem-Installationspaket.</span><span class="sxs-lookup"><span data-stu-id="a951d-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="a951d-117">Erstellen der benutzerdefinierten Aktion "starten"</span><span class="sxs-lookup"><span data-stu-id="a951d-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="a951d-118">Hinzufügen von Start zu den Tabellen CustomAction und Binary</span><span class="sxs-lookup"><span data-stu-id="a951d-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="a951d-119">Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts</span><span class="sxs-lookup"><span data-stu-id="a951d-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



