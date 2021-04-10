---
title: /mktyplib203-Schalter
description: Der/mktyplib203-Schalter zwingt den Mittel l-Compiler, die Eingabedatei zu analysieren.
ms.assetid: e1eddf03-db42-426e-bdf1-b7122b862756
keywords:
- /mktyplib203-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /mktyplib203
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8fd972355c2f6d37300c60f4bf74e76bf4396
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857551"
---
# <a name="mktyplib203-switch"></a><span data-ttu-id="b7083-104">/mktyplib203-Schalter</span><span class="sxs-lookup"><span data-stu-id="b7083-104">/mktyplib203 switch</span></span>

<span data-ttu-id="b7083-105">Der **/mktyplib203** -Schalter zwingt den Mittel l-Compiler, die Eingabedatei zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="b7083-105">The **/mktyplib203** switch forces the MIDL compiler to parse the input file.</span></span>

``` syntax
midl /mktyplib203
```

## <a name="switch-options"></a><span data-ttu-id="b7083-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="b7083-106">Switch Options</span></span>

<span data-ttu-id="b7083-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7083-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7083-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7083-108">Remarks</span></span>

<span data-ttu-id="b7083-109">Um den **/mktyplib203** -Schalter verwenden zu können, muss die Eingabedatei genau der ODL-Syntax folgen. Dies bedeutet, dass Sie keine Anweisungen außerhalb des Bibliotheks Blocks platzieren können.</span><span class="sxs-lookup"><span data-stu-id="b7083-109">In order to use the **/mktyplib203** switch, the input file must follow the ODL syntax exactly, which means you cannot place any statements outside of the library block.</span></span> <span data-ttu-id="b7083-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7083-110">Examples</span></span>

<span data-ttu-id="b7083-111">**Mittel l/mktyplib203 myoldodl. ODL**</span><span class="sxs-lookup"><span data-stu-id="b7083-111">**midl /mktyplib203 myoldodl.odl**</span></span>

<span data-ttu-id="b7083-112">**Mittel l/mktyplib203 oldhabit. idl**</span><span class="sxs-lookup"><span data-stu-id="b7083-112">**midl /mktyplib203 oldhabit.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="b7083-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7083-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7083-114">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="b7083-114">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="b7083-115">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="b7083-115">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 




