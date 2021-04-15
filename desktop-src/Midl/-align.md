---
title: /align-Schalter
description: Der/Align-Schalter ist funktional identisch mit der Option "Mittel l/ZP" und wird vom Mittelwert des compl-Compilers nur aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a06be10a4937127d98d508275b57dfe508399
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516335"
---
# <a name="align-switch"></a><span data-ttu-id="c9025-104">/align-Schalter</span><span class="sxs-lookup"><span data-stu-id="c9025-104">/align switch</span></span>

<span data-ttu-id="c9025-105">Der **/align** -Schalter ist funktional identisch mit der Option "Mittel l [**/ZP**](-zp.md) " und wird vom Mittelwert des compl-Compilers nur aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt.</span><span class="sxs-lookup"><span data-stu-id="c9025-105">The **/align** switch is functionally the same as the MIDL [**/Zp**](-zp.md) option and is recognized by the MIDL compiler solely for backward compatibility with MkTypLib.</span></span>

> [!Note]  
> <span data-ttu-id="c9025-106">Das Mktyplib.exe Tool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="c9025-106">The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="c9025-107">Verwenden Sie stattdessen den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="c9025-107">Use the MIDL compiler instead.</span></span>

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a><span data-ttu-id="c9025-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="c9025-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c9025-109">*Richt*</span><span class="sxs-lookup"><span data-stu-id="c9025-109">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="c9025-110">Gibt die Ausrichtung für Typen in der Bibliothek an.</span><span class="sxs-lookup"><span data-stu-id="c9025-110">Specifies the alignment for types in the library.</span></span> <span data-ttu-id="c9025-111">Der *Ausrichtungs* Wert kann 1, 2, 4 oder 8 sein.</span><span class="sxs-lookup"><span data-stu-id="c9025-111">The *alignment* value can be 1, 2, 4, or 8.</span></span> <span data-ttu-id="c9025-112">Der Wert 1 gibt die natürliche Ausrichtung an. *n* gibt die Ausrichtung auf Byte *n* an.</span><span class="sxs-lookup"><span data-stu-id="c9025-112">The value 1 indicates natural alignment; *n* indicates alignment on byte *n*.</span></span> <span data-ttu-id="c9025-113">Wenn Sie den **/align** -Schalter nicht angeben, ist der Standardwert 8.</span><span class="sxs-lookup"><span data-stu-id="c9025-113">When you do not specify the **/align** switch, the default is 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9025-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9025-114">Remarks</span></span>

<span data-ttu-id="c9025-115">Wenn Sie ein neues Makefile-Skript erstellen, verwenden Sie den [**/ZP**](-zp.md) -Schalter.</span><span class="sxs-lookup"><span data-stu-id="c9025-115">If you are generating a new makefile, use the [**/Zp**](-zp.md) switch.</span></span>

<span data-ttu-id="c9025-116">Der Ausrichtungs Wert entspricht dem [**/ZP**](-zp.md) -Optionswert, der vom Microsoft C/C++-Compiler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c9025-116">The alignment value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="c9025-117">Achten Sie darauf, dass Sie die gleiche Ausrichtung angeben, wenn Sie den C-Compiler aufrufen, als wenn Sie den Mittelwert Compiler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9025-117">Be sure that you specify the same alignment when you invoke the C compiler as when you invoke the MIDL compiler.</span></span>

<span data-ttu-id="c9025-118">Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="c9025-118">For more information, see your Microsoft C/C++ programming documentation.</span></span> <span data-ttu-id="c9025-119">Eine Erläuterung der möglichen Gefahren bei der Verwendung nicht standardmäßiger Verpackungs Stufen finden Sie im [**/ZP**](-zp.md) -Hilfethema.</span><span class="sxs-lookup"><span data-stu-id="c9025-119">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="c9025-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9025-120">Examples</span></span>

<span data-ttu-id="c9025-121">**Mittel l/align: 4 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c9025-121">**midl /align:4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c9025-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9025-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9025-123">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c9025-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c9025-124">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="c9025-124">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




