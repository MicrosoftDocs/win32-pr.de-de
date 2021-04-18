---
title: Große ganze Zahlen
description: Die großen ganzzahligen Funktionen und Strukturen haben ursprünglich 64-Bit-Werte auf 32-Bit-Fenstern unterstützt.
ms.assetid: db4ffbd5-d9e4-4c95-83cc-6f0691c080d2
keywords:
- große ganze Zahlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ab6276ff6879ce5b72f198e3ccbd247f456e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339086"
---
# <a name="large-integers"></a><span data-ttu-id="6683f-104">Große ganze Zahlen</span><span class="sxs-lookup"><span data-stu-id="6683f-104">Large Integers</span></span>

<span data-ttu-id="6683f-105">Die großen ganzzahligen Funktionen und Strukturen haben ursprünglich 64-Bit-Werte auf 32-Bit-Fenstern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6683f-105">The large integer functions and structures originally provided support for 64-bit values on 32-bit Windows.</span></span> <span data-ttu-id="6683f-106">Nun unterstützt der C-Compiler möglicherweise ganzzahlige 64-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="6683f-106">Now, your C compiler may support 64-bit integers natively.</span></span> <span data-ttu-id="6683f-107">Beispielsweise unterstützt Microsoft Visual C++ den ganzzahligen Typ [**\_ \_ Int64**](/windows/desktop/Midl/--int64) .</span><span class="sxs-lookup"><span data-stu-id="6683f-107">For example, Microsoft Visual C++ supports the [**\_\_int64**](/windows/desktop/Midl/--int64) sized integer type.</span></span> <span data-ttu-id="6683f-108">Weitere Informationen finden Sie in der Dokumentation, die in Ihrem C-Compiler enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6683f-108">For more information, see the documentation included with your C compiler.</span></span>

<span data-ttu-id="6683f-109">Informationen zu ganzzahligen 64-Bit-Zahlen auf 64-Bit-Fenstern finden Sie [unter den neuen Datentypen](/windows/desktop/WinProg64/the-new-data-types).</span><span class="sxs-lookup"><span data-stu-id="6683f-109">For information on 64-bit integers on 64-bit Windows, see [The New Data Types](/windows/desktop/WinProg64/the-new-data-types).</span></span>

## <a name="large-integer-operations"></a><span data-ttu-id="6683f-110">Große ganzzahlige Vorgänge</span><span class="sxs-lookup"><span data-stu-id="6683f-110">Large Integer Operations</span></span>

<span data-ttu-id="6683f-111">Anwendungen können mit der [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) -Funktion und der [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) -Funktion eine 64 ganze Zahl mit oder 32 ohne Vorzeichen oder ganze Zahlen mit Vorzeichen oder ohne Vorzeichen multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="6683f-111">Applications can multiply signed or unsigned 32-bit integers, generating 64-bit results, by using the [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64) and [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64) functions.</span></span> <span data-ttu-id="6683f-112">Anwendungen können Bits in 64-Bit-Werten mithilfe der Funktionen [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)und [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) nach links oder rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="6683f-112">Applications can shift bits in 64-bit values to the left or right by using the [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32), [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32), and [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32) functions.</span></span> <span data-ttu-id="6683f-113">Diese Funktionen bieten logische und arithmetische Verschiebungen.</span><span class="sxs-lookup"><span data-stu-id="6683f-113">These functions provide logical and arithmetic shifting.</span></span>

<span data-ttu-id="6683f-114">Anwendungen können auch 32-Bit-Werte in einem einzelnen Vorgang multiplizieren und teilen, indem Sie die [**muldiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="6683f-114">Applications can also multiply and divide 32-bit values in a single operation by using the [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv) function.</span></span> <span data-ttu-id="6683f-115">Obwohl das Ergebnis des Vorgangs ein 32-Bit-Wert ist, speichert die Funktion das Zwischenergebnis als 64-Bit-Wert, sodass die Informationen nicht verloren gehen, wenn große 32-Bit-Werte multipliziert und dividiert werden.</span><span class="sxs-lookup"><span data-stu-id="6683f-115">Although the result of the operation is a 32-bit value, the function stores the intermediate result as a 64-bit value, so that information is not lost when large 32-bit values are multiplied and divided.</span></span>

## <a name="large-integer-reference"></a><span data-ttu-id="6683f-116">Verweis auf große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="6683f-116">Large Integer Reference</span></span>

-   [<span data-ttu-id="6683f-117">Große ganzzahlige Funktionen</span><span class="sxs-lookup"><span data-stu-id="6683f-117">Large Integer Functions</span></span>](large-integer-functions.md)
-   [<span data-ttu-id="6683f-118">Large Integer-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6683f-118">Large Integer Structures</span></span>](large-integer-structures.md)

 

 