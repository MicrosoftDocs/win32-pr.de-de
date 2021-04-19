---
description: Bei Sicherungs-und Wiederherstellungs Vorgängen werden Dateien in der Regel von einem angegebenen Standard Speicherort auf einem Datenträger auf ein Sicherungsmedium kopiert und dann von diesem Medium wieder am gleichen Standard Speicherort auf dem Datenträger
ms.assetid: 7609c392-d5f8-48c2-8e7e-f35f56cf94f8
title: Nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c809b886886c1d84de1cc3960163a7cc94179cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367873"
---
# <a name="non-default-backup-and-restore-locations"></a><span data-ttu-id="896fd-103">Nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte</span><span class="sxs-lookup"><span data-stu-id="896fd-103">Non-Default Backup and Restore Locations</span></span>

<span data-ttu-id="896fd-104">Bei Sicherungs-und Wiederherstellungs Vorgängen werden Dateien in der Regel von einem angegebenen Standard Speicherort auf einem Datenträger auf ein Sicherungsmedium kopiert und dann von diesem Medium wieder am gleichen Standard Speicherort auf dem Datenträger</span><span class="sxs-lookup"><span data-stu-id="896fd-104">Backup and restore operations typically copy files from a given, default location on disk to backup media and then restore from that media to the same default location on disk.</span></span>

<span data-ttu-id="896fd-105">Es gibt viele Gründe, insbesondere beim Umgang mit laufenden Prozessen, nicht um dieses einfache Modell zu befolgen.</span><span class="sxs-lookup"><span data-stu-id="896fd-105">There are many reasons, particularly when dealing with running processes, not to follow this simple model.</span></span> <span data-ttu-id="896fd-106">VSS unterstützt die Verwendung von nicht standardmäßigen Quellen für die Sicherung und Alternative Ziele für die Wiederherstellung und umfasst Mechanismen zum Arbeiten mit Teilmengen von Dateien und zum erneuten Zuordnen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="896fd-106">VSS supports using nonstandard sources for backup and alternate destinations for restore, and includes mechanisms to work with subsets of files and to remap files.</span></span>

-   [<span data-ttu-id="896fd-107">Arbeiten mit alternativen Pfaden während der Sicherung</span><span class="sxs-lookup"><span data-stu-id="896fd-107">Working with Alternate Paths during Backup</span></span>](working-with-alternate-paths-during-backup.md)
-   [<span data-ttu-id="896fd-108">Arbeiten mit alternativen Speicherorten während der Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="896fd-108">Working with Alternate Locations during Restore</span></span>](working-with-alternate-locations-during-restore.md)
-   [<span data-ttu-id="896fd-109">Arbeiten mit neuen Zielen während der Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="896fd-109">Working with New Targets during Restore</span></span>](working-with-new-targets-during-restore.md)
-   [<span data-ttu-id="896fd-110">Arbeiten mit partiellen Dateien</span><span class="sxs-lookup"><span data-stu-id="896fd-110">Working with Partial Files</span></span>](working-with-partial-files.md)
-   [<span data-ttu-id="896fd-111">Arbeiten mit gerichteten Zielen</span><span class="sxs-lookup"><span data-stu-id="896fd-111">Working with Directed Targets</span></span>](working-with-directed-targets.md)

 

 



