---
title: /Pack-Schalter
description: Der/Pack-Schalter ist mit der Option/ZP identisch.
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /Pack-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c807846148d81e0e59620046d9f24380fe647c11
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038108"
---
# <a name="pack-switch"></a><span data-ttu-id="18d3c-104">/Pack-Schalter</span><span class="sxs-lookup"><span data-stu-id="18d3c-104">/pack switch</span></span>

<span data-ttu-id="18d3c-105">Der **/Pack** -Schalter ist mit der Option [**/ZP**](-zp.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="18d3c-105">The **/pack** switch is the same as the [**/Zp**](-zp.md) option.</span></span>

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a><span data-ttu-id="18d3c-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="18d3c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="18d3c-107">*Packungs \_ Stufe*</span><span class="sxs-lookup"><span data-stu-id="18d3c-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="18d3c-108">Gibt die Verpackungs Ebene von Strukturen im Zielsystem an.</span><span class="sxs-lookup"><span data-stu-id="18d3c-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="18d3c-109">Der Wert auf der Verpackungs Ebene kann auf 1, 2, 4 oder 8 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="18d3c-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18d3c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18d3c-110">Remarks</span></span>

<span data-ttu-id="18d3c-111">Der **/Pack** -Schalter legt die Verpackungs Ebene von Strukturen im Zielsystem fest.</span><span class="sxs-lookup"><span data-stu-id="18d3c-111">The **/pack** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="18d3c-112">Der Wert auf der Packungs Ebene entspricht dem Wert der [**/ZP**](-zp.md) -Option, der vom Microsoft C/C++-Compiler, Version 7,0, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18d3c-112">The packing-level value corresponds to the [**/Zp**](-zp.md) option value used by the Microsoft C/C++ version 7.0 compiler.</span></span> <span data-ttu-id="18d3c-113">Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="18d3c-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="18d3c-114">Geben Sie die gleiche Packungs Ebene an, wenn Sie den Mittelwert Compiler und den C-Compiler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="18d3c-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span> <span data-ttu-id="18d3c-115">Der standardmäßige Verpackungs Grad, der verwendet wird, wenn weder der [**/ZP**](-zp.md) -noch der **/Pack** -Schalter angegeben ist, in beiden Buildumgebungen 8.</span><span class="sxs-lookup"><span data-stu-id="18d3c-115">The default packing level used when neither the [**/Zp**](-zp.md) nor **/pack** switch is specified is 8, in both all build environments.</span></span>

<span data-ttu-id="18d3c-116">Eine Erläuterung der möglichen Gefahren bei der Verwendung nicht standardmäßiger Verpackungs Stufen finden Sie im [**/ZP**](-zp.md) -Hilfethema.</span><span class="sxs-lookup"><span data-stu-id="18d3c-116">For a discussion of the potential dangers in using nonstandard packing levels, see the [**/Zp**](-zp.md) help topic.</span></span>

## <a name="examples"></a><span data-ttu-id="18d3c-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18d3c-117">Examples</span></span>

<span data-ttu-id="18d3c-118">**Mittel l/Pack 2 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="18d3c-118">**midl /pack 2 filename.idl**</span></span>

<span data-ttu-id="18d3c-119">**Mittel l/Pack 8. idl**</span><span class="sxs-lookup"><span data-stu-id="18d3c-119">**midl /pack 8 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="18d3c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18d3c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d3c-121">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="18d3c-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="18d3c-122">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="18d3c-122">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="18d3c-123">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="18d3c-123">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




