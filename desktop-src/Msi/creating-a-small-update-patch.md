---
description: Befolgen Sie die folgenden Richtlinien, wenn Sie einen Patch für ein Windows Installer kleines Update erstellen.
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: Erstellen eines kleinen Update-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359544"
---
# <a name="creating-a-small-update-patch"></a><span data-ttu-id="efdbf-103">Erstellen eines kleinen Update-Patches</span><span class="sxs-lookup"><span data-stu-id="efdbf-103">Creating a Small Update Patch</span></span>

<span data-ttu-id="efdbf-104">Beim Erstellen eines Patches für [kleine Updates](small-updates.md)sollten Autoren die folgenden Richtlinien befolgen:</span><span class="sxs-lookup"><span data-stu-id="efdbf-104">When creating a patch for [small updates](small-updates.md), authors should adhere to the following guidelines:</span></span>

-   <span data-ttu-id="efdbf-105">Kleine Updatepatches müssen für eine einzelne Ziel Installation entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="efdbf-105">Small update patches must be designed for a single, target installation.</span></span>
-   <span data-ttu-id="efdbf-106">Für kleine Updatepatches sollte die früheste Version als Ziel Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efdbf-106">Small update patches should use the earliest version as the target installation.</span></span>
-   <span data-ttu-id="efdbf-107">Ein kleiner Update Patch sollte alle früheren kleinen Updatepatches ersetzen und veraltete Dateien als veraltet festlegen.</span><span class="sxs-lookup"><span data-stu-id="efdbf-107">A small update patch should replace and make obsolete any earlier small update patches.</span></span>

<span data-ttu-id="efdbf-108">Im folgenden Szenario wird veranschaulicht, wann ein kleines Update Patch am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="efdbf-108">The following scenario illustrates when a small update patch is best.</span></span>

<span data-ttu-id="efdbf-109">Ihr Unternehmen wird in Version 1,0 von Myproduct.msi ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="efdbf-109">Your company ships version 1.0 of Myproduct.msi.</span></span> <span data-ttu-id="efdbf-110">Kurz danach liefern Sie einen [kleinen Update](small-updates.md) Patch für Myproduct.msi mit dem Namen QFE1.</span><span class="sxs-lookup"><span data-stu-id="efdbf-110">Shortly thereafter, you ship a [small update](small-updates.md) patch for Myproduct.msi called QFE1.</span></span> <span data-ttu-id="efdbf-111">Dadurch wird die [**ProductCode**](productcode.md) -Eigenschaft oder die [**ProductVersion**](productversion.md) -Eigenschaft nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="efdbf-111">This does not change the [**ProductCode**](productcode.md) property or the [**ProductVersion**](productversion.md) property.</span></span>

<span data-ttu-id="efdbf-112">Später erstellen Sie einen zweiten [kleinen Update](small-updates.md) Patch für Myproduct.msi mit dem Namen QFE2.</span><span class="sxs-lookup"><span data-stu-id="efdbf-112">Later, you author a second [small update](small-updates.md) patch for Myproduct.msi called QFE2.</span></span> <span data-ttu-id="efdbf-113">Dieser zweite Patch muss auf Myproduct.msi Version 1,0 ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="efdbf-113">This second patch must target Myproduct.msi version 1.0.</span></span> <span data-ttu-id="efdbf-114">Dieser zweite Patch darf nicht sowohl Myproduct.msi Version 1,0 als auch Myproduct.msi Version 1,0 + QFE1 als Ziel haben.</span><span class="sxs-lookup"><span data-stu-id="efdbf-114">This second patch must not target both Myproduct.msi version 1.0 and Myproduct.msi version 1.0 + QFE1.</span></span> <span data-ttu-id="efdbf-115">Wenn QFE2 angewendet wird, sollte QFE1 entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="efdbf-115">When QFE2 is applied it should remove QFE1.</span></span>

 

 



