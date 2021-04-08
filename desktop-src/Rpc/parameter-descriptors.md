---
title: Parameter Deskriptoren
description: Wie bereits erwähnt, sind die OIF-Stil Parameter Deskriptoren vorhanden.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729409"
---
# <a name="parameter-descriptors"></a><span data-ttu-id="2f8e2-103">Parameter Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="2f8e2-103">Parameter Descriptors</span></span>

<span data-ttu-id="2f8e2-104">Wie bereits erwähnt, gibt es die Parameter Deskriptoren [**– Oi**](/windows/desktop/Midl/-oi) und **– OIF** .</span><span class="sxs-lookup"><span data-stu-id="2f8e2-104">As mentioned previously, [**–Oi**](/windows/desktop/Midl/-oi) and **–Oif** style parameter descriptors exist.</span></span>

## <a name="the-oi-parameter-descriptors"></a><span data-ttu-id="2f8e2-105">Die Parameter Deskriptoren von – Oi</span><span class="sxs-lookup"><span data-stu-id="2f8e2-105">The –Oi Parameter Descriptors</span></span>

<span data-ttu-id="2f8e2-106">Vollständig interpretierte stubvorgänge erfordern zusätzliche Informationen für jeden Parameter in einem RPC-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-106">Fully interpreted stubs require additional information for each of the parameters in an RPC call.</span></span> <span data-ttu-id="2f8e2-107">Die Parameter Beschreibungen einer Prozedur folgen unmittelbar nach der Beschreibung der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-107">The parameter descriptions of a procedure follow immediately after the description of the procedure.</span></span>

[<span data-ttu-id="2f8e2-108">**Einfache – Oi**</span><span class="sxs-lookup"><span data-stu-id="2f8e2-108">**Simple –Oi**</span></span>](/windows/desktop/Midl/-oi)

<span data-ttu-id="2f8e2-109">**Parameter Deskriptoren**</span><span class="sxs-lookup"><span data-stu-id="2f8e2-109">**Parameter Descriptors**</span></span>

<span data-ttu-id="2f8e2-110">Das Format für die Beschreibung eines \[ **in** - \] oder Return simple type-Parameters ist:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-110">The format for the description of an \[**in**\] or return simple type parameter is:</span></span>

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="2f8e2-111">– oder –</span><span class="sxs-lookup"><span data-stu-id="2f8e2-111">–or–</span></span>

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

<span data-ttu-id="2f8e2-112">Dabei \_ ist Simple Type<1> das FC-Token, das den einfachen Typ angibt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-112">Where simple\_type<1> is the FC token indicating the simple type.</span></span> <span data-ttu-id="2f8e2-113">Die Codes lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-113">The codes are as follows:</span></span>

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

<span data-ttu-id="2f8e2-114">**Sonstige – Oi**</span><span class="sxs-lookup"><span data-stu-id="2f8e2-114">**Other –Oi**</span></span>

<span data-ttu-id="2f8e2-115">**Parameter Deskriptoren**</span><span class="sxs-lookup"><span data-stu-id="2f8e2-115">**Parameter Descriptors**</span></span>

<span data-ttu-id="2f8e2-116">Das Format der Beschreibung für alle anderen Parametertypen lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-116">The format for the description for all other parameter types is:</span></span>

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

<span data-ttu-id="2f8e2-117">Dabei muss die Parameter \_ Richtung<1> für jede dieser Beschreibungen eine der in der folgenden Tabelle aufgeführten Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-117">Where the param\_direction<1> field for each of these descriptions must be one of those shown in the following table.</span></span>



