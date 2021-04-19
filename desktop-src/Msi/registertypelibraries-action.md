---
description: Mit der registertypelibraries-Aktion werden Typbibliotheken beim System registriert. Diese Aktion wird auf jede Datei angewendet, auf die in der TypeLib-Tabelle verwiesen wird, die für die Installation geplant ist.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Registertypelibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353443"
---
# <a name="registertypelibraries-action"></a><span data-ttu-id="c0fc3-104">Registertypelibraries-Aktion</span><span class="sxs-lookup"><span data-stu-id="c0fc3-104">RegisterTypeLibraries Action</span></span>

<span data-ttu-id="c0fc3-105">Mit der registertypelibraries-Aktion werden Typbibliotheken beim System registriert.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-105">The RegisterTypeLibraries action registers type libraries with the system.</span></span> <span data-ttu-id="c0fc3-106">Diese Aktion wird auf jede Datei angewendet, auf die in der [typelib-Tabelle](typelib-table.md) verwiesen wird, die für die Installation geplant ist.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-106">This action is applied to each file referred to in the [TypeLib table](typelib-table.md) that is scheduled for install.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="c0fc3-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="c0fc3-107">Sequence Restrictions</span></span>

<span data-ttu-id="c0fc3-108">Die Aktion registertypelibraries muss nach der Aktion [InstallFiles](installfiles-action.md) erfolgen.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-108">The RegisterTypeLibraries action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="c0fc3-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="c0fc3-109">ActionData Messages</span></span>



| <span data-ttu-id="c0fc3-110">Feld</span><span class="sxs-lookup"><span data-stu-id="c0fc3-110">Field</span></span> | <span data-ttu-id="c0fc3-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="c0fc3-111">Description of action data</span></span>                   |
|-------|----------------------------------------------|
| <span data-ttu-id="c0fc3-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c0fc3-112">\[1\]</span></span> | <span data-ttu-id="c0fc3-113">[GUID](guid.md) der registrierten Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-113">[GUID](guid.md) of registered type library.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c0fc3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0fc3-114">Remarks</span></span>

<span data-ttu-id="c0fc3-115">Die registertypelibraries-Aktion erfordert, dass die Typbibliotheks Sprache im Language-Feld der TypeLib-Tabelle ordnungsgemäß verfasst wird.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-115">The RegisterTypeLibraries action requires that the type library language be correctly authored in the Language field of the TypeLib table.</span></span> <span data-ttu-id="c0fc3-116">Eine falsche Erstellung des sprach Felds kann bewirken, dass das Installationsprogramm eine ansonsten gültige Typbibliothek nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="c0fc3-116">Incorrect authoring of the Language field can cause the installer to fail to register an otherwise valid type library.</span></span>

 

 



