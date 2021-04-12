---
title: Häufige Compilerfehler
description: In diesem Abschnitt werden typische Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten. Diese Beispiele stammen aus dem HAL-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.
ms.assetid: bbb6a57f-281a-4a6e-a4b6-15846d0cf21f
keywords:
- Compilerfehler 64-Bit-Windows-Programmierung
- Migration 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84a5f5f58f2cab7555ce3401ed6fae0af240f4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316803"
---
# <a name="common-compiler-errors"></a><span data-ttu-id="10adf-106">Häufige Compilerfehler</span><span class="sxs-lookup"><span data-stu-id="10adf-106">Common Compiler Errors</span></span>

<span data-ttu-id="10adf-107">In diesem Abschnitt werden typische Compilerfehler veranschaulicht, die beim Migrieren einer vorhandenen Codebasis auftreten.</span><span class="sxs-lookup"><span data-stu-id="10adf-107">This section illustrates the typical compiler errors that occur when migrating an existing code base.</span></span> <span data-ttu-id="10adf-108">Diese Beispiele stammen aus dem HAL-Code auf Systemebene, obwohl die Konzepte direkt auf Code auf Benutzerebene anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="10adf-108">These examples happen to be from system-level HAL code, although the concepts are directly applicable to user-level code.</span></span>

## <a name="warning-c4311-example-1"></a><span data-ttu-id="10adf-109">Warnung C4311 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10adf-109">Warning C4311 Example 1</span></span>

<span data-ttu-id="10adf-110">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-110">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="10adf-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-111"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = (ULONG) CIA_PCI_CONFIG_BASE_QVA;`

</dd> <dt>

<span data-ttu-id="10adf-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-112"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-113">**Ptrtoulong** ist abhängig von ihrer Verwendung eine Inline Funktion oder ein Makro.</span><span class="sxs-lookup"><span data-stu-id="10adf-113">**PtrToUlong** is an inline function or macro, depending on your usage.</span></span> <span data-ttu-id="10adf-114">Ein Zeiger auf einen **ulong**-Wert wird abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10adf-114">It truncates a pointer to a **ULONG**.</span></span> <span data-ttu-id="10adf-115">Obwohl 32-Bit-Zeiger nicht betroffen sind, wird die obere Hälfte eines 64-Bit-Zeigers abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="10adf-115">Although 32-bit pointers are not affected, the upper half of a 64-bit pointer is truncated.</span></span>

<span data-ttu-id="10adf-116">Die CIA \_ PCI- \_ Konfigurations Basis- \_ \_ QVA ist als **pVoid** deklariert.</span><span class="sxs-lookup"><span data-stu-id="10adf-116">CIA\_PCI\_CONFIG\_BASE\_QVA is declared as a **PVOID**.</span></span> <span data-ttu-id="10adf-117">Der **ulong** Cast funktioniert in der 32-Bit-Welt, führt jedoch zu einem Fehler in der 64-Bit-Welt.</span><span class="sxs-lookup"><span data-stu-id="10adf-117">The **ULONG** cast works in the 32-bit world, but results in an error in the 64-bit world.</span></span> <span data-ttu-id="10adf-118">Die Lösung besteht darin, einen 64-Bit-Zeiger auf einen **ulong**-Wert zu erhalten, da das Ändern der Definition der Union, die ppciaddr->u. AsULong definiert ist, zu viel Code ändert.</span><span class="sxs-lookup"><span data-stu-id="10adf-118">The solution is to get a 64-bit pointer to a **ULONG**, because changing the definition of the union that pPciAddr->u.AsULONG is defined in changes too much code.</span></span>

<span data-ttu-id="10adf-119">Die Verwendung des Makros **ptrtoulong** zum Konvertieren der 64-Bit- **pVoid** in den benötigten **ulong** -Wert ist zulässig, da wir wissen über den spezifischen Wert der CIA- \_ PCI- \_ Konfigurations Basis- \_ \_ QVA verfügen.</span><span class="sxs-lookup"><span data-stu-id="10adf-119">Using the macro **PtrToUlong** to convert the 64-bit **PVOID** to the needed **ULONG** is allowed because we have knowledge about the specific value of CIA\_PCI\_CONFIG\_BASE\_QVA.</span></span> <span data-ttu-id="10adf-120">In diesem Fall enthält dieser Zeiger niemals Daten in den oberen 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="10adf-120">In this case, this pointer will never have data in the upper 32 bits.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-121"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`pPciAddr->u.AsULONG = PtrToUlong(CIA_PCI_CONFIG_BASE_QVA);`