| <span data-ttu-id="2f8e2-118">Hex</span><span class="sxs-lookup"><span data-stu-id="2f8e2-118">Hex</span></span> | <span data-ttu-id="2f8e2-119">Flag</span><span class="sxs-lookup"><span data-stu-id="2f8e2-119">Flag</span></span>                          | <span data-ttu-id="2f8e2-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2f8e2-120">Meaning</span></span>                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f8e2-121">4d</span><span class="sxs-lookup"><span data-stu-id="2f8e2-121">4d</span></span>  | <span data-ttu-id="2f8e2-122">FC \_ in \_ param</span><span class="sxs-lookup"><span data-stu-id="2f8e2-122">FC\_IN\_PARAM</span></span>                 | <span data-ttu-id="2f8e2-123">Ein in-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-123">An in parameter.</span></span>                                            |
| <span data-ttu-id="2f8e2-124">50</span><span class="sxs-lookup"><span data-stu-id="2f8e2-124">50</span></span>  | <span data-ttu-id="2f8e2-125">FC \_ im \_ out-Parameter \_</span><span class="sxs-lookup"><span data-stu-id="2f8e2-125">FC\_IN\_OUT\_PARAM</span></span>            | <span data-ttu-id="2f8e2-126">Ein in/out-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-126">An in/out parameter.</span></span>                                        |
| <span data-ttu-id="2f8e2-127">51</span><span class="sxs-lookup"><span data-stu-id="2f8e2-127">51</span></span>  | <span data-ttu-id="2f8e2-128">FC-out-Parameter \_ \_</span><span class="sxs-lookup"><span data-stu-id="2f8e2-128">FC\_OUT\_PARAM</span></span>                | <span data-ttu-id="2f8e2-129">Ein out-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-129">An out parameter.</span></span>                                           |
| <span data-ttu-id="2f8e2-130">52</span><span class="sxs-lookup"><span data-stu-id="2f8e2-130">52</span></span>  | <span data-ttu-id="2f8e2-131">FC- \_ Rückgabe Parameter \_</span><span class="sxs-lookup"><span data-stu-id="2f8e2-131">FC\_RETURN\_PARAM</span></span>             | <span data-ttu-id="2f8e2-132">Ein-Prozedur Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-132">A procedure return value.</span></span>                                   |
| <span data-ttu-id="2f8e2-133">4f</span><span class="sxs-lookup"><span data-stu-id="2f8e2-133">4f</span></span>  | <span data-ttu-id="2f8e2-134">FC \_ in \_ param \_ ohne \_ freie \_ inst</span><span class="sxs-lookup"><span data-stu-id="2f8e2-134">FC\_IN\_PARAM\_NO\_FREE\_INST</span></span> | <span data-ttu-id="2f8e2-135">Ein in xmit/Rep als Parameter, für den keine Freigabe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-135">An in xmit/rep as a parameter for which no freeing is made.</span></span> |



 

<span data-ttu-id="2f8e2-136">Die Stapel \_ Größe<1> ist die Größe des Parameters auf dem Stapel, ausgedrückt als die Anzahl von Ganzzahlen, die der Parameter im Stapel einnimmt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-136">The stack\_size<1> is the size of the parameter on the stack, expressed as the number of integers the parameter occupies on the stack.</span></span>

> [!Note]  
> <span data-ttu-id="2f8e2-137">Der [**– Oi**](/windows/desktop/Midl/-oi) -Modus wird auf 64-Bit-Plattformen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-137">The [**–Oi**](/windows/desktop/Midl/-oi) mode is not supported on 64-bit platforms.</span></span>

 

<span data-ttu-id="2f8e2-138">Der \_ typoffset<2> Feld ist der Offset in der Zeichen folgen Tabelle des typformats, der den Typdeskriptor für das Argument angibt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-138">The type\_offset<2> field is the offset in the type format string table, indicating the type descriptor for the argument.</span></span>

## <a name="the-oif-parameter-descriptors"></a><span data-ttu-id="2f8e2-139">Die – OIF-Parameter Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="2f8e2-139">The –Oif Parameter Descriptors</span></span>

<span data-ttu-id="2f8e2-140">Es gibt zwei mögliche Formate für eine Parameter Beschreibung: eine für Basis Typen, eine für alle anderen Typen.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-140">There are two possible formats for a parameter description, one for base types, another for all other types.</span></span>

<span data-ttu-id="2f8e2-141">Basis Typen:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-141">Base types:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

<span data-ttu-id="2f8e2-142">Sonstiges:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-142">Other:</span></span>

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

<span data-ttu-id="2f8e2-143">In beiden Stapel \_ Offset<2> den Offset auf dem virtuellen Argument Stapel in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-143">In both stack\_offset<2> indicates the offset on the virtual argument stack, in bytes.</span></span> <span data-ttu-id="2f8e2-144">Für Basis Typen wird der Argumenttyp direkt durch das Formatzeichen angegeben, das dem-Typ entspricht.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-144">For base types, the argument type is given directly by the format character corresponding to the type.</span></span> <span data-ttu-id="2f8e2-145">Bei anderen Typen \_ gibt das> Feld typoffset<2 den Offset in der Zeichen folgen Tabelle des typformats an, in der sich der Typdeskriptor für das Argument befindet.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-145">For other types, the type\_offset<2> field gives the offset in the type format string table where the type descriptor for the argument is located.</span></span>

