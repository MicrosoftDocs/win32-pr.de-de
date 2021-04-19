---
description: Die unregisterfonts-Aktion entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.
ms.assetid: 97cbbcbe-eb1c-45f0-91d2-4b17984498ae
title: Unregisterfonts-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fcc847203b72b0e2d92fb5e9a4dc465bebb001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359600"
---
# <a name="unregisterfonts-action"></a><span data-ttu-id="e7709-103">Unregisterfonts-Aktion</span><span class="sxs-lookup"><span data-stu-id="e7709-103">UnregisterFonts Action</span></span>

<span data-ttu-id="e7709-104">Die unregisterfonts-Aktion entfernt Registrierungsinformationen zu installierten Schriftarten aus dem System.</span><span class="sxs-lookup"><span data-stu-id="e7709-104">The UnregisterFonts action removes registration information about installed fonts from the system.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="e7709-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="e7709-105">Sequence Restrictions</span></span>

<span data-ttu-id="e7709-106">Die [RemoveFiles](removefiles-action.md) -Aktion muss nach ' unregisterfonts ' aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e7709-106">The [RemoveFiles](removefiles-action.md) action must be called after UnregisterFonts.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="e7709-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="e7709-107">ActionData Messages</span></span>



| <span data-ttu-id="e7709-108">Feld</span><span class="sxs-lookup"><span data-stu-id="e7709-108">Field</span></span> | <span data-ttu-id="e7709-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="e7709-109">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="e7709-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="e7709-110">\[1\]</span></span> | <span data-ttu-id="e7709-111">Schriftart Datei.</span><span class="sxs-lookup"><span data-stu-id="e7709-111">Font file.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="e7709-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7709-112">Remarks</span></span>

<span data-ttu-id="e7709-113">Die unregisterfonts-Aktion wird ausgeführt, wenn die Datei, die in der Datei \_ Spalte der [Schriftart Tabelle](font-table.md) angegeben ist, zu einer Komponente gehört, die deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="e7709-113">The UnregisterFonts action is executed if the file specified in the File\_ column of the [Font table](font-table.md) belongs to a component being uninstalled.</span></span>

 

 



