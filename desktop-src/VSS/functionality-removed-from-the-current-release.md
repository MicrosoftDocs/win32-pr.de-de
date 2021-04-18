---
description: 'Die Windows Server 2003-Version von VSS unterstützt nicht mehr Folgendes:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Aus Windows Server 2003 entfernte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343451"
---
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="86b38-103">Aus Windows Server 2003 entfernte Funktionen</span><span class="sxs-lookup"><span data-stu-id="86b38-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="86b38-104">Die Windows Server 2003-Version von VSS unterstützt nicht mehr Folgendes:</span><span class="sxs-lookup"><span data-stu-id="86b38-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="86b38-105">Writer können bei Wiederherstellungs Vorgängen keine neuen Datei Wiederherstellungs Ziele ([*neue Zielspeicher Orte*](vssgloss-n.md)) angeben.</span><span class="sxs-lookup"><span data-stu-id="86b38-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="86b38-106">Das erneute Bereitstellen einer verfügbar gemachten Schatten Kopie als beschreibbares Volume wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="86b38-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="86b38-107">Die **IVssBackupComponents:: remountreadwrite** -Methode ist nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86b38-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="86b38-108">Writer können nicht explizit enthaltene Dateien angeben (mithilfe von [**ivsskreatewritermetadata:: addincludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="86b38-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="86b38-109">Dateien können einer Komponente nur als Teil eines Datei Satzes mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="86b38-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="86b38-110">Dateien können mithilfe von [**ivsskreateschreitermetadata:: addexcludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)weiterhin explizit aus einer Komponente ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="86b38-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



