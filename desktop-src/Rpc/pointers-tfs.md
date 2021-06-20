---
title: Zeiger (RPC)
description: Erfahren Sie mehr über einen allgemeinen RPC-Zeiger, der als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert ist.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e41a0b6208745b543a9efe2fe22ab090046778
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406593"
---
# <a name="pointers-rpc"></a><span data-ttu-id="83f12-103">Zeiger (RPC)</span><span class="sxs-lookup"><span data-stu-id="83f12-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="83f12-104">Allgemeine Zeiger</span><span class="sxs-lookup"><span data-stu-id="83f12-104">Common Pointers</span></span>

<span data-ttu-id="83f12-105">Ein gängiger Zeiger wird als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert.</span><span class="sxs-lookup"><span data-stu-id="83f12-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="83f12-106">Es gibt zwei mögliche Layouts für die Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="83f12-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="83f12-107">– oder –</span><span class="sxs-lookup"><span data-stu-id="83f12-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="83f12-108">Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder einen nicht großen Zeichenfolgenzeiger ist.</span><span class="sxs-lookup"><span data-stu-id="83f12-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="83f12-109">Das zweite Format wird für Zeiger auf alle anderen Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="83f12-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="83f12-110">Zeigerattribute geben mit dem FC SIMPLE POINTER-Flag an, welches \_ \_ Beschreibungslayout es ist.</span><span class="sxs-lookup"><span data-stu-id="83f12-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="83f12-111">Zeigertyp \_<1> ist einer der folgenden.</span><span class="sxs-lookup"><span data-stu-id="83f12-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="83f12-112">Formatzeichen</span><span class="sxs-lookup"><span data-stu-id="83f12-112">Format character</span></span> | <span data-ttu-id="83f12-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83f12-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="83f12-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="83f12-114">FC\_RP</span></span>           | <span data-ttu-id="83f12-115">Ein Verweiszeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="83f12-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="83f12-116">FC\_UP</span></span>           | <span data-ttu-id="83f12-117">Ein eindeutiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="83f12-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="83f12-118">FC\_FP</span></span>           | <span data-ttu-id="83f12-119">Ein vollständiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-119">A full pointer.</span></span>                          |
| <span data-ttu-id="83f12-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="83f12-120">FC\_OP</span></span>           | <span data-ttu-id="83f12-121">Ein eindeutiger Zeiger in einer Objektschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="83f12-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="83f12-122">Der Grund für die Unterscheidung von FC OP ist semantisch: In Objektschnittstellen sollte ein in,out-Zeiger frei werden, bevor die Zuordnung eines neuen Objekts und das Zuweisen eines neuen Zeigerwerts entschniffen \_ \[ \] wird.</span><span class="sxs-lookup"><span data-stu-id="83f12-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="83f12-123">Zeigerattribute<1> können über eines der in der folgenden \_ Tabelle gezeigten Flags verfügen.</span><span class="sxs-lookup"><span data-stu-id="83f12-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="83f12-124">Flag</span><span class="sxs-lookup"><span data-stu-id="83f12-124">Flag</span></span> | <span data-ttu-id="83f12-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83f12-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83f12-126">01</span><span class="sxs-lookup"><span data-stu-id="83f12-126">01</span></span>   | <span data-ttu-id="83f12-127">FC \_ ALLOCATE \_ ALL \_ NODES</span><span class="sxs-lookup"><span data-stu-id="83f12-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="83f12-128">Der Zeiger ist Teil eines Zuordnungsschemas für "allocate(alle \_ Knoten)".</span><span class="sxs-lookup"><span data-stu-id="83f12-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="83f12-129">02</span><span class="sxs-lookup"><span data-stu-id="83f12-129">02</span></span>   | <span data-ttu-id="83f12-130">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="83f12-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="83f12-131">Ein allocate(don't \_ free)-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="83f12-132">04</span><span class="sxs-lookup"><span data-stu-id="83f12-132">04</span></span>   | <span data-ttu-id="83f12-133">FC \_ ALLOCED \_ ON \_ STACK</span><span class="sxs-lookup"><span data-stu-id="83f12-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="83f12-134">Ein Zeiger, dessen Referenz auf dem Stapel des Stubs zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83f12-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="83f12-135">08</span><span class="sxs-lookup"><span data-stu-id="83f12-135">08</span></span>   | <span data-ttu-id="83f12-136">EINFACHER \_ \_ FC-ZEIGER</span><span class="sxs-lookup"><span data-stu-id="83f12-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="83f12-137">Ein Zeiger auf einen einfachen Typ oder eine nicht konforme Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="83f12-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="83f12-138">Dieses Flag, das festgelegt wird, gibt das Layout der Zeigerbeschreibung als das oben beschriebene einfache Zeigerlayout an, andernfalls wird das Deskriptorformat mit dem Offset angegeben.</span><span class="sxs-lookup"><span data-stu-id="83f12-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="83f12-139">10</span><span class="sxs-lookup"><span data-stu-id="83f12-139">10</span></span>   | <span data-ttu-id="83f12-140">\_ \_ FC-ZEIGER-DEREF</span><span class="sxs-lookup"><span data-stu-id="83f12-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="83f12-141">Ein Zeiger, der dereferenziert werden muss, bevor der Zeigerreferenzierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83f12-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="83f12-142">Zeiger, auf die die Größe \_ is(), max \_ is(), length \_ is(), last \_ is() und/oder first \_ is() angewendet \_ \_ werden, verfügen über Formatzeichenfolgenbeschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs \_ identisch sind (z. B. ein konformes Array, wenn size is() angewendet wird, ein konformes variierende Array, wenn size () und length angewendet werden).</span><span class="sxs-lookup"><span data-stu-id="83f12-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="83f12-143">Schnittstellenzeker</span><span class="sxs-lookup"><span data-stu-id="83f12-143">Interface Pointers</span></span>

