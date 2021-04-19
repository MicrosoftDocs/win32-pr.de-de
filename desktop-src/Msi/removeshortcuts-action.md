---
description: Mit der removeshortcuts-Aktion wird das Entfernen einer angekündigten Verknüpfung, deren Funktion für die Deinstallation ausgewählt ist, oder eine nicht angekündigte Verknüpfung, deren Komponente für die Deinstallation ausgewählt ist, verwaltet. Weitere Informationen finden Sie in der Verknüpfungs Tabelle.
ms.assetid: 897e8a13-d9c5-4f98-8785-c0f053a11f3d
title: Removeshortcuts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151f5fac6733e61b7ba27320a5e79c522abcc3e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363541"
---
# <a name="removeshortcuts-action"></a><span data-ttu-id="cb4a5-104">Removeshortcuts-Aktion</span><span class="sxs-lookup"><span data-stu-id="cb4a5-104">RemoveShortcuts Action</span></span>

<span data-ttu-id="cb4a5-105">Mit der removeshortcuts-Aktion wird das Entfernen einer angekündigten Verknüpfung, deren Funktion für die Deinstallation ausgewählt ist, oder eine nicht angekündigte Verknüpfung, deren Komponente für die Deinstallation ausgewählt ist, verwaltet.</span><span class="sxs-lookup"><span data-stu-id="cb4a5-105">The RemoveShortcuts action manages the removal of an advertised shortcut whose feature is selected for uninstallation or a nonadvertised shortcut whose component is selected for uninstallation.</span></span> <span data-ttu-id="cb4a5-106">Weitere Informationen finden Sie in der Verknüpfungs [Tabelle](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="cb4a5-106">For more information, see the [Shortcut Table](shortcut-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cb4a5-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="cb4a5-107">Sequence Restrictions</span></span>

<span data-ttu-id="cb4a5-108">Die removeshortcuts-Aktion muss vor der Aktion " [kreateshortcuts](createshortcuts-action.md) " erfolgen.</span><span class="sxs-lookup"><span data-stu-id="cb4a5-108">The RemoveShortcuts action must come before the [CreateShortcuts](createshortcuts-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cb4a5-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="cb4a5-109">ActionData Messages</span></span>



| <span data-ttu-id="cb4a5-110">Feld</span><span class="sxs-lookup"><span data-stu-id="cb4a5-110">Field</span></span> | <span data-ttu-id="cb4a5-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="cb4a5-111">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="cb4a5-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cb4a5-112">\[1\]</span></span> | <span data-ttu-id="cb4a5-113">Bezeichner der entfernten Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="cb4a5-113">Identifier of removed shortcut.</span></span> |



 

 

 