</dd> </dl>

## <a name="warning-c4311-example-2"></a><span data-ttu-id="10adf-122">Warnung C4311 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10adf-122">Warning C4311 Example 2</span></span>

<span data-ttu-id="10adf-123">"Typumwandlung": Zeiger Verkürzung von "struct \_ Error \_ Frame \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-123">'type cast' : pointer truncation from 'struct \_ERROR\_FRAME \*\_\_ptr64 ' to 'unsigned long</span></span>

<dl> <dt>

<span data-ttu-id="10adf-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-124"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG)PUncorrectableError );`

</dd> <dt>

<span data-ttu-id="10adf-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-125"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-126">Das Problem besteht darin, dass der letzte Parameter für diese Funktion ein Zeiger auf eine Datenstruktur ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-126">The problem is that the last parameter to this function is a pointer to a data structure.</span></span> <span data-ttu-id="10adf-127">Da puncorrectableerror ein Zeiger ist, ändert sich die Größe mit dem Programmiermodell.</span><span class="sxs-lookup"><span data-stu-id="10adf-127">Because PUncorrectableError is a pointer, it changes size with the programming model.</span></span> <span data-ttu-id="10adf-128">Der Prototyp für **kebugcheckex** wurde geändert, sodass der letzte Parameter ein **ulong- \_ ptr** ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-128">The prototype for **KeBugCheckEx** was changed so that the last parameter is a **ULONG\_PTR**.</span></span> <span data-ttu-id="10adf-129">Daher ist es erforderlich, den Funktionszeiger in ein **ulong- \_ ptr** umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="10adf-129">As a result, it's necessary to cast the function pointer to a **ULONG\_PTR**.</span></span>

<span data-ttu-id="10adf-130">Sie können Fragen, warum **pVoid** nicht als letzter Parameter verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="10adf-130">You might ask why **PVOID** was not used as the last parameter.</span></span> <span data-ttu-id="10adf-131">Je nach Kontext des Aufrufes ist der letzte Parameter möglicherweise etwas anderes als ein Zeiger oder möglicherweise ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="10adf-131">Depending on the context of the call, the last parameter may be something other than a pointer or perhaps an error code.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-132"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`KeBugCheckEx( DATA_BUS_ERROR,0,0,0,(ULONG_PTR)PUncorrectableError );`

</dd> </dl>

## <a name="warning-c4244-example-1"></a><span data-ttu-id="10adf-133">Warnung C4244 Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10adf-133">Warning C4244 Example 1</span></span>

<span data-ttu-id="10adf-134">"=": Konvertierung von "struct \_ Configuration \_ Component \* \_ \_ ptr64" in "struct \_ Configuration \_ Component \* ", möglicher Datenverlust</span><span class="sxs-lookup"><span data-stu-id="10adf-134">'=' : conversion from 'struct \_CONFIGURATION\_COMPONENT \*\_\_ptr64 ' to 'struct \_CONFIGURATION\_COMPONENT \*', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="10adf-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-135"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

`Component = &CurrentEntry->ComponentEntry;`

</dd> <dt>

<span data-ttu-id="10adf-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-136"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-137">Die-Funktion deklariert die Variablen Komponente als pconfiguration- \_ Komponente.</span><span class="sxs-lookup"><span data-stu-id="10adf-137">The function declares the variable Component as a PCONFIGURATION\_COMPONENT.</span></span> <span data-ttu-id="10adf-138">Später wird die Variable in der folgenden Zuweisung verwendet, die korrekt angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="10adf-138">Later, the variable is used in the following assignment that appears correct:</span></span>

`Component = &CurrentEntry->ComponentEntry;`

<span data-ttu-id="10adf-139">Der Typ "pconfiguration" \_ ist jedoch wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="10adf-139">However, the type PCONFIGURATION\_COMPONENT is defined as:</span></span>

``` syntax
typedef struct __CONFIGURATION_COMPONENT {
...
...
} CONFIGURATION_COMPONENT, * POINTER_32 PCONFIGURATION_COMPONENT;
```

<span data-ttu-id="10adf-140">Die Typdefinition für die pconfiguration \_ -Komponente stellt einen 32-Bit-Zeiger sowohl in 32-Bit-als auch in 64-Bit-Modellen bereit, da Sie als **Zeiger \_ 32** deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-140">The type definition for PCONFIGURATION\_COMPONENT provides a 32-bit pointer in both 32-bit and 64-bit models because it is declared **POINTER\_32**.</span></span> <span data-ttu-id="10adf-141">Der ursprüngliche Designer dieser Struktur wusste, dass er in einem 32-Bit-Kontext im BIOS verwendet und ausdrücklich für diese Verwendung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="10adf-141">The original designer of this structure knew it was going to be used in a 32-bit context in the BIOS and expressly defined it for that use.</span></span> <span data-ttu-id="10adf-142">Dieser Code funktioniert problemlos in 32-Bit-Fenstern, da die Zeiger 32-Bit sind.</span><span class="sxs-lookup"><span data-stu-id="10adf-142">This code works fine in 32-bit Windows because the pointers happen to be 32-bit.</span></span> <span data-ttu-id="10adf-143">In 64-Bit-Fenstern funktioniert es nicht, da sich der Code im 64-Bit-Kontext befindet.</span><span class="sxs-lookup"><span data-stu-id="10adf-143">In 64-bit Windows, it does not work because the code is in 64-bit context.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-144"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="10adf-145">Um dieses Problem zu umgehen, verwenden Sie \_ die Konfigurationskomponente \* anstelle der 32-Bit-pconfiguration- \_ Komponente.</span><span class="sxs-lookup"><span data-stu-id="10adf-145">To work around this problem, use CONFIGURATION\_COMPONENT \* rather than the 32-bit PCONFIGURATION\_COMPONENT .</span></span> <span data-ttu-id="10adf-146">Es ist wichtig, dass Sie den Zweck des Codes eindeutig verstehen.</span><span class="sxs-lookup"><span data-stu-id="10adf-146">It is important to clearly understand the purpose of the code.</span></span> <span data-ttu-id="10adf-147">Wenn dieser Code das 32-Bit-BIOS oder den System Raum berühren soll, funktioniert diese Korrektur nicht.</span><span class="sxs-lookup"><span data-stu-id="10adf-147">If this code is intended to touch 32-bit BIOS or System space, this fix will not work.</span></span>

<span data-ttu-id="10adf-148">Der **Zeiger \_ 32** ist in "ntdef. h" und "Winnt. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="10adf-148">**POINTER\_32** is defined in Ntdef.h and Winnt.h.</span></span>

``` syntax
#ifdef (__AXP64__)
#define POINTER_32 _ptr32
#else
#define POINTER_32
#endif
```

</dd> </dl>

## <a name="warning-c4242-example-2"></a><span data-ttu-id="10adf-149">Warnung C4242 Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10adf-149">Warning C4242 Example 2</span></span>

<span data-ttu-id="10adf-150">"=": Konvertierung von " \_ \_ Int64" in "unsigned long", möglicher Datenverlust</span><span class="sxs-lookup"><span data-stu-id="10adf-150">'=' : conversion from '\_\_int64 ' to 'unsigned long ', possible loss of data</span></span>

<dl> <dt>

<span data-ttu-id="10adf-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-151"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ARC_STATUS HalpCopyNVRamBuffer (
IN PCHAR NvDestPtr,
IN PCHAR NvSrcPtr,
IN ULONG Length )
{

ULONG PageSelect1, ByteSelect1;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;

ByteSelect1 = (NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;
```