<span data-ttu-id="83f12-144">Eine Objektschnittstellenzeiger-Formatzeichenfolge hat eines von zwei Formaten, je nachdem, ob die entsprechende IID dem Compiler bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="83f12-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="83f12-145">Ein Schnittstellenzeiger mit einer konstanten IID hat die folgende Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="83f12-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="83f12-146">Der iid<16> ist die tatsächliche IID für den Schnittstellenzeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="83f12-147">Die IID wird in einem Format, das mit der GUID-Datenstruktur identisch ist, in die Formatzeichenfolge geschrieben: long, short, short, char \[ \] 8.</span><span class="sxs-lookup"><span data-stu-id="83f12-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="83f12-148">Die Beschreibung eines Schnittstellenzeigers, auf den iid \_ is() angewendet wird, ist:</span><span class="sxs-lookup"><span data-stu-id="83f12-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="83f12-149">Die iid description<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="83f12-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="83f12-150">Der von der **NdrComputeConformance-Funktion** berechnete Wert ist der IID-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="83f12-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="83f12-151">Zeiger auf die Byteanzahl</span><span class="sxs-lookup"><span data-stu-id="83f12-151">Byte Count Pointers</span></span>

<span data-ttu-id="83f12-152">Byteanzahlze zeiger beziehen sich auf ein spezielles Optimierungsattribut namens \[ **\_ Byteanzahl.** \]</span><span class="sxs-lookup"><span data-stu-id="83f12-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="83f12-153">Die folgenden Formate werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="83f12-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="83f12-154">– und –</span><span class="sxs-lookup"><span data-stu-id="83f12-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="83f12-155">Die Beschreibung der Byteanzahl<> korrelationsdeskriptor und hat je nachdem, ob \_ \_ [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes.</span><span class="sxs-lookup"><span data-stu-id="83f12-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="83f12-156">Die Zeigerbeschreibung \_<> eine Beschreibung des Zeigertyps.</span><span class="sxs-lookup"><span data-stu-id="83f12-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
