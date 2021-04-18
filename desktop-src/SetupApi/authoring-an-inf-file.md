---
description: Wenn Sie eine INF-Datei für eine Setup Anwendung erstellen, sollten Sie auch auf das INF-Dateiformat verweisen, das unter Allgemeine Richtlinien für INF-Dateien und INF-Datei Abschnitte und Direktiven des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Erstellen einer INF-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347737"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="828ba-103">Erstellen einer INF-Datei</span><span class="sxs-lookup"><span data-stu-id="828ba-103">Authoring an INF file</span></span>

<span data-ttu-id="828ba-104">Wenn Sie eine INF-Datei für eine Setup Anwendung erstellen, sollten Sie auch auf das INF-Dateiformat verweisen, das unter *Allgemeine Richtlinien für INF-Dateien* und *INF-Datei Abschnitte und Direktiven* des Microsoft Windows 2000 Driver Development Kit dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="828ba-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="828ba-105">Wenn Sie die INF-Dateien für eine Setup Anwendung erstellen, befolgen Sie die folgenden Regeln.</span><span class="sxs-lookup"><span data-stu-id="828ba-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="828ba-106">Ein **Versions** Abschnitt ist in jeder INF-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="828ba-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="828ba-107">Abschnitte müssen mit dem Abschnittsnamen beginnen, der von eckigen Klammern () eingeschlossen wird \[ \] .</span><span class="sxs-lookup"><span data-stu-id="828ba-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="828ba-108">Die Namen der Abschnitte **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** und **Version** müssen mit dem Typ des Abschnitts identisch sein.</span><span class="sxs-lookup"><span data-stu-id="828ba-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="828ba-109">Verwenden Sie beispielsweise \[ DestinationDirs \] .</span><span class="sxs-lookup"><span data-stu-id="828ba-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="828ba-110">Autoren können die Namen anderer Abschnitts Typen angeben.</span><span class="sxs-lookup"><span data-stu-id="828ba-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="828ba-111">Die Namen der Abschnitte " **SourceDisksNames** " und " **SourceDisksFiles** " können mit einem plattformspezifischen Suffix angehängt werden.</span><span class="sxs-lookup"><span data-stu-id="828ba-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="828ba-112">Verwenden Sie z. b. zum Anzeigen eines Intel-spezifischen **SourceDisksNames** -Abschnitts " \[ SourceDisksNames. x86" \] .</span><span class="sxs-lookup"><span data-stu-id="828ba-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="828ba-113">Wenn die Setup Funktionen plattformspezifische **SourceDisksNames** -und **SourceDisksFiles** -Abschnitte finden, die mit der Plattform des Benutzers übereinstimmen, verwenden die Funktionen die plattformspezifischen Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="828ba-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="828ba-114">Andernfalls verwenden die Setup Funktionen die nicht-suffixt-Abschnitte " **SourceDisksNames** " und " **SourceDisksFiles** ".</span><span class="sxs-lookup"><span data-stu-id="828ba-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="828ba-115">Mit den Setup Funktionen kann das System des Benutzers Programm gesteuert bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="828ba-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="828ba-116">Weitere Informationen finden Sie im [Abschnitt INF SourceDisksNames und SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="828ba-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="828ba-117">Werte können mithilfe der Form%*strKey*% als ersetzbare Zeichenfolge ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="828ba-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="828ba-118">Verwenden Sie%%, um ein%-Zeichen in der Zeichenfolge zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="828ba-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="828ba-119">Der ' strKey ' muss in einem **String** -Abschnitt der INF-Datei definiert werden.</span><span class="sxs-lookup"><span data-stu-id="828ba-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



