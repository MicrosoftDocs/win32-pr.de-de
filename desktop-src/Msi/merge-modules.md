---
description: Mergemodule stellen eine Standardmethode bereit, mit der Entwickler freigegebene Windows Installer Komponenten und Setup Logik für Ihre Anwendungen bereitstellen.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218344"
---
# <a name="merge-modules"></a><span data-ttu-id="f1047-103">Mergemodule</span><span class="sxs-lookup"><span data-stu-id="f1047-103">Merge Modules</span></span>

<span data-ttu-id="f1047-104">Mergemodule stellen eine Standardmethode bereit, mit der Entwickler freigegebene Windows Installer [*Komponenten*](c-gly.md) und Setup Logik für Ihre Anwendungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f1047-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="f1047-105">Mergemodule werden verwendet, um freigegebenen Code, Dateien, Ressourcen, Registrierungseinträge und Setup Logik als einzelne Verbund Datei an Anwendungen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="f1047-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="f1047-106">Entwickler, die neue Mergemodule erstellen oder vorhandene Mergemodule verwenden, sollten den in diesem Abschnitt beschriebenen Standard befolgen.</span><span class="sxs-lookup"><span data-stu-id="f1047-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="f1047-107">Ein Mergemodul ähnelt der Struktur einer vereinfachten Windows Installer [*. msi-Datei*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f1047-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="f1047-108">Allerdings kann ein Mergemodul nicht allein installiert werden, sondern es muss mithilfe eines Merge-Tools in einem Installationspaket zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f1047-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="f1047-109">Entwickler, die Mergemodule verwenden möchten, müssen eines der frei verteilten mergetools (z. b. Mergemod.dll) abrufen oder ein Mergetool von einem unabhängigen Softwarehersteller erwerben.</span><span class="sxs-lookup"><span data-stu-id="f1047-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="f1047-110">Entwickler können neue Mergemodule erstellen, indem Sie viele derselben Software Tools verwenden, die zum Erstellen eines Windows Installer Installationspakets verwendet werden, z. b. den Datenbanktabellen-Editor, der mit dem Windows Installer SDK bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f1047-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="f1047-111">Wenn ein Mergemodul in die MSI-Datei einer Anwendung zusammengeführt wird, werden alle Informationen und Ressourcen, die für die Installation der vom Mergemodul gelieferten Komponenten erforderlich sind, in die MSI-Datei der Anwendung integriert.</span><span class="sxs-lookup"><span data-stu-id="f1047-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="f1047-112">Das Mergemodul ist dann nicht mehr erforderlich, um diese Komponenten zu installieren, und das Mergemodul muss für einen Benutzer nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f1047-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="f1047-113">Da alle Informationen, die zum Installieren der Komponenten erforderlich sind, als einzelne Datei bereitgestellt werden, können durch die Verwendung von Mergemodulen viele Instanzen von Versions Konflikten, fehlende Registrierungseinträge und nicht ordnungsgemäß installierte Dateien eliminiert werden.</span><span class="sxs-lookup"><span data-stu-id="f1047-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="f1047-114">Weitere Informationen zu Mergemodulen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="f1047-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="f1047-115">Informationen zu Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="f1047-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="f1047-116">Verwenden von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="f1047-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="f1047-117">Modul Verweis zusammenführen</span><span class="sxs-lookup"><span data-stu-id="f1047-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 



