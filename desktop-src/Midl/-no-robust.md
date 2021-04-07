---
title: /no_robust Schalter
description: Der/No \_ robust-Switch weist den Mittel l-Compiler an, die/robust-Befehlszeilen Funktion explizit zu deaktivieren. Der Befehls Zeilenschalter/robust und die zugehörigen Features sind die standardmäßige Compilereinstellung für die Mittel l-Version 6.0.359 und höher.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718773"
---
# <a name="no_robust-switch"></a><span data-ttu-id="9510e-105">/No \_ robuster Switch</span><span class="sxs-lookup"><span data-stu-id="9510e-105">/no\_robust switch</span></span>

<span data-ttu-id="9510e-106">Der **/No \_ robust** -Switch weist den Mittel l-Compiler an, die [**/robust**](-robust.md) -Befehlszeilen Funktion explizit zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9510e-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="9510e-107">Der Befehls Zeilenschalter **/robust** und die zugehörigen Features sind die standardmäßige Compilereinstellung für die Mittel l-Version 6.0.359 und höher.</span><span class="sxs-lookup"><span data-stu-id="9510e-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="9510e-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="9510e-108">Switch Options</span></span>

<span data-ttu-id="9510e-109">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9510e-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9510e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9510e-110">Remarks</span></span>

<span data-ttu-id="9510e-111">Mit der mittleren l-Version 6.0.359 und höher legt der Mittelwert Compiler standardmäßig [**/robust**](-robust.md) fest.</span><span class="sxs-lookup"><span data-stu-id="9510e-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="9510e-112">Der **/No \_ robust** -Befehls Zeilenschalter muss verwendet werden, um das **/robust** -Feature zu deaktivieren, wenn generierte Stubdateien unter Microsoft Windows NT, Windows-95/98 oder Windows-Windows ausgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9510e-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="9510e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9510e-113">Examples</span></span>

<span data-ttu-id="9510e-114">**Mittel l/No \_ robuster Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="9510e-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="9510e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9510e-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9510e-116">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="9510e-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="9510e-117">**/robust**</span><span class="sxs-lookup"><span data-stu-id="9510e-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




