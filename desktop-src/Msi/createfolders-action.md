---
description: Mit der Aktion "Aktionen erstellen" werden leere Ordner für Komponenten erstellt, die für die Installation festgelegt sind.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Aktion "kreatefolders"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366241"
---
# <a name="createfolders-action"></a><span data-ttu-id="70073-103">Aktion "kreatefolders"</span><span class="sxs-lookup"><span data-stu-id="70073-103">CreateFolders Action</span></span>

<span data-ttu-id="70073-104">Mit der Aktion "Aktionen erstellen" werden leere Ordner für Komponenten erstellt, die für die Installation festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="70073-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="70073-105">Das Installationsprogramm erstellt Ordner für Komponenten, die lokal ausgeführt werden und von der Quelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70073-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="70073-106">Neu erstellte Ordner werden mit dem entsprechenden Komponenten Bezeichner registriert.</span><span class="sxs-lookup"><span data-stu-id="70073-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="70073-107">Mit der Aktion "Up Folder" werden die Tabelle "die [Tabelle](createfolder-table.md) " und die [Komponenten Tabelle](component-table.md)abgefragt.</span><span class="sxs-lookup"><span data-stu-id="70073-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="70073-108">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="70073-108">Sequence Restrictions</span></span>

<span data-ttu-id="70073-109">Die Aktion "up Folders" muss entweder vor der Aktion " [InstallFiles](installfiles-action.md) " oder vor einer Aktion ausgeführt werden, durch die Dateien zu Ordnern hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="70073-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="70073-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="70073-110">ActionData Messages</span></span>



| <span data-ttu-id="70073-111">Feld</span><span class="sxs-lookup"><span data-stu-id="70073-111">Field</span></span> | <span data-ttu-id="70073-112">Beschreibung der Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="70073-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="70073-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="70073-113">\[1\]</span></span> | <span data-ttu-id="70073-114">Verzeichnis Bezeichner des Ordners.</span><span class="sxs-lookup"><span data-stu-id="70073-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="70073-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70073-115">Remarks</span></span>

<span data-ttu-id="70073-116">Beim Deinstallieren der Anwendung werden von der Aktion "Aktionen erstellen" erstellte Ordner nicht automatisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="70073-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="70073-117">Der Installer entfernt nur Ordner, wenn die Aktion [RemoveFolders](removefolders-action.md) in der Aktions Sequenz enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="70073-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



