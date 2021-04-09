---
description: Autoren sollten die Validierung für jedes neue oder neu geänderte Mergemodul ausführen, bevor Sie versuchen, das Modul zum ersten Mal in eine Installations Datenbank zu mergen.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validieren von Mergemodulen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8bbe7f1c1ea32baa39cadd7c729f3a8ca3ac17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129941"
---
# <a name="validating-merge-modules"></a><span data-ttu-id="a59e1-103">Validieren von Mergemodulen</span><span class="sxs-lookup"><span data-stu-id="a59e1-103">Validating Merge Modules</span></span>

<span data-ttu-id="a59e1-104">Autoren sollten die Validierung für jedes neue oder neu geänderte Mergemodul ausführen, bevor Sie versuchen, das Modul zum ersten Mal in eine Installations Datenbank zu mergen.</span><span class="sxs-lookup"><span data-stu-id="a59e1-104">Authors should run validation on every new, or newly modified, merge module before attempting to merge the module into an installation database for the first time.</span></span> <span data-ttu-id="a59e1-105">Die mergemodulvalidierung funktioniert auf dieselbe Weise wie die [Paket](package-validation.md) Überprüfung, verwendet jedoch einen anderen Satz [interner Konsistenz](internal-consistency-evaluators-ices.md) Auswertungen (ICES), die für Mergemodule spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="a59e1-105">Merge module validation works in the same way as [package validation](package-validation.md) but uses a different set of [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) (ICEs) specific to merge modules.</span></span> <span data-ttu-id="a59e1-106">Weitere Informationen zu diesen Merge-Modul-ICES finden Sie unter [Merge Module Ice Reference](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a59e1-106">For more information about these merge module ICEs, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

<span data-ttu-id="a59e1-107">Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" (Mergemod. CUB) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a59e1-107">Merge module ICEs are stored in the merge module .cub file, Mergemod.cub.</span></span> <span data-ttu-id="a59e1-108">Bei der Installation des Orca-Tools oder msival2 werden auch die Dateien "Logo. Cub", "Darice. Cub" und "Mergemod. Cub" bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a59e1-108">The installation of the Orca tool or msival2 also provides the Logo.cub, Darice.cub, and Mergemod.cub files.</span></span>

<span data-ttu-id="a59e1-109">Weitere Informationen finden Sie unter [Merge Module Ice Reference](merge-module-ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a59e1-109">For more information, see [Merge Module ICE Reference](merge-module-ice-reference.md).</span></span>

 

 



