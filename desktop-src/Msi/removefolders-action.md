---
description: Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen. Diese Ordner werden nur entfernt, wenn Sie leer sind. Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponenten Bezeichner aufgehoben.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: RemoveFolders-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216935"
---
# <a name="removefolders-action"></a><span data-ttu-id="56ae9-105">RemoveFolders-Aktion</span><span class="sxs-lookup"><span data-stu-id="56ae9-105">RemoveFolders Action</span></span>

<span data-ttu-id="56ae9-106">Die Aktion RemoveFolders entfernt alle Ordner, die mit Komponenten verknüpft sind, die entfernt oder aus der Quelle ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="56ae9-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="56ae9-107">Diese Ordner werden nur entfernt, wenn Sie leer sind.</span><span class="sxs-lookup"><span data-stu-id="56ae9-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="56ae9-108">Wenn ein Ordner entfernt wird, wird die Registrierung mit dem entsprechenden Komponenten Bezeichner aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="56ae9-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="56ae9-109">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="56ae9-109">Sequence Restrictions</span></span>

<span data-ttu-id="56ae9-110">Die RemoveFolders-Aktion muss nach der [RemoveFiles](removefiles-action.md) -Aktion oder einer beliebigen Aktion erfolgen, die möglicherweise Dateien aus Ordnern entfernt.</span><span class="sxs-lookup"><span data-stu-id="56ae9-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="56ae9-111">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="56ae9-111">ActionData Messages</span></span>



| <span data-ttu-id="56ae9-112">Feld</span><span class="sxs-lookup"><span data-stu-id="56ae9-112">Field</span></span> | <span data-ttu-id="56ae9-113">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="56ae9-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="56ae9-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="56ae9-114">\[1\]</span></span> | <span data-ttu-id="56ae9-115">Der Bezeichner des entfernten Ordners.</span><span class="sxs-lookup"><span data-stu-id="56ae9-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="56ae9-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="56ae9-116">Remarks</span></span>

<span data-ttu-id="56ae9-117">Der Installer entfernt nicht automatisch die Ordner, die von der [Aktion](createfolders-action.md) "Erstellungs Ordner" während einer Deinstallieren der Anwendung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="56ae9-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="56ae9-118">Das Installationsprogramm muss angewiesen werden, diese Ordner zu entfernen, indem Sie die RemoveFolders-Aktion in der Aktions Sequenz erstellen.</span><span class="sxs-lookup"><span data-stu-id="56ae9-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="56ae9-119">Um den Namen und den Speicherort des Ordners anzugeben, verwenden Sie die \_ Spalte Verzeichnis der [Tabelle "Tabelle](createfolder-table.md)".</span><span class="sxs-lookup"><span data-stu-id="56ae9-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="56ae9-120">Es wird davon ausgegangen, dass jeder Ordnername in der Tabelle "foratefolder" eine Eigenschaft ist, die den Ordner Speicherort definiert.</span><span class="sxs-lookup"><span data-stu-id="56ae9-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="56ae9-121">Um die Komponente anzugeben, die den Ordner besitzt, verwenden Sie die Spalte ComponentID der [Component-Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="56ae9-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



