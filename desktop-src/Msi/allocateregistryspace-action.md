---
description: Mit der Aktion "Zuweisung zuweisen" wird sichergestellt, dass der von der Eigenschaft availablefreereg angegebene freie Registrierungs Speicherplatz in der Registrierung vorhanden ist.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Zuordnung von "depjeeregistryspace"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348345"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="cf663-103">Zuordnung von "depjeeregistryspace"</span><span class="sxs-lookup"><span data-stu-id="cf663-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="cf663-104">Mit der Aktion "Zuweisung zuweisen" wird sichergestellt, dass der von der Eigenschaft [**availablefreereg**](availablefreereg.md) angegebene freie Registrierungs Speicherplatz in der Registrierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cf663-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cf663-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="cf663-105">Sequence Restrictions</span></span>

<span data-ttu-id="cf663-106">Die Aktion "zustelleregistryspace" muss nach " [InstallInitialize](installinitialize-action.md)" aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cf663-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="cf663-107">Es empfiehlt sich, den zustellereregistryspace vor allen anderen Aktionen zu planen, um sicherzustellen, dass ausreichend Registrierungs Speicher verfügbar ist, um den Vorgang fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="cf663-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cf663-108">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="cf663-108">ActionData Messages</span></span>



| <span data-ttu-id="cf663-109">Feld</span><span class="sxs-lookup"><span data-stu-id="cf663-109">Field</span></span> | <span data-ttu-id="cf663-110">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="cf663-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="cf663-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cf663-111">\[1\]</span></span> | <span data-ttu-id="cf663-112">Benötigtes Registrierungs Speicher in KB.</span><span class="sxs-lookup"><span data-stu-id="cf663-112">Registry space required in KB.</span></span> |



 

 

 



