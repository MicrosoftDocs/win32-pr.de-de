---
description: Zum Generieren eines Mergemoduls müssen Sie ein Software Tool abrufen, mit dem eine MSM-Datei bearbeitet werden kann.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Abrufen von mergemodulauthoring-Tools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dac673c7cfa191cecb1b576e1b17f2f4a7a1f4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356562"
---
# <a name="obtaining-merge-module-authoring-tools"></a><span data-ttu-id="7bf22-103">Abrufen von mergemodulauthoring-Tools</span><span class="sxs-lookup"><span data-stu-id="7bf22-103">Obtaining Merge Module Authoring Tools</span></span>

<span data-ttu-id="7bf22-104">Zum Generieren eines Mergemoduls müssen Sie ein Software Tool abrufen, mit dem eine MSM-Datei bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7bf22-104">To generate a merge module, you need to obtain a software tool with which to edit an .msm file.</span></span> <span data-ttu-id="7bf22-105">Da es sich bei einer MSM-Datei im Grunde um eine vereinfachte MSI-Datei handelt, können Sie möglicherweise dieselben Tools verwenden, die auch zum Erstellen einer Installations Datenbank verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="7bf22-105">Because an .msm file is basically a simplified .msi file, you may be able to use the same tools used to create an installation database.</span></span> <span data-ttu-id="7bf22-106">Beispielsweise Orca.exe die Anwendung mit dem Windows Installer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7bf22-106">For example, the application Orca.exe provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="7bf22-107">Eine Alternative besteht darin, eines der Installer-Paket Erstellungs Tools zu erwerben, die von unabhängigen Softwareanbietern zur Verfügung gestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7bf22-107">An alternative is to purchase one of the installer packaging tools to be available from independent software vendors.</span></span> <span data-ttu-id="7bf22-108">Es gibt mehrere Tools von Drittanbietern, die für die Erstellung von Mergemodulen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7bf22-108">There are several third-party tools under development that may be used for producing merge modules.</span></span> <span data-ttu-id="7bf22-109">Wenn Sie sich für die Verwendung eines Drittanbieter Tools entscheiden, sollten Sie sicherstellen, dass Mergemodule generiert werden, die mit dem in diesem Dokument beschriebenen Standard übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7bf22-109">If you choose to use a third-party tool you should verify that it generates merge modules that are consistent with the standard described in this document.</span></span> <span data-ttu-id="7bf22-110">Insbesondere sollten Sie feststellen, dass die Bearbeitungs Tools für das Mergemodul keines der folgenden Aktionen durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="7bf22-110">In particular, you should determine that the editing tools have not done any of the following to the merge module.</span></span>

-   <span data-ttu-id="7bf22-111">Dem Mergemodul wurden überflüssige Tabellen hinzugefügt, auf die in der [Tabelle "moduleignoretable](moduleignoretable-table.md)" nicht verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7bf22-111">Added extraneous tables to the merge module that are not referenced in the [ModuleIgnoreTable table](moduleignoretable-table.md).</span></span>

    <span data-ttu-id="7bf22-112">Löschen Sie diese Tabellen, oder fügen Sie Sie der Tabelle moduleignoretable hinzu.</span><span class="sxs-lookup"><span data-stu-id="7bf22-112">Delete these tables or add them to the ModuleIgnoreTable table.</span></span>

-   <span data-ttu-id="7bf22-113">Dem Mergemodul wurde eine unnötige [TextStyle-Tabelle](textstyle-table.md) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7bf22-113">Added an unnecessary [TextStyle table](textstyle-table.md) to the merge module.</span></span>

    <span data-ttu-id="7bf22-114">Wenn das Mergemodul über keine Benutzeroberfläche verfügt (was in der Regel nicht der Fall ist), können Sie diese Tabelle gefahrlos löschen.</span><span class="sxs-lookup"><span data-stu-id="7bf22-114">If your merge module has no UI (and it generally should not) you can safely delete this table.</span></span>

-   <span data-ttu-id="7bf22-115">Der [Verzeichnis Tabelle](directory-table.md)wurden unnötige Einträge hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7bf22-115">Added unnecessary entries to the [Directory table](directory-table.md).</span></span>

    <span data-ttu-id="7bf22-116">Entfernen Sie unnötige Einträge aus der Verzeichnis Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7bf22-116">Remove unnecessary entries from the Directory table.</span></span>

-   <span data-ttu-id="7bf22-117">Linke Informationen aus der Validierungs Tabelle des Mergemoduls \_ .</span><span class="sxs-lookup"><span data-stu-id="7bf22-117">Left information out of the merge module's \_Validation table.</span></span>

    <span data-ttu-id="7bf22-118">Dadurch wird die mergemodulvalidierung verhindert.</span><span class="sxs-lookup"><span data-stu-id="7bf22-118">This prevents merge module validation.</span></span> <span data-ttu-id="7bf22-119">Fügen Sie eine komplette \_ Validierungs Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7bf22-119">Add a complete \_Validation table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bf22-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bf22-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bf22-121">Erstellen von Benutzeroberflächen in Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7bf22-121">Authoring User Interfaces in Merge Modules</span></span>](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="7bf22-122">Erstellen von mergemodulverzeichnistabellen</span><span class="sxs-lookup"><span data-stu-id="7bf22-122">Authoring Merge Module Directory Tables</span></span>](authoring-merge-module-directory-tables.md)
</dt> <dt>

[<span data-ttu-id="7bf22-123">Validieren von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="7bf22-123">Validating Merge Modules</span></span>](validating-merge-modules.md)
</dt> </dl>

 

 



