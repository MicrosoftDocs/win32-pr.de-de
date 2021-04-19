---
title: Weitere Überlegungen
description: Beachten Sie beim Portieren Ihres Codes die folgenden Punkte.
ms.assetid: 2d649a09-b593-477a-9b4f-d2404784f4b0
keywords:
- Portieren von Tipps 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7607685f4b4ba04b86da276c38090a48ce0fead
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "106350740"
---
# <a name="additional-considerations"></a><span data-ttu-id="ab40c-104">Weitere Überlegungen</span><span class="sxs-lookup"><span data-stu-id="ab40c-104">Additional Considerations</span></span>

<span data-ttu-id="ab40c-105">Beachten Sie beim Portieren Ihres Codes die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="ab40c-105">When porting your code, consider the following points:</span></span>

- <span data-ttu-id="ab40c-106">Die folgende Annahme ist nicht mehr gültig:</span><span class="sxs-lookup"><span data-stu-id="ab40c-106">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN32 // Win32 code
      ...
   #else         // Win16 code
      ...
   #endif
   ```

   <span data-ttu-id="ab40c-107">Der 64-Bit-Compiler definiert \_ Win32 jedoch aus Gründen der Abwärtskompatibilität.</span><span class="sxs-lookup"><span data-stu-id="ab40c-107">However, the 64-bit compiler defines \_WIN32 for backward compatibility.</span></span>

- <span data-ttu-id="ab40c-108">Die folgende Annahme ist nicht mehr gültig:</span><span class="sxs-lookup"><span data-stu-id="ab40c-108">The following assumption is no longer valid:</span></span>

   ```syntax
   #ifdef _WIN16 // Win16 code
      ...
   #else         // Win32 code
      ...
   #endif
   ```

   <span data-ttu-id="ab40c-109">In diesem Fall kann die Else-Klausel \_ Win32 oder \_ Win64 darstellen.</span><span class="sxs-lookup"><span data-stu-id="ab40c-109">In this case, the else clause can represent \_WIN32 or \_WIN64.</span></span>

- <span data-ttu-id="ab40c-110">Achten Sie auf die Ausrichtung des Datentyps.</span><span class="sxs-lookup"><span data-stu-id="ab40c-110">Be careful with data-type alignment.</span></span> <span data-ttu-id="ab40c-111">Das **\_ typausrichtungs** Makro gibt die Ausrichtungs Anforderungen eines Datentyps zurück.</span><span class="sxs-lookup"><span data-stu-id="ab40c-111">The **TYPE\_ALIGNMENT** macro returns the alignment requirements of a data type.</span></span> <span data-ttu-id="ab40c-112">Beispiel: `TYPE_ALIGNMENT( KFLOATING_SAVE )` = = 4 auf x86, 8 auf dem Intel Itanium-Prozessor `TYPE_ALIGNMENT( UCHAR )` = = 1 Everywhere</span><span class="sxs-lookup"><span data-stu-id="ab40c-112">For example: `TYPE_ALIGNMENT( KFLOATING_SAVE )` == 4 on x86, 8 on Intel Itanium processor`TYPE_ALIGNMENT( UCHAR )` == 1 everywhere</span></span>

    <span data-ttu-id="ab40c-113">Beispiel: Kernel Code, der derzeit wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="ab40c-113">As an example, kernel code that currently looks like this:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, sizeof(ULONG) );
    ```

    <span data-ttu-id="ab40c-114">sollte wahrscheinlich in geändert werden:</span><span class="sxs-lookup"><span data-stu-id="ab40c-114">should probably be changed to:</span></span>

    ```syntax
    ProbeForRead( UserBuffer, UserBufferLength, TYPE_ALIGNMENT(IOCTL_STRUC) );
    ```

    <span data-ttu-id="ab40c-115">Automatische Korrekturen der kernelmodusausrichtungs-Ausnahmen sind für Intel Itanium-Systeme deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab40c-115">Automatic fixes of kernel-mode alignment exceptions are disabled for Intel Itanium systems.</span></span>

