---
title: /ENV-Schalter
description: Der Schalter/env wählt die Umgebung aus, in der die Anwendung ausgeführt wird.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390185"
---
# <a name="env-switch"></a><span data-ttu-id="21c8e-104">/ENV-Schalter</span><span class="sxs-lookup"><span data-stu-id="21c8e-104">/env switch</span></span>

<span data-ttu-id="21c8e-105">Der Schalter **/env** wählt die Umgebung aus, in der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21c8e-105">The **/env** switch selects the environment in which the application runs.</span></span>

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a><span data-ttu-id="21c8e-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="21c8e-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span data-ttu-id="21c8e-107"><span id="win32"></span><span id="WIN32"></span>Win32 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="21c8e-107"><span id="win32"></span><span id="WIN32"></span>\*\*\*\*win32\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="21c8e-108">Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 32-Bit-Umgebung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="21c8e-108">Directs the MIDL compiler to generate stub files, or a type library file, for a 32-bit environment.</span></span>

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span data-ttu-id="21c8e-109"><span id="ia64"></span><span id="IA64"></span>ia64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="21c8e-109"><span id="ia64"></span><span id="IA64"></span>\*\*\*\*ia64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="21c8e-110">Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine Intel Architecture 64-Bit (ia64)-Umgebung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="21c8e-110">Directs the MIDL compiler to generate stub files, or a type library file, for a Intel Architecture 64-bit (IA64) environment.</span></span>

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span data-ttu-id="21c8e-111"><span id="amd64"></span><span id="AMD64"></span>amd64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="21c8e-111"><span id="amd64"></span><span id="AMD64"></span>\*\*\*\*amd64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="21c8e-112">Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine Advanced Micro Devices 64-Bit-Umgebung (amd64) zu generieren.</span><span class="sxs-lookup"><span data-stu-id="21c8e-112">Directs the MIDL compiler to generate stub files, or a type library file, for an Advanced Micro Devices 64-bit (AMD64) environment.</span></span>

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span data-ttu-id="21c8e-113"><span id="win64"></span><span id="WIN64"></span>Win64 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="21c8e-113"><span id="win64"></span><span id="WIN64"></span>\*\*\*\*win64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="21c8e-114">Gleiches Verhalten wie *ia64*.</span><span class="sxs-lookup"><span data-stu-id="21c8e-114">Same behavior as *ia64*.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21c8e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21c8e-115">Remarks</span></span>

<span data-ttu-id="21c8e-116">Der **/env** -Switch wirkt sich hauptsächlich auf die Verpackungs Ebene aus, die für Strukturen in dieser Umgebung verwendet wird</span><span class="sxs-lookup"><span data-stu-id="21c8e-116">The **/env** switch primarily affects the packing level used for structures in that environment.</span></span> <span data-ttu-id="21c8e-117">Stellen Sie sicher, dass Sie dieselbe Einstellung auf Verpackungs Ebene sowohl für den Mittelwert Compiler als auch für den C-Compiler angeben.</span><span class="sxs-lookup"><span data-stu-id="21c8e-117">Be sure you specify the same packing-level setting for both the MIDL compiler and the C compiler.</span></span>

<span data-ttu-id="21c8e-118">Der Schalter **/env** bestimmt die Verpackungs Ebene und andere Einstellungen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="21c8e-118">The **/env** switch determines the packing level and other settings as follows:</span></span>

-   <span data-ttu-id="21c8e-119">Wenn Sie **Win32** angeben, verwenden generierte Stub für alle Typen, die an Remote Vorgängen beteiligt sind, C-Compiler Packaging-Level 8.</span><span class="sxs-lookup"><span data-stu-id="21c8e-119">When you specify **win32**, generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="21c8e-120">Die [**int**](int.md) -Datentypen sind 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="21c8e-120">The [**int**](int.md) data types are both 32 bits.</span></span> <span data-ttu-id="21c8e-121">Zeiger sind 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="21c8e-121">Pointers are 32 bits.</span></span>
-   <span data-ttu-id="21c8e-122">Wenn Sie **ia64** oder **amd64** angeben, wird der mittlerer l-Compiler in einem Kreuz Compilermodus für die angegebene (Intel oder AMD) 64-Bit-Plattform ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21c8e-122">When you specify **ia64** or **amd64**, the MIDL compiler runs in a cross-compiler mode for the indicated (Intel or AMD) 64-bit platform.</span></span> <span data-ttu-id="21c8e-123">Die generierten Stub verwenden C-Compiler-Komprimierungs Ebene 8 für alle Typen, die an Remote Vorgängen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="21c8e-123">The generated stubs use C-compiler packing-level 8 for all types involved in remote operations.</span></span> <span data-ttu-id="21c8e-124">Die [**Long**](long.md) -und [**int**](int.md) -Datentypen sind 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="21c8e-124">The [**long**](long.md) and [**int**](int.md) data types are 32 bits.</span></span> <span data-ttu-id="21c8e-125">Zeiger sind 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="21c8e-125">Pointers are 64 bits.</span></span>

<span data-ttu-id="21c8e-126">Die Schalter [**/align**](-align.md), [**/Pack**](-pack.md)und [**/ZP**](-zp.md) haben Vorrang vor den **/env** -Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="21c8e-126">The [**/align**](-align.md), [**/pack**](-pack.md), and [**/Zp**](-zp.md) switches take precedence over the **/env** settings.</span></span>

<span data-ttu-id="21c8e-127">Weitere Informationen zur 64-Bit-Unterstützung für die mittlere und RPC finden Sie unter [Entwerfen von 64-Bit-kompatiblen Schnittstellen](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span><span class="sxs-lookup"><span data-stu-id="21c8e-127">For more information on 64 bit support for MIDL and RPC see [Designing 64-bit-Compatible Interfaces](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).</span></span>

## <a name="examples"></a><span data-ttu-id="21c8e-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21c8e-128">Examples</span></span>

<span data-ttu-id="21c8e-129">**Mittel l/env Win32 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="21c8e-129">**midl /env win32 filename.idl**</span></span>

<span data-ttu-id="21c8e-130">**Mittel l/env ia64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="21c8e-130">**midl /env ia64 filename.idl**</span></span>

<span data-ttu-id="21c8e-131">**Mittel l/env amd64 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="21c8e-131">**midl /env amd64 filename.idl**</span></span>

<span data-ttu-id="21c8e-132">**Mittel l/env Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="21c8e-132">**midl /env win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="21c8e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21c8e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c8e-134">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="21c8e-134">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="21c8e-135">**/Pack**</span><span class="sxs-lookup"><span data-stu-id="21c8e-135">**/pack**</span></span>](-pack.md)
</dt> <dt>

[<span data-ttu-id="21c8e-136">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="21c8e-136">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 