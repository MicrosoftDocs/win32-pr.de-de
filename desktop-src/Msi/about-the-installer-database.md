---
description: Die Windows Installer-Datenbank besteht aus vielen miteinander verknüpften Tabellen, die zusammen eine relationale Datenbank mit den für die Installation einer Gruppe von Anwendungen erforderlichen Informationen bilden.
ms.assetid: 3352dd8f-c082-4c4b-98be-5823c8b28f07
title: Informationen zur Installer-Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f0ee2cc326f85d964ac3d845b97751a48fbb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864535"
---
# <a name="about-the-installer-database"></a><span data-ttu-id="4c5bc-103">Informationen zur Installer-Datenbank</span><span class="sxs-lookup"><span data-stu-id="4c5bc-103">About the Installer Database</span></span>

<span data-ttu-id="4c5bc-104">Die Windows Installer-Datenbank besteht aus vielen miteinander verknüpften Tabellen, die zusammen eine relationale Datenbank mit den für die Installation einer Gruppe von Anwendungen erforderlichen Informationen bilden.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-104">The Windows Installer database consists of many interrelated tables that together comprise a relational database of the information necessary to install a group of applications.</span></span> <span data-ttu-id="4c5bc-105">Da die Datenbank relational ist, werden die Tabellen über die Daten in den Primär-und Fremdschlüssel Werten verknüpft.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-105">Because the database is relational, the tables are linked through the data in the primary and foreign key values.</span></span> <span data-ttu-id="4c5bc-106">Dies stellt eine effiziente Methode zum Ändern des Installationsvorgangs dar und bedeutet, dass Benutzer eine große Anwendung oder Anwendungs Gruppe leichter anpassen können.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-106">This provides an efficient method for changing the installation process and means that users can more easily customize a large application or group of applications.</span></span> <span data-ttu-id="4c5bc-107">Die Datenbanktabellen spiegeln das allgemeine Layout der gesamten Gruppe von Anwendungen wider, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="4c5bc-107">The database tables reflect the general layout of the entire group of applications, including:</span></span>

-   <span data-ttu-id="4c5bc-108">Verfügbare Features</span><span class="sxs-lookup"><span data-stu-id="4c5bc-108">Available features</span></span>
-   <span data-ttu-id="4c5bc-109">Komponenten</span><span class="sxs-lookup"><span data-stu-id="4c5bc-109">Components</span></span>
-   <span data-ttu-id="4c5bc-110">Beziehung zwischen Features und Komponenten</span><span class="sxs-lookup"><span data-stu-id="4c5bc-110">Relationship between features and components</span></span>
-   <span data-ttu-id="4c5bc-111">Erforderliche Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="4c5bc-111">Necessary registry settings</span></span>
-   <span data-ttu-id="4c5bc-112">Benutzeroberfläche für die Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c5bc-112">User interface for the application</span></span>

<span data-ttu-id="4c5bc-113">Zum Erstellen einer Installations Datenbank müssen Sie die Tabellen mit allen Informationen über die Anwendungen und den Installationsvorgang auffüllen.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-113">To create an installation database, you must populate the tables with all the information about the applications and the installation process.</span></span> <span data-ttu-id="4c5bc-114">Das manuelle Erstellen dieser Tabellen wird zu einer großen Aufgabe, auch bei einer mittleren Größen Installation. Daher stehen einige Tools von Drittanbietern zur Verfügung, die Sie beim Aufbau der Installer-Datenbank unterstützen.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-114">Manually authoring all these tables becomes a large task even for a moderate size installation; therefore some third-party tools are available to assist with building the installer database.</span></span> <span data-ttu-id="4c5bc-115">In den folgenden Abschnitten werden Gruppen verwandter Datenbanktabellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4c5bc-115">The following sections describe groups of related database tables.</span></span>

[<span data-ttu-id="4c5bc-116">Kern Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="4c5bc-116">Core Tables Group</span></span>](core-tables-group.md)

[<span data-ttu-id="4c5bc-117">Datei Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="4c5bc-117">File Tables Group</span></span>](file-tables-group.md)

[<span data-ttu-id="4c5bc-118">Registrierungs Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="4c5bc-118">Registry Tables Group</span></span>](registry-tables-group.md)

[<span data-ttu-id="4c5bc-119">System Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="4c5bc-119">System Tables Group</span></span>](system-tables-group.md)

[<span data-ttu-id="4c5bc-120">Locator-Tabellen Gruppe</span><span class="sxs-lookup"><span data-stu-id="4c5bc-120">Locator Tables Group</span></span>](locator-tables-group.md)

[<span data-ttu-id="4c5bc-121">Gruppe "Programm Informationstabellen"</span><span class="sxs-lookup"><span data-stu-id="4c5bc-121">Program Information Tables Group</span></span>](program-information-tables-group.md)

[<span data-ttu-id="4c5bc-122">Gruppe "Installationsprozedur Tabellen"</span><span class="sxs-lookup"><span data-stu-id="4c5bc-122">Installation Procedure Tables Group</span></span>](installation-procedure-tables-group.md)

[<span data-ttu-id="4c5bc-123">Legende des Entitäts Beziehungs Diagramms</span><span class="sxs-lookup"><span data-stu-id="4c5bc-123">Entity Relationship Diagram Legend</span></span>](entity-relationship-diagram-legend.md)

[<span data-ttu-id="4c5bc-124">Text Archivdateien</span><span class="sxs-lookup"><span data-stu-id="4c5bc-124">Text Archive Files</span></span>](text-archive-files.md)

<span data-ttu-id="4c5bc-125">Eine vollständige Liste aller Tabellen in einer-Installations Datenbank finden Sie unter [Datenbanktabellen](database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="4c5bc-125">For a complete list of all tables in an installation database, see [Database Tables](database-tables.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c5bc-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c5bc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c5bc-127">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="4c5bc-127">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