- <span data-ttu-id="ab40c-116">Seien Sie vorsichtig mit nicht Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="ab40c-116">Be careful with NOT operations.</span></span> <span data-ttu-id="ab40c-117">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ab40c-117">Consider the following:</span></span>

    ```syntax
    UINT_PTR a; 
    ULONG b;
    a = a & ~(b - 1);
    ```

    <span data-ttu-id="ab40c-118">Das Problem besteht darin, dass ~ (b – 1) "0x0000 0000 xxxx xxxx" und nicht "0xFFFF FFFF xxxx xxxx" erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ab40c-118">The problem is that ~(b–1) produces "0x0000 0000 xxxx xxxx" and not "0xFFFF FFFF xxxx xxxx".</span></span> <span data-ttu-id="ab40c-119">Der Compiler erkennt dies nicht.</span><span class="sxs-lookup"><span data-stu-id="ab40c-119">The compiler will not detect this.</span></span> <span data-ttu-id="ab40c-120">Um dieses Problem zu beheben, ändern Sie den Code wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ab40c-120">To fix this, change the code as follows:</span></span>

    ```syntax
    a = a & ~((UINT_PTR)b - 1);
    ```

- <span data-ttu-id="ab40c-121">Achten Sie darauf, nicht signierte und signierte Vorgänge auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ab40c-121">Be careful performing unsigned and signed operations.</span></span> <span data-ttu-id="ab40c-122">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ab40c-122">Consider the following:</span></span>

    ```syntax
    LONG a;
    ULONG b;
    LONG c;

    a = -10;
    b = 2;
    c = a / b;
    ```

    <span data-ttu-id="ab40c-123">Das Ergebnis ist unerwartet groß.</span><span class="sxs-lookup"><span data-stu-id="ab40c-123">The result is unexpectedly large.</span></span> <span data-ttu-id="ab40c-124">Die Regel ist, dass das Ergebnis ohne Vorzeichen ist, wenn einer der beiden Operanden nicht signiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab40c-124">The rule is that if either operand is unsigned, the result is unsigned.</span></span> <span data-ttu-id="ab40c-125">Im vorherigen Beispiel wird eine in einen nicht signierten Wert, dividiert durch b, und das in c gespeicherte Ergebnis konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ab40c-125">In the preceding example, a is converted to an unsigned value, divided by b, and the result stored in c.</span></span> <span data-ttu-id="ab40c-126">Die Konvertierung umfasst keine numerische Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="ab40c-126">The conversion involves no numeric manipulation.</span></span>

    <span data-ttu-id="ab40c-127">Beachten Sie als weiteres Beispiel Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ab40c-127">As another example, consider the following:</span></span>

    ```syntax
    ULONG x;
    LONG y;
    LONG *pVar1;
    LONG *pVar2;

    pVar2 = pVar1 + y * (x - 1);
    ```

    <span data-ttu-id="ab40c-128">Das Problem tritt auf, weil x nicht signiert ist, wodurch der gesamte Ausdruck nicht signiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab40c-128">The problem arises because x is unsigned, which makes the entire expression unsigned.</span></span> <span data-ttu-id="ab40c-129">Dies funktioniert problemlos, es sei denn, y ist negativ.</span><span class="sxs-lookup"><span data-stu-id="ab40c-129">This works fine unless y is negative.</span></span> <span data-ttu-id="ab40c-130">In diesem Fall wird y in einen Wert ohne Vorzeichen konvertiert, der Ausdruck wird mit einer Genauigkeit von 32 Bit ausgewertet, skaliert und zu pVar1 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab40c-130">In this case, y is converted to an unsigned value, the expression is evaluated using 32-bit precision, scaled, and added to pVar1.</span></span> <span data-ttu-id="ab40c-131">Eine negative 32-Bit-Zahl ohne Vorzeichen wird zu einer großen 64-Bit-positiven Zahl, die das falsche Ergebnis liefert.</span><span class="sxs-lookup"><span data-stu-id="ab40c-131">A 32-bit unsigned negative number becomes a large 64-bit positive number, which gives the wrong result.</span></span> <span data-ttu-id="ab40c-132">Um dieses Problem zu beheben, deklarieren Sie x als einen signierten Wert, oder legen Sie ihn explizit in **Long** im Ausdruck ab.</span><span class="sxs-lookup"><span data-stu-id="ab40c-132">To fix this problem, declare x as a signed value or explicitly typecast it to **LONG** in the expression.</span></span>

