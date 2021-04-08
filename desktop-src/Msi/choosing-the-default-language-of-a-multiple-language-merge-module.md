---
description: Die Standardsprache für ein Mergemodul ist die Sprache, die in der Tabelle ModuleSignature des Moduls aufgeführt ist, bevor sprach Transformationen angewendet werden. Dies ist auch die erste Sprache, die in der Template-Übersichts Eigenschaft aufgeführt ist.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864416"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="77dc7-104">Auswählen der Standardsprache eines Mergemoduls mit mehreren Sprachen</span><span class="sxs-lookup"><span data-stu-id="77dc7-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="77dc7-105">Die Standardsprache für ein Mergemodul ist die Sprache, die in der [Tabelle ModuleSignature](modulesignature-table.md) des Moduls aufgeführt ist, bevor sprach Transformationen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="77dc7-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="77dc7-106">Dies ist auch die erste Sprache, die in der [**Template-Übersichts**](template-summary.md) Eigenschaft aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="77dc7-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="77dc7-107">Die Standardsprache für das Modul sollte eine der spezifischsten Sprachen sein, die Sie unterstützen, da die Standardsprache immer zuerst geprüft wird, und wenn Sie der angeforderten Sprache entspricht, wird Sie auch dann verwendet, wenn eine andere Sprache eine bessere Übereinstimmung ist.</span><span class="sxs-lookup"><span data-stu-id="77dc7-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="77dc7-108">Wenn ein Modul z. b. 1033 und 0 unterstützt, sollte 1033 die Standardsprache sein.</span><span class="sxs-lookup"><span data-stu-id="77dc7-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="77dc7-109">Wenn 0 die Standardsprache wäre, würde Sie immer jede Anforderung erfüllen, und die 1033-Transformation würde nie verwendet werden, auch wenn 1033 die exakt angeforderte Sprache ist.</span><span class="sxs-lookup"><span data-stu-id="77dc7-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



