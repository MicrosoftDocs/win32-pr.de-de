---
title: Flusssteuerung
description: Die meisten Hardwarekomponenten sind dafür ausgelegt, den Shader-Codezeilen Weise auszuführen und jede HLSL-Anweisung einmal auszuführen.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309668"
---
# <a name="flow-control"></a><span data-ttu-id="301fa-103">Flusssteuerung</span><span class="sxs-lookup"><span data-stu-id="301fa-103">Flow Control</span></span>

<span data-ttu-id="301fa-104">Die meisten Hardwarekomponenten sind dafür ausgelegt, den Shader-Codezeilen Weise auszuführen und jede HLSL-Anweisung einmal auszuführen.</span><span class="sxs-lookup"><span data-stu-id="301fa-104">Most hardware is designed to run shader code line by line, executing each HLSL statement once.</span></span> <span data-ttu-id="301fa-105">Eine Fluss Steuerungs Anweisung bestimmt zur Laufzeit den Block der HLSL-Anweisungen, der als nächstes ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="301fa-105">A flow-control statement determines at run time which block of HLSL statements to execute next.</span></span> <span data-ttu-id="301fa-106">Mithilfe einer Flow-Control-Anweisung kann ein Shader eine Reihe von Anweisungen durchlaufen oder eine Schleife (Verzweigung) in eine andere Anweisung als die in der nächsten Zeile springen.</span><span class="sxs-lookup"><span data-stu-id="301fa-106">Using a flow-control statement, a shader can loop through a set of statements, or jump (branch) to an instruction other than the one on the next line.</span></span> <span data-ttu-id="301fa-107">Einige Fluss Steuerungs Anweisungen unterstützen ein statisches Steuerelement, das zum Zeitpunkt der Kompilierung angegeben wird. andere bieten eine Prädikat Kontrolle, bei der es sich um eine pro-Komponente-Entscheidung zur Laufzeit handelt, und andere unterstützen die dynamische Steuerung, die zur Laufzeit basierend auf dem Inhalt einer Variablen getroffen wird.</span><span class="sxs-lookup"><span data-stu-id="301fa-107">Some flow-control statements support static control that is specified at compile time; others offer predicated control which is a per-component decision made at runtime, and still others support dynamic control which is a decision made at run time based on the contents of a variable.</span></span>

<span data-ttu-id="301fa-108">HLSL unterstützt die folgenden Anweisungen für die Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="301fa-108">HLSL supports the following flow-control statements.</span></span>

-   [<span data-ttu-id="301fa-109">break</span><span class="sxs-lookup"><span data-stu-id="301fa-109">break</span></span>](dx-graphics-hlsl-break.md)
-   [<span data-ttu-id="301fa-110">continue</span><span class="sxs-lookup"><span data-stu-id="301fa-110">continue</span></span>](dx-graphics-hlsl-continue.md)
-   [<span data-ttu-id="301fa-111">Würfen</span><span class="sxs-lookup"><span data-stu-id="301fa-111">discard</span></span>](dx-graphics-hlsl-discard.md)
-   [<span data-ttu-id="301fa-112">do</span><span class="sxs-lookup"><span data-stu-id="301fa-112">do</span></span>](dx-graphics-hlsl-do.md)
-   [<span data-ttu-id="301fa-113">for</span><span class="sxs-lookup"><span data-stu-id="301fa-113">for</span></span>](dx-graphics-hlsl-for.md)
-   [<span data-ttu-id="301fa-114">if</span><span class="sxs-lookup"><span data-stu-id="301fa-114">if</span></span>](dx-graphics-hlsl-if.md)
-   [<span data-ttu-id="301fa-115">switch</span><span class="sxs-lookup"><span data-stu-id="301fa-115">switch</span></span>](dx-graphics-hlsl-switch.md)
-   [<span data-ttu-id="301fa-116">while</span><span class="sxs-lookup"><span data-stu-id="301fa-116">while</span></span>](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a><span data-ttu-id="301fa-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="301fa-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="301fa-118">Sprach Syntax (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="301fa-118">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