</dd> <dt>

<span data-ttu-id="10adf-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-152"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-153">Diese Warnung wird generiert, da die Berechnung 64-Bit-Werte verwendet, in diesem Fall Zeiger und das Ergebnis in einem 32-Bit- **ulong** platzieren.</span><span class="sxs-lookup"><span data-stu-id="10adf-153">This warning is generated because the calculation is using 64-bit values, in this case pointers, and placing the result in a 32-bit **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-154"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="10adf-155">Geben Sie das Ergebnis der Berechnung in ein **ulong** -Ergebnis ein, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="10adf-155">Type cast the result of the calculation to a **ULONG** as shown here:</span></span>

`ByteSelect1 = (ULONG)(NvDestPtr - (PUCHAR)HalpCMOSRamBase) & CONFIG_RAM_BYTE_MASK;`

<span data-ttu-id="10adf-156">Typecasting das Ergebnis ermöglicht dem Compiler, dass Sie sich über das Ergebnis sicher sind.</span><span class="sxs-lookup"><span data-stu-id="10adf-156">Typecasting the result lets the compiler know you are sure about the result.</span></span> <span data-ttu-id="10adf-157">Das heißt, dass Sie die Berechnung verstehen und sicher sind, dass Sie in einen 32-Bit- **ulong** passt.</span><span class="sxs-lookup"><span data-stu-id="10adf-157">That being said, make certain you understand the calculation and really are sure it will fit in a 32-bit **ULONG**.</span></span>

