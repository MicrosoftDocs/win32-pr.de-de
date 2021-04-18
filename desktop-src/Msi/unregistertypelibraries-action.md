---
description: Die unregistertypelibraries-Aktion hebt die Registrierung von Typbibliotheken im System auf. Diese Aktion wird auf jede Datei angewendet, die in der TypeLib-Tabelle aufgelistet ist, die für die Deinstallation ausgelöst wird.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Unregistertypelibraries-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352386"
---
# <a name="unregistertypelibraries-action"></a><span data-ttu-id="76e52-104">Unregistertypelibraries-Aktion</span><span class="sxs-lookup"><span data-stu-id="76e52-104">UnregisterTypeLibraries Action</span></span>

<span data-ttu-id="76e52-105">Die unregistertypelibraries-Aktion hebt die Registrierung von Typbibliotheken im System auf.</span><span class="sxs-lookup"><span data-stu-id="76e52-105">The UnregisterTypeLibraries action unregisters type libraries from the system.</span></span> <span data-ttu-id="76e52-106">Diese Aktion wird auf jede Datei angewendet, die in der [typelib](typelib-table.md) -Tabelle aufgelistet ist, die für die Deinstallation ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="76e52-106">This action is applied to each file listed in the [TypeLib](typelib-table.md) table that is triggered to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="76e52-107">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="76e52-107">Sequence Restrictions</span></span>

<span data-ttu-id="76e52-108">Die unregistertypelibraries-Aktion muss vor der [RemoveFiles](removefiles-action.md) -Aktion erfolgen.</span><span class="sxs-lookup"><span data-stu-id="76e52-108">The UnregisterTypeLibraries action must come before the [RemoveFiles](removefiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="76e52-109">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="76e52-109">ActionData Messages</span></span>



| <span data-ttu-id="76e52-110">Feld</span><span class="sxs-lookup"><span data-stu-id="76e52-110">Field</span></span> | <span data-ttu-id="76e52-111">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="76e52-111">Description of action data</span></span>                        |
|-------|---------------------------------------------------|
| <span data-ttu-id="76e52-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="76e52-112">\[1\]</span></span> | <span data-ttu-id="76e52-113">[GUID](guid.md) einer nicht registrierten Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="76e52-113">[GUID](guid.md) of an unregistered type library.</span></span> |



 

 

 



