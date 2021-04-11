---
description: Mit der Aktion "Aktion erstellen" wird die Erstellung von Verknüpfungen verwaltet.
ms.assetid: 2e8a30ec-e8e7-4855-addb-2501bf85ab54
title: Aktion "kreateshortcuts"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e59ae3cdcc9d35091690742322617f3c9d07628
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050362"
---
# <a name="createshortcuts-action"></a><span data-ttu-id="09c7f-103">Aktion "kreateshortcuts"</span><span class="sxs-lookup"><span data-stu-id="09c7f-103">CreateShortcuts Action</span></span>

<span data-ttu-id="09c7f-104">Mit der Aktion "Aktion erstellen" wird die Erstellung von Verknüpfungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="09c7f-104">The CreateShortcuts action manages the creation of shortcuts.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="09c7f-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="09c7f-105">Sequence Restrictions</span></span>

<span data-ttu-id="09c7f-106">Die Aktion "Aktion durchsetzen" muss nach der Aktion " [InstallFiles](installfiles-action.md) " und der Aktion " [removeshortcuts](removeshortcuts-action.md) " erfolgen.</span><span class="sxs-lookup"><span data-stu-id="09c7f-106">The CreateShortcuts action must come after the [InstallFiles](installfiles-action.md) action and the [RemoveShortcuts](removeshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="09c7f-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="09c7f-107">ActionData Messages</span></span>



| <span data-ttu-id="09c7f-108">Feld</span><span class="sxs-lookup"><span data-stu-id="09c7f-108">Field</span></span> | <span data-ttu-id="09c7f-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="09c7f-109">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="09c7f-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="09c7f-110">\[1\]</span></span> | <span data-ttu-id="09c7f-111">Bezeichner der erstellten Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="09c7f-111">Identifier of created shortcut.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="09c7f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09c7f-112">Remarks</span></span>

<span data-ttu-id="09c7f-113">Mit der Aktion "| ateshortcuts" werden Verknüpfungen zu den Schlüsseldateien von Komponenten von Features erstellt, die für die Installation oder Ankündigung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="09c7f-113">The CreateShortcuts action creates shortcuts to the key files of components of features that are selected for installation or advertisement.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09c7f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09c7f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c7f-115">Verknüpfungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="09c7f-115">Shortcut Table</span></span>](shortcut-table.md)
</dt> <dt>

[<span data-ttu-id="09c7f-116">Msishortcutproperty-Tabelle</span><span class="sxs-lookup"><span data-stu-id="09c7f-116">MsiShortcutProperty Table</span></span>](msishortcutproperty-table.md)
</dt> </dl>

 

 



