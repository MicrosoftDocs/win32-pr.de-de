---
description: Die RemoveFiles-Aktion entfernt Dateien, die zuvor von der InstallFiles-Aktion installiert wurden.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: RemoveFiles-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349348"
---
# <a name="removefiles-action"></a><span data-ttu-id="d3800-103">RemoveFiles-Aktion</span><span class="sxs-lookup"><span data-stu-id="d3800-103">RemoveFiles Action</span></span>

<span data-ttu-id="d3800-104">Die RemoveFiles-Aktion entfernt Dateien, die zuvor von der [InstallFiles](installfiles-action.md) -Aktion installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d3800-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="d3800-105">Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Komponenten](component-table.md) Tabelle abgegrenzt.</span><span class="sxs-lookup"><span data-stu-id="d3800-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="d3800-106">Nur die Dateien, deren Komponenten entweder in den Zustand " *msiinstallstatemissing* " oder " *msiinstallstatelocal* " aufgelöst werden, wenn die Komponente lokal installiert ist, werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3800-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="d3800-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="d3800-107">Sequence Restrictions</span></span>

<span data-ttu-id="d3800-108">Die [InstallValidate](installvalidate-action.md) -Aktion muss vor dem Aufrufen von RemoveFiles aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d3800-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="d3800-109">Wenn eine [InstallFiles](installfiles-action.md) -Aktion verwendet wird, muss Sie nach RemoveFiles angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3800-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="d3800-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="d3800-110">ActionData Messages</span></span>



| <span data-ttu-id="d3800-111">Feld</span><span class="sxs-lookup"><span data-stu-id="d3800-111">Field</span></span> | <span data-ttu-id="d3800-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="d3800-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="d3800-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="d3800-113">\[1\]</span></span> | <span data-ttu-id="d3800-114">Bezeichner der entfernten Datei.</span><span class="sxs-lookup"><span data-stu-id="d3800-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="d3800-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="d3800-115">\[9\]</span></span> | <span data-ttu-id="d3800-116">Der Bezeichner des Verzeichnisses, das die entfernte Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d3800-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d3800-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3800-117">Remarks</span></span>

<span data-ttu-id="d3800-118">Die Tabelle " [RemoveFile](removefile-table.md) " kann aus der Installer-Datenbank weggelassen werden, wenn keine anderen Dateien entfernt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d3800-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="d3800-119">Mit der Aktion RemoveFiles können auch vom Autor angegebene Dateien entfernt werden, die nicht von der InstallFiles-Aktion installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d3800-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="d3800-120">Diese Dateien werden in der Tabelle " [RemoveFile](removefile-table.md) " angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3800-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="d3800-121">Jede dieser Dateien wird durch einen Link zu einem Eintrag in der [Komponenten](component-table.md) Tabelle abgegrenzt.</span><span class="sxs-lookup"><span data-stu-id="d3800-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="d3800-122">Die Dateien, deren Komponenten in einen aktiven Aktionszustand aufgelöst werden (d. h. nicht in den Status OFF oder NULL), werden entfernt, wenn die Datei im angegebenen Verzeichnis vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d3800-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="d3800-123">Es wird versucht, die in der Tabelle "RemoveFile" angegebenen Dateien zu entfernen, wenn die verknüpfte Komponente zum ersten Mal installiert wird, während einer Neuinstallation und erneut, wenn die verknüpfte Komponente entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d3800-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="d3800-124">Mit der Aktion RemoveFiles können auch Ordner entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d3800-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="d3800-125">Wenn der Wert in der Dateiname-Spalte der RemoveFile-Tabelle NULL ist, wird ein leerer Ordner entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3800-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="d3800-126">Beim Entfernen zuvor installierter Dateien werden die gleichen Felder in denselben Tabellen abgefragt, die von der [InstallFiles](installfiles-action.md) -Aktion abgefragt wurden, mit der Ausnahme, dass die [Medien Tabelle](media-table.md) nicht von der RemoveFiles-Aktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d3800-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="d3800-127">Der Ziel Dateiname kann in lokalisiertem Text in der Dateiname-Spalte der RemoveFile-Tabelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3800-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