<span data-ttu-id="10adf-158">Wenn das Ergebnis möglicherweise nicht in einen 32-Bit- **ulong** passt, ändern Sie den Basistyp der Variablen, die das Ergebnis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="10adf-158">If the result may not fit in a 32-bit **ULONG**, change the base type of the variable that will hold the result.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-1"></a><span data-ttu-id="10adf-159">Warnung C4311-Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10adf-159">Warning C4311 - Example 1</span></span>

<span data-ttu-id="10adf-160">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-160">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="10adf-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-161"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
ULONG HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG ReadQva,
OUT PULONG WriteQva)
{
ULONG ComPortAddress;

ULONG PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}
PortQva = (ULONG)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

</dd> <dt>

<span data-ttu-id="10adf-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-162"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-163">Diese gesamte Funktion behandelt Adressen als ganze Zahlen. Dies erfordert, dass die ganzen Zahlen auf tragbare Weise typiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="10adf-163">This entire function deals with addresses as integers, necessitating the need to type those integers in a portable way.</span></span> <span data-ttu-id="10adf-164">Alle lokalen Variablen, Zwischenwerte in Berechnungen und Rückgabewerte sollten Portable Typen sein.</span><span class="sxs-lookup"><span data-stu-id="10adf-164">All the local variables, intermediate values in calculations, and return values should be portable types.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-165"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
ULONG_PTR HalpMapDebugPort(
IN ULONG ComPort,
OUT PULONG_PTR ReadQva,
OUT PULONG_PTR WriteQva)
{
ULONG_PTR ComPortAddress;

ULONG_PTR PortQva;

// Compute the port address, based on the desired com port.

switch( ComPort ){
case 1:
   ComPortAddress = COM1_ISA_PORT_ADDRESS;
   break;

case 2:
default:
   ComPortAddress = COM2_ISA_PORT_ADDRESS;
}

PortQva = (ULONG_PTR)HAL_MAKE_QVA(CIA_PCI_SPARSE_IO_PHYSICAL) + ComPortAddress;

// Return the QVAs for read and write access.

*ReadQva = PortQva;
*WriteQva = PortQva;

return ComPortAddress;
}
```

<span data-ttu-id="10adf-166">**Pulong \_ PTR** ist ein Zeiger, der selbst 32 Bits für 32-Bit-Windows und 64 Bits für 64-Bit-Windows ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-166">**PULONG\_PTR** is a pointer that is itself 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span> <span data-ttu-id="10adf-167">Er verweist auf eine Ganzzahl ohne Vorzeichen, **ulong \_ ptr**, 32 Bits für 32-Bit-Windows und 64 Bits für 64-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="10adf-167">It points to an unsigned integer, **ULONG\_PTR**, that is 32 bits for 32-bit Windows and 64 bits for 64-bit Windows.</span></span>

</dd> </dl>

## <a name="warning-c4311---example-2"></a><span data-ttu-id="10adf-168">Warnung C4311-Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="10adf-168">Warning C4311 - Example 2</span></span>

<span data-ttu-id="10adf-169">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-169">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="10adf-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-170"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
BOOLEAN
HalpMapIoSpace (
VOID
)
{
PVOID PciIoSpaceBase;
PciIoSpaceBase = HAL_MAKE_QVA( CIA_PCI_SPARSE_IO_PHYSICAL );

//Map base addresses in QVA space.

HalpCMOSRamBase = (PVOID)((ULONG)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);
```

