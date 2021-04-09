---
description: Die BindImage-Aktion bindet jede ausführbare Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: BindImage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864439"
---
# <a name="bindimage-action"></a><span data-ttu-id="925ae-103">BindImage-Aktion</span><span class="sxs-lookup"><span data-stu-id="925ae-103">BindImage Action</span></span>

<span data-ttu-id="925ae-104">Die BindImage-Aktion bindet jede ausführbare Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.</span><span class="sxs-lookup"><span data-stu-id="925ae-104">The BindImage action binds each executable or DLL that must be bound to the DLLs imported by it.</span></span> <span data-ttu-id="925ae-105">Die BindImage-Aktion agiert für jede Datei in der [BindImage](bindimage-table.md) -Tabelle, aber nur für die, die lokal installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="925ae-105">The BindImage action acts on each file in the [BindImage](bindimage-table.md) table, but only those that are to be installed locally.</span></span> <span data-ttu-id="925ae-106">Das Installationsprogramm berechnet die virtuelle Adresse jeder aus allen DLLs importierten Funktion und speichert dann die berechnete virtuelle Adresse in der [*Import Adress Tabelle*](i-gly.md) (IAT) des importierten Images.</span><span class="sxs-lookup"><span data-stu-id="925ae-106">The installer computes the virtual address of each function imported from all DLLs, then saves the computed virtual address in the importing image's [*import address table*](i-gly.md) (IAT).</span></span>

<span data-ttu-id="925ae-107">Mit der BindImage-Aktion wird die Windows-API **BindImageEx** intern aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="925ae-107">The BindImage Action internally calls the **BindImageEx** Windows API.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="925ae-108">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="925ae-108">Sequence Restrictions</span></span>

<span data-ttu-id="925ae-109">Die BindImage-Aktion muss nach der Aktion " [InstallFiles](installfiles-action.md) " erfolgen.</span><span class="sxs-lookup"><span data-stu-id="925ae-109">The BindImage action must come after the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="925ae-110">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="925ae-110">ActionData Messages</span></span>



| <span data-ttu-id="925ae-111">Feld</span><span class="sxs-lookup"><span data-stu-id="925ae-111">Field</span></span> | <span data-ttu-id="925ae-112">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="925ae-112">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="925ae-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="925ae-113">\[1\]</span></span> | <span data-ttu-id="925ae-114">Datei Bezeichner der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="925ae-114">File identifier of executable.</span></span> |



 

 

 