- <span data-ttu-id="ab40c-133">Gehen Sie beim Erstellen von Zuordnungen mit schrittweisen Größen vorsichtig vor.</span><span class="sxs-lookup"><span data-stu-id="ab40c-133">Be careful when making piecemeal size allocations.</span></span> <span data-ttu-id="ab40c-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ab40c-134">For example:</span></span>

    ```syntax
    struct xx {
       DWORD NumberOfPointers;
       PVOID Pointers[100];
    };
    ```

    <span data-ttu-id="ab40c-135">Der folgende Code ist falsch, da der Compiler die Struktur mit zusätzlichen 4 Bytes auffüllt, um die 8-Byte-Ausrichtung zu treffen:</span><span class="sxs-lookup"><span data-stu-id="ab40c-135">The following code is wrong because the compiler will pad the structure with an additional 4 bytes to make the 8-byte alignment:</span></span>

    ```syntax
    malloc(sizeof(DWORD) + 100*sizeof(PVOID));
    ```

    <span data-ttu-id="ab40c-136">Der folgende Code ist korrekt:</span><span class="sxs-lookup"><span data-stu-id="ab40c-136">The following code is correct:</span></span>

    ```syntax
    malloc(offsetof(struct xx, Pointers) + 100*sizeof(PVOID));
    ```

- <span data-ttu-id="ab40c-137">Übergeben Sie nicht `(HANDLE)0xFFFFFFFF` an Funktionen wie z. b. " [**kreatefilemapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)".</span><span class="sxs-lookup"><span data-stu-id="ab40c-137">Do not pass `(HANDLE)0xFFFFFFFF` to functions such as [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga).</span></span> <span data-ttu-id="ab40c-138">Verwenden Sie stattdessen **einen ungültigen \_ handle- \_ Wert**.</span><span class="sxs-lookup"><span data-stu-id="ab40c-138">Instead, use **INVALID\_HANDLE\_VALUE**.</span></span>
- <span data-ttu-id="ab40c-139">Verwenden Sie die richtigen Format Bearbeiter, wenn Sie eine Zeichenfolge drucken.</span><span class="sxs-lookup"><span data-stu-id="ab40c-139">Use the proper format specifiers when printing a string.</span></span> <span data-ttu-id="ab40c-140">Verwenden Sie% p, um Zeiger in Hexadezimal zu drucken.</span><span class="sxs-lookup"><span data-stu-id="ab40c-140">Use %p to print pointers in hexadecimal.</span></span> <span data-ttu-id="ab40c-141">Dies ist die beste Wahl für das Drucken von Zeigern.</span><span class="sxs-lookup"><span data-stu-id="ab40c-141">This is the best choice for printing pointers.</span></span> <span data-ttu-id="ab40c-142">Der Microsoft Visual C++ unterstützt% I. zum Drucken von polymorphen Daten.</span><span class="sxs-lookup"><span data-stu-id="ab40c-142">Microsoft Visual C++ supports %I to print polymorphic data.</span></span> <span data-ttu-id="ab40c-143">Visual C++ unterstützt auch% I64, um Werte, die 64 Bits sind, zu drucken.</span><span class="sxs-lookup"><span data-stu-id="ab40c-143">Visual C++ also supports %I64 to print values that are 64 bits.</span></span>

 

 