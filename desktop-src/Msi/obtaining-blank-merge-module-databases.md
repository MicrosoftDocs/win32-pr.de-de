---
description: Abrufen einer leeren mergemoduldatenbank. Sie können die Datei Schema. msm verwenden, die mit dem Windows Installer SDK bereitgestellt wird, als Start Datenbank für das Mergemodul. Weitere Informationen finden Sie unter Windows SDK Komponenten für Windows Installer Entwickler.
ms.assetid: 8408e892-adc6-4ef5-ad36-4d04c021c899
title: Abrufen von leeren mergemoduldatenbanken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba75d55763d30b0ab545d2dbddbc19c1b0c279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343804"
---
# <a name="obtaining-blank-merge-module-databases"></a><span data-ttu-id="16bd1-105">Abrufen von leeren mergemoduldatenbanken</span><span class="sxs-lookup"><span data-stu-id="16bd1-105">Obtaining Blank Merge Module Databases</span></span>

<span data-ttu-id="16bd1-106">Abrufen einer leeren mergemoduldatenbank.</span><span class="sxs-lookup"><span data-stu-id="16bd1-106">Obtain a blank merge module database.</span></span> <span data-ttu-id="16bd1-107">Sie können die Datei Schema. msm verwenden, die mit dem Windows Installer SDK bereitgestellt wird, als Start Datenbank für das Mergemodul.</span><span class="sxs-lookup"><span data-stu-id="16bd1-107">You can use the file Schema.msm provided with the Windows Installer SDK as a starting database for your merge module.</span></span> <span data-ttu-id="16bd1-108">Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="16bd1-108">For more information, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="16bd1-109">Entwickler sollten Mergemodule mithilfe des einfachsten Datenbankschemas erstellen, das Ihre Komponenten installiert.</span><span class="sxs-lookup"><span data-stu-id="16bd1-109">Developers should author merge modules using the simplest database schema that installs their components.</span></span> <span data-ttu-id="16bd1-110">Durch die Verwendung eines einfachen Schemas wird die höchste Kompatibilität für das Mergemodul sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="16bd1-110">The use of a simple schema ensures the greatest compatibility for the merge module.</span></span> <span data-ttu-id="16bd1-111">Das Zusammenführen eines Mergemoduls in ein Installationspaket mit einem anderen Datenbankschema führt in der Regel zu Mergekonflikten.</span><span class="sxs-lookup"><span data-stu-id="16bd1-111">Merging a merge module into an installation package with a different database schema usually results in merge conflicts.</span></span>

<span data-ttu-id="16bd1-112">Eine vollständige Liste aller erforderlichen und optionalen Tabellen in Mergemodulen finden Sie unter [Merge Module Database Tables](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="16bd1-112">For a complete list of all the required and optional tables in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span>

 

 