</dd> <dt>

<span data-ttu-id="10adf-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-171"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-172">Obwohl alle QVA (quasi Virtual Address)-Werte in dieser Phase tatsächlich 32-Bit-Werte sind und in einen **ulong** passen, ist es einheitlicher, alle Adressen als **ulong \_ ptr** -Werte zu behandeln, wenn dies möglich ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-172">Even though all QVA (Quasi Virtual Address) values are really 32-bit values at this stage and will fit in a **ULONG**, it is more consistent to treat all addresses as **ULONG\_PTR** values when possible.</span></span>

<span data-ttu-id="10adf-173">Der Zeiger pciiospacebase enthält das QVA, das im Makro-HAL \_ make \_ QVA erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="10adf-173">The pointer PciIoSpaceBase holds the QVA that is created in the macro HAL\_MAKE\_QVA.</span></span> <span data-ttu-id="10adf-174">Dieses Makro gibt einen 64-Bit-Wert zurück, bei dem die oberen 32 Bits auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="10adf-174">This macro returns a 64-bit value with the top 32 bits set to zero so the math will work.</span></span> <span data-ttu-id="10adf-175">Wir könnten einfach den Code belassen, um den Zeiger auf einen **ulong**-Wert zu kürzen, aber diese Vorgehensweise wird nicht empfohlen, um die Code Wartbarkeit und Portabilität zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="10adf-175">We could simply leave the code to truncate the pointer into a **ULONG**, but this practice is discouraged to enhance code maintainability and portability.</span></span> <span data-ttu-id="10adf-176">Beispielsweise kann sich der Inhalt eines QVA in der Zukunft ändern, um einige der oberen Bits auf dieser Ebene zu verwenden, und den Code zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="10adf-176">For example, the contents of a QVA might change in the future to use some of the upper bits at this level, breaking the code.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-177"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="10adf-178">Stellen Sie sicher, und verwenden Sie **ulong \_ ptr** für alle Adress-und Zeiger-Mathematik.</span><span class="sxs-lookup"><span data-stu-id="10adf-178">Be safe and use **ULONG\_PTR** for all address and pointer math.</span></span>

`HalpCMOSRamBase = (PVOID)((ULONG_PTR)PciIoSpaceBase + CMOS_ISA_PORT_ADDRESS);`

</dd> </dl>

## <a name="warning-c4311-example-3"></a><span data-ttu-id="10adf-179">Warnung C4311 Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="10adf-179">Warning C4311 Example 3</span></span>

<span data-ttu-id="10adf-180">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-180">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="10adf-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-181"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
PVOID
HalDereferenceQva(
PVOID Qva,
INTERFACE_TYPE InterfaceType,
ULONG BusNumber)