<span data-ttu-id="2f8e2-146">Das Feld "Parameter Attribut" ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="2f8e2-146">The parameter attribute field is defined as follows:</span></span>

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   <span data-ttu-id="2f8e2-147">Das **mustsize** -Bit wird nur festgelegt, wenn der Parameter eine Größe aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-147">The **MustSize** bit is set only if the parameter must be sized.</span></span>
-   <span data-ttu-id="2f8e2-148">Das **mustfree** -Bit wird festgelegt, wenn der Server die ndrfree-Routine des Parameters aufrufen muss \* .</span><span class="sxs-lookup"><span data-stu-id="2f8e2-148">The **MustFree** bit is set if the server must call the parameter's NdrFree\* routine.</span></span>
-   <span data-ttu-id="2f8e2-149">Das **issimpleref** -Bit ist für einen Parameter festgelegt, bei dem es sich um einen Verweis Zeiger auf einen anderen Zeiger handelt, der keine Attribute zuordnen hat.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-149">The **IsSimpleRef** bit is set for a parameter that is a reference pointer to anything other than another pointer, and which has no allocate attributes.</span></span> <span data-ttu-id="2f8e2-150">Bei einem solchen Typ \_ stellt das typoffset<> Feld der Parameter Beschreibung, mit Ausnahme eines Verweis Zeigers auf einen Basistyp, den Offset für den Typ des Referenten bereit. der Verweis Zeiger wird einfach übersprungen.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-150">For such a type, the parameter description's type\_offset<> field, except for a reference pointer to a base type, provides the offset to the referent's type; the reference pointer is simply skipped.</span></span>
-   <span data-ttu-id="2f8e2-151">Das **isdontcallfreeinst** Bit ist für eine bestimmte Darstellung \_ als Parameter festgelegt, deren freie instanzroutinen nicht aufgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-151">The **IsDontCallFreeInst** bit is set for certain represent\_as parameters whose free instance routines should not be called.</span></span>
-   <span data-ttu-id="2f8e2-152">Die " **serverallocsize** "-Bits sind ungleich 0 (null), wenn der Parameter " \[ **out**" \] , " \[ **in**" oder "in", " \] \[ **out** " \] -Zeiger auf einen Zeiger oder ein Zeiger auf "enum16" ist und auf dem Stapel des Server interpreters initialisiert wird, anstatt einen Aufrufen von " **I \_ rpczuordnen**"</span><span class="sxs-lookup"><span data-stu-id="2f8e2-152">The **ServerAllocSize** bits are nonzero if the parameter is \[**out**\], \[**in**\], or \[**in,out**\] pointer to pointer, or pointer to enum16, and will be initialized on the server interpreter's stack, rather than using a call to **I\_RpcAllocate**.</span></span> <span data-ttu-id="2f8e2-153">Wenn der Wert ungleich 0 (null) ist, wird dieser Wert mit 8 multipliziert, um die Anzahl der Bytes für den Parameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-153">If nonzero, this value is multiplied by 8 to get the number of bytes for the parameter.</span></span> <span data-ttu-id="2f8e2-154">Beachten Sie, dass dies bedeutet, dass mindestens 8 Bytes immer für einen Zeiger zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-154">Note that doing so means at least 8 bytes are always allocated for a pointer.</span></span>
-   <span data-ttu-id="2f8e2-155">Das **isbasetype** -Bit ist für einfache Typen festgelegt, die von der Main [**– OIF**](/windows/desktop/Midl/-oi) -interpreterschleife gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-155">The **IsBasetype** bit is set for simple types that are being marshaled by the main [**–Oif**](/windows/desktop/Midl/-oi) interpreter loop.</span></span> <span data-ttu-id="2f8e2-156">Insbesondere wird ein einfacher Typ mit einem Range-Attribut nicht als Basistyp gekennzeichnet, um das Marshalling der Bereichs Routine durch die Verteilung mit einem FC- \_ Bereichs Token zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-156">In particular, a simple type with a range attribute on it is not flagged as a base type in order to force the range routine marshaling through dispatching using an FC\_RANGE token.</span></span>
-   <span data-ttu-id="2f8e2-157">Das **IsByValue** -Bit ist für Verbund Typen festgelegt, die als Wert gesendet werden, aber nicht für einfache Typen festgelegt sind, unabhängig davon, ob das Argument ein Zeiger ist.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-157">The **IsByValue** bit is set for compound types being sent by value, but is not set for simple types, regardless of whether the argument is a pointer.</span></span> <span data-ttu-id="2f8e2-158">Die Verbund Typen, für die Sie festgelegt ist, sind Strukturen, Unions, über [**tragen \_ als**](/windows/desktop/Midl/transmit-as), [**darstellen \_ als**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) und SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-158">The compound types for which it is set are structures, unions, [**transmit\_as**](/windows/desktop/Midl/transmit-as), [**represent\_as**](/windows/desktop/Midl/represent-as), [**wire\_marshal**](/windows/desktop/Midl/wire-marshal) and SAFEARRAY.</span></span> <span data-ttu-id="2f8e2-159">Im Allgemeinen wurde das-Bit für den Vorteil der hauptinterpreterschleife im [**– Oicf**](/windows/desktop/Midl/-oi) -Interpreter eingeführt, um sicherzustellen, dass die nicht einfachen Argumente (die als Verbund-Typargumente bezeichnet werden) ordnungsgemäß dereferenziert werden.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-159">In general, the bit was introduced for the benefit of the main interpreter loop in the [**–Oicf**](/windows/desktop/Midl/-oi) interpreter, to ensure the nonsimple arguments (referred to as compound type arguments) are properly dereferenced.</span></span> <span data-ttu-id="2f8e2-160">Dieses Bit wurde in früheren Versionen des interpreterers nie verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f8e2-160">This bit was never used in previous versions of the interpreter.</span></span>

 

 