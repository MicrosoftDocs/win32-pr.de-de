---
title: /ZP-Schalter
description: Der/ZP-Schalter ist mit der Option/Pack identisch.
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /ZP-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 553d99dee7dd08218680fc0b43e6e12237c4f8fa
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718161"
---
# <a name="zp-switch"></a><span data-ttu-id="a251f-104">/ZP-Schalter</span><span class="sxs-lookup"><span data-stu-id="a251f-104">/Zp switch</span></span>

<span data-ttu-id="a251f-105">Der **/ZP** -Schalter ist mit der Option [**/Pack**](-pack.md) identisch.</span><span class="sxs-lookup"><span data-stu-id="a251f-105">The **/Zp** switch is the same as the [**/pack**](-pack.md) option.</span></span>

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a><span data-ttu-id="a251f-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="a251f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a251f-107">*Packungs \_ Stufe*</span><span class="sxs-lookup"><span data-stu-id="a251f-107">*packing\_level*</span></span> 
</dt> <dd>

<span data-ttu-id="a251f-108">Gibt die Verpackungs Ebene von Strukturen im Zielsystem an.</span><span class="sxs-lookup"><span data-stu-id="a251f-108">Specifies the packing level of structures in the target system.</span></span> <span data-ttu-id="a251f-109">Der Wert auf der Verpackungs Ebene kann auf 1, 2, 4 oder 8 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a251f-109">The packing-level value can be set to 1, 2, 4, or 8.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a251f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a251f-110">Remarks</span></span>

<span data-ttu-id="a251f-111">Der **/ZP** -Schalter legt die Verpackungs Ebene von Strukturen im Zielsystem fest.</span><span class="sxs-lookup"><span data-stu-id="a251f-111">The **/Zp** switch designates the packing level of structures in the target system.</span></span> <span data-ttu-id="a251f-112">Der Wert auf der Packungs Ebene entspricht dem Wert der **/ZP** -Option, der vom Microsoft C/C++-Compiler verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a251f-112">The packing-level value corresponds to the **/Zp** option value used by the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="a251f-113">Weitere Informationen finden Sie in der Microsoft C/C++-Programmier Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a251f-113">For more information, see your Microsoft C/C++ programming documentation.</span></span>

<span data-ttu-id="a251f-114">Geben Sie die gleiche Packungs Ebene an, wenn Sie den Mittelwert Compiler und den C-Compiler aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a251f-114">Specify the same packing level when you invoke the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="a251f-115">Der standardmäßige Verpackungs Grad, der verwendet wird, wenn weder der Schalter **/ZP** noch [**/Pack**](-pack.md) in allen Buildumgebungen 8 angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a251f-115">The default packing level used when neither the **/Zp** nor [**/pack**](-pack.md) switch is specified is 8 in all build environments.</span></span>

> [!Note]  
> <span data-ttu-id="a251f-116">Verwenden Sie nicht **/Zp1** oder **/Zp2** auf MIPS-oder Alpha-Plattformen, und verwenden Sie **/zp4** oder **/Zp8** nicht auf 16-Bit-Plattformen.</span><span class="sxs-lookup"><span data-stu-id="a251f-116">Do not use **/Zp1** or **/Zp2** on MIPS or Alpha platforms and do not use **/Zp4** or **/Zp8** on 16-bit platforms.</span></span> <span data-ttu-id="a251f-117">Abhängig vom Datentyp und dem Speicherort, die der C-Compiler zur Laufzeit zugewiesen hat, kann dies zu einer Ausnahme bei der Daten Ausrichtungs Änderung auf MIPS-und Alpha-Plattformen führen.</span><span class="sxs-lookup"><span data-stu-id="a251f-117">Depending on the data type and memory location assigned by the C compiler at run time, this can result in a data misalignment exception on MIPS and Alpha platforms.</span></span> <span data-ttu-id="a251f-118">Auf MS-DOS-Plattformen stellt der C-Compiler die Ausrichtung bei 4 oder 8 nicht sicher, sodass die Anwendung beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a251f-118">On MS-DOS platforms, the C compiler will not ensure the alignment at 4 or 8, and so the application may terminate.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a251f-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a251f-119">Examples</span></span>

<span data-ttu-id="a251f-120">**Mittel l/zp4 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="a251f-120">**midl /Zp4 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="a251f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a251f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a251f-122">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="a251f-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="a251f-123">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="a251f-123">**/pack**</span></span>](-pack.md)
</dt> </dl>

 

 




