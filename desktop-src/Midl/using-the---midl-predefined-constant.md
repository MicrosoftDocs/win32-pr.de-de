---
title: Verwenden der __midl vordefinierten Konstante
description: Wenn der Mittell-Compiler die Eingabe-IDL-und ACF-Dateien verarbeitet, \_ \_ wird die mittlere-Version standardmäßig definiert und zur bedingten Kompilierung verwendet, um die Konsistenz im gesamten Build zu erzielen.
ms.assetid: ba9557f8-d398-4c87-993d-f4e545894cdd
keywords:
- Mittlerer l-compilermittell, Verwendung der _midl vordefinierten Konstante
- _midl der vordefinierten Konstanten-Mittel l
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae49675b38dcc3cab2d3d41e4f48cd0637d78523
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037039"
---
# <a name="using-the-__midl-predefined-constant"></a><span data-ttu-id="210e6-105">Verwenden der \_ \_ vordefinierten-Konstante (Mitte)</span><span class="sxs-lookup"><span data-stu-id="210e6-105">Using the \_\_midl Predefined Constant</span></span>

<span data-ttu-id="210e6-106">Wenn der Mittell-Compiler die Eingabe-IDL-und ACF-Dateien verarbeitet, \_ \_ wird die mittlere-Version standardmäßig definiert und zur bedingten Kompilierung verwendet, um die Konsistenz im gesamten Build zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="210e6-106">When the MIDL compiler processes the input IDL and ACF files, \_\_midl is defined by default and is used for conditional compilation to attain consistency throughout the build.</span></span> <span data-ttu-id="210e6-107">Dadurch wird die Verwendung von define-Anweisungen in den Header Dateien, wie z. b. " **Mittel l \_ Pass**", ausgeblendet und durch ein konsistentes Flag ersetzt.</span><span class="sxs-lookup"><span data-stu-id="210e6-107">This phases out the use of define statements in the header files, such as **MIDL\_PASS**, and replaces them with a consistent flag.</span></span> <span data-ttu-id="210e6-108">Der Wert der \_ \_ mittleren l-Konstante gibt die Compilerversion *Major. Minor* gemäß der Formel *Major* \* 100 + *Minor* an, z. b. mittlerer l-ver.</span><span class="sxs-lookup"><span data-stu-id="210e6-108">The value of the \_\_midl constant indicates the compiler version *major.minor* according to the formula *major* \* 100 + *minor*; for example MIDL ver.</span></span> <span data-ttu-id="210e6-109">bei 6.0. x ist die \_ \_ Mittel-l als 600 definiert.</span><span class="sxs-lookup"><span data-stu-id="210e6-109">6.0.x has the \_\_midl defined as 600.</span></span>

<span data-ttu-id="210e6-110">Wenn Sie sich entscheiden, können Sie diese Standardeinstellung überschreiben, indem Sie Folgendes in der Befehlszeile angeben: **/U- \_ \_ Mittell**.</span><span class="sxs-lookup"><span data-stu-id="210e6-110">If you choose, you can override this default by specifying the following on the command line: **/U\_\_midl**.</span></span> <span data-ttu-id="210e6-111">Weitere Informationen finden Sie unter [**/U**](-u.md).</span><span class="sxs-lookup"><span data-stu-id="210e6-111">For more information, see [**/U**](-u.md).</span></span>

 

 




