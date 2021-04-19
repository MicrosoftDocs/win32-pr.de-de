---
description: Bevor Sie Datei Vorgänge in der Liste der Speicherplätze hinzufügen oder entfernen können, müssen Sie Sie mithilfe der setupkreatediskspacelist-Funktion erstellen.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Verwenden der Disk-Space Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349789"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="56ab9-103">Verwenden der Disk-Space Liste</span><span class="sxs-lookup"><span data-stu-id="56ab9-103">Using the Disk-Space List</span></span>

<span data-ttu-id="56ab9-104">Bevor Sie Datei Vorgänge in der Liste der Speicherplätze hinzufügen oder entfernen können, müssen Sie Sie mithilfe der [**setupkreatediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) -Funktion erstellen.</span><span class="sxs-lookup"><span data-stu-id="56ab9-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="56ab9-105">Nachdem Sie eine Speicherplatz Liste erstellt haben, können Sie mithilfe von [**setupadddediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista)einzelne Datei Kopier-oder Löschvorgänge zur Liste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="56ab9-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="56ab9-106">Wenn Sie alle Datei Kopier-oder Löschvorgänge in einem gesamten INF-Abschnitt hinzufügen möchten, verwenden Sie entweder die [**setupaddsectiondediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) -oder die [**setupaddinstallsectiondediskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="56ab9-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="56ab9-107">Nachdem Sie alle Installations Vorgänge der Liste Speicherplatz hinzugefügt haben, können Sie Sie Abfragen, um herauszufinden, wie viel Speicherplatz für die angegebene Installation erforderlich ist, indem Sie die [**setupqueryspacerequiredondrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="56ab9-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="56ab9-108">Die [**setupquerydrivesindiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) -Funktion gibt die Laufwerk Spezifikationen für jedes Ziellaufwerk zurück, auf das in den Datei Vorgängen auf der Speicherplatz Liste verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="56ab9-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="56ab9-109">Sie können diese Informationen verwenden, um den verfügbaren Speicherplatz auf diesen Laufwerken Programm gesteuert mit dem für die Installation erforderlichen Speicherplatz zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="56ab9-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="56ab9-110">Um einen Datei Vorgang aus der Liste der Speicherplätze zu entfernen, verwenden Sie die Funktion [**setupremuvefromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="56ab9-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="56ab9-111">Um alle Kopier-oder Löschvorgänge für Dateien aus einem gesamten INF-Abschnitt zu entfernen, verwenden Sie die Funktion [**setupremuvesectionfromdiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) oder [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="56ab9-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="56ab9-112">Nachdem die Speicherplatz Liste nicht mehr benötigt wird, können Sie die Ihnen zugeordneten Ressourcen freigeben, indem Sie die [**setupdestroydiskspacelist**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="56ab9-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