if ( ((ULONG) Qva & QVA_SELECTORS) == QVA_ENABLE ) {

return( (PVOID)( (ULONG)Qva << IO_BIT_SHIFT ) );
} 
else {
return (Qva);
}
```

</dd> <dt>

<span data-ttu-id="10adf-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-182"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-183">Der Compiler warnt vor der Adresse der (&)-und Left Shift-Operatoren (<<), wenn Sie auf Zeiger Typen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="10adf-183">The compiler warns about the address of (&) and left shift (<<) operators if they are applied to pointer types.</span></span> <span data-ttu-id="10adf-184">Im obigen Code ist QVA ein **pVoid** -Wert.</span><span class="sxs-lookup"><span data-stu-id="10adf-184">In the above code, Qva is a **PVOID** value.</span></span> <span data-ttu-id="10adf-185">Dies muss in einen ganzzahligen Typ umgewandelt werden, um die Mathematik auszuführen.</span><span class="sxs-lookup"><span data-stu-id="10adf-185">We need to cast that to an integer type to perform the math.</span></span> <span data-ttu-id="10adf-186">Da der Code portabel sein muss, verwenden Sie **ulong \_ ptr** anstelle von **ulong**.</span><span class="sxs-lookup"><span data-stu-id="10adf-186">Because the code must be portable, use **ULONG\_PTR** instead of **ULONG**.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-187"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

``` syntax
if ( ((ULONG_PTR) Qva & QVA_SELECTORS) == QVA_ENABLE ) {
  return( (PVOID)( (ULONG_PTR)Qva << IO_BIT_SHIFT ) );
```

</dd> </dl>

## <a name="warning-c4311-example-4"></a><span data-ttu-id="10adf-188">Warnung C4311 Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="10adf-188">Warning C4311 Example 4</span></span>

<span data-ttu-id="10adf-189">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-189">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="10adf-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-190"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
TranslatedAddress->LowPart = (ULONG)HalCreateQva(
*TranslatedAddress, va);
```

</dd> <dt>

<span data-ttu-id="10adf-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-192">Translatedaddress ist eine Union, die etwa wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="10adf-192">TranslatedAddress is a union that looks something like the following:</span></span>

``` syntax
typedef union
   Struct {
      ULONG LowPart;
      LONG Highpart;
   }
   LONGLONG QuadPart;
}
```

</dd> <dt>

<span data-ttu-id="10adf-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-193"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

<span data-ttu-id="10adf-194">Wenn Sie wissen, was der restliche Code in highpart platzieren könnte, können wir eine der hier gezeigten Lösungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="10adf-194">Knowing what the rest of the code might place in Highpart, we can select either of the solutions shown here.</span></span>

`TranslatedAddress->LowPart = PtrToUlong(HalCreateQva(*TranslatedAddress,va) );`

<span data-ttu-id="10adf-195">Das **ptrtoulong** -Makro verkürzt den von **halkreateqva** zurückgegebenen Zeiger auf 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="10adf-195">The **PtrToUlong** macro truncates the pointer returned by **HalCreateQva** to 32 bits.</span></span> <span data-ttu-id="10adf-196">Wir wissen, dass für das von **halkreateqva** zurückgegebene QVA die oberen 32 Bits auf NULL festgelegt sind und die nächste Zeile des Codes translatedaddress->highpart auf 0 (null) festlegt.</span><span class="sxs-lookup"><span data-stu-id="10adf-196">We know that the QVA returned by **HalCreateQva** has the upper 32 bits set to zero and the very next line of code sets TranslatedAddress->Highpart to zero.</span></span>

<span data-ttu-id="10adf-197">Mit Vorsicht können wir Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="10adf-197">With caution, we could use the following:</span></span>

`TranslatedAddress->QuadPart = (LONGLONG)HalCreateQva(*TranslatedAddress,va);`

<span data-ttu-id="10adf-198">Dies funktioniert in diesem Beispiel: das-Makro von **halkreateqva** gibt 64 Bits zurück, wobei die oberen 32 Bits auf 0 (null) festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="10adf-198">This works in this example: the **HalCreateQva** macro is returning 64 bits, with the upper 32 bits set to zero.</span></span> <span data-ttu-id="10adf-199">Achten Sie darauf, dass die oberen 32 Bits nicht in einer 32-Bit-Umgebung undefiniert bleiben, was diese zweite Lösung tatsächlich bewirken könnte.</span><span class="sxs-lookup"><span data-stu-id="10adf-199">Just be careful not to leave the upper 32 bits undefined in a 32-bit environment, which this second solution may actually do.</span></span>

</dd> </dl>

## <a name="warning-c4311-example-5"></a><span data-ttu-id="10adf-200">Warnung C4311 Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="10adf-200">Warning C4311 Example 5</span></span>

<span data-ttu-id="10adf-201">"Typumwandlung": Zeiger Verkürzung von "void \* \_ \_ ptr64" in "unsigned long"</span><span class="sxs-lookup"><span data-stu-id="10adf-201">'type cast' : pointer truncation from 'void \*\_\_ptr64 ' to 'unsigned long '</span></span>

<dl> <dt>

<span data-ttu-id="10adf-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="10adf-202"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

``` syntax
VOID
HalpCiaProgramDmaWindow(
PWINDOW_CONTROL_REGISTERS WindowRegisters,
PVOID MapRegisterBase
)
{
CIA_WBASE Wbase;

Wbase.all = 0;
Wbase.Wen = 1;
Wbase.SgEn = 1;
Wbase.Wbase = (ULONG)(WindowRegisters->WindowBase) >> 20;
```

</dd> <dt>

<span data-ttu-id="10adf-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung</span><span class="sxs-lookup"><span data-stu-id="10adf-203"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="10adf-204">Windowregistern->windowbase ist ein Zeiger und ist nun 64 Bits.</span><span class="sxs-lookup"><span data-stu-id="10adf-204">WindowRegisters->WindowBase is a pointer and is now 64 bits.</span></span> <span data-ttu-id="10adf-205">Der Code besagt, dass dieser Wert 20 Bits nach rechts verschiebt.</span><span class="sxs-lookup"><span data-stu-id="10adf-205">The code says to right-shift this value 20 bits.</span></span> <span data-ttu-id="10adf-206">Der Compiler lässt nicht zu, dass der Right Shift-Operator (>>) auf einem Zeiger verwendet wird. Daher müssen wir Sie in eine ganze Zahl umwandeln.</span><span class="sxs-lookup"><span data-stu-id="10adf-206">The compiler will not let us use the right-shift (>>) operator on a pointer; therefore, we need to cast it to some sort of integer.</span></span>

</dd> <dt>

<span data-ttu-id="10adf-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Not</span><span class="sxs-lookup"><span data-stu-id="10adf-207"><span id="Solution"></span><span id="solution"></span><span id="SOLUTION"></span>Solution</span></span>
</dt> <dd>

`Wbase.Wbase= PtrToUlong ( (PVOID) ((ULONG_PTR) (WindowRegisters->WindowBase) >> 20));`

<span data-ttu-id="10adf-208">Die Umwandlung in einen **ulong- \_ ptr** ist genau das, was wir benötigen.</span><span class="sxs-lookup"><span data-stu-id="10adf-208">Casting to a **ULONG\_PTR** is just what we need.</span></span> <span data-ttu-id="10adf-209">Das nächste Problem ist wbase.</span><span class="sxs-lookup"><span data-stu-id="10adf-209">The next problem is Wbase.</span></span> <span data-ttu-id="10adf-210">Wbase ist ein **ulong** und ist 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="10adf-210">Wbase is a **ULONG** and is 32 bits.</span></span> <span data-ttu-id="10adf-211">In diesem Fall wissen wir, dass der 64-Bit-Zeiger windowregistern->windowbase in den niedrigeren 32 Bits auch nach dem Verschieben gültig ist.</span><span class="sxs-lookup"><span data-stu-id="10adf-211">In this case, we know that the 64-bit pointer WindowRegisters->WindowBase is valid in the lower 32 bits even after being shifted.</span></span> <span data-ttu-id="10adf-212">Dies verwendet das **ptrtoulong** -Makro als akzeptabel, da der 64-Bit-Zeiger in ein 32-Bit- **ulong** abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="10adf-212">This makes use of the **PtrToUlong** macro acceptable, because it will truncate the 64-bit pointer into a 32-bit **ULONG**.</span></span> <span data-ttu-id="10adf-213">Die **pVoid** -Umwandlung ist erforderlich, da **ptrtoulong** ein Zeigerargument erwartet.</span><span class="sxs-lookup"><span data-stu-id="10adf-213">The **PVOID** cast is necessary because **PtrToUlong** expects a pointer argument.</span></span> <span data-ttu-id="10adf-214">Wenn Sie sich den resultierenden Assemblycode ansehen, wird die gesamte Umwandlung von C-Code nur zu einer Last von Quad, Shift Right und Store Long.</span><span class="sxs-lookup"><span data-stu-id="10adf-214">When you look at the resulting assembler code, all this C code casting becomes just a load quad, shift right, and store long.</span></span>

</dd> </dl>

 

 




