---
title: Zeiger (RPC)
description: Erfahren Sie mehr über einen allgemeinen RPC-Zeiger, der als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert ist.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119705"
---
# <a name="pointers-rpc"></a><span data-ttu-id="dcbf2-103">Zeiger (RPC)</span><span class="sxs-lookup"><span data-stu-id="dcbf2-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="dcbf2-104">Allgemeine Zeiger</span><span class="sxs-lookup"><span data-stu-id="dcbf2-104">Common Pointers</span></span>

<span data-ttu-id="dcbf2-105">Ein allgemeiner Zeiger wird als alles andere als Schnittstellenzeiger und Byteanzahlzeiger definiert.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="dcbf2-106">Es gibt zwei mögliche Layouts für die Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="dcbf2-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="dcbf2-107">– oder –</span><span class="sxs-lookup"><span data-stu-id="dcbf2-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="dcbf2-108">Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder ein nicht formatierter Zeichenfolgenzeiger ist.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="dcbf2-109">Das zweite Format wird für Zeiger auf alle anderen Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="dcbf2-110">Zeigerattribute geben das Beschreibungslayout mit dem FC \_ SIMPLE \_ POINTER-Flag an.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="dcbf2-111">Zeigertyp \_<1> ist einer der folgenden.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="dcbf2-112">Formatieren eines Zeichens</span><span class="sxs-lookup"><span data-stu-id="dcbf2-112">Format character</span></span> | <span data-ttu-id="dcbf2-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcbf2-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="dcbf2-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="dcbf2-114">FC\_RP</span></span>           | <span data-ttu-id="dcbf2-115">Ein Verweiszeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="dcbf2-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="dcbf2-116">FC\_UP</span></span>           | <span data-ttu-id="dcbf2-117">Ein eindeutiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="dcbf2-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="dcbf2-118">FC\_FP</span></span>           | <span data-ttu-id="dcbf2-119">Ein vollständiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-119">A full pointer.</span></span>                          |
| <span data-ttu-id="dcbf2-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="dcbf2-120">FC\_OP</span></span>           | <span data-ttu-id="dcbf2-121">Ein eindeutiger Zeiger in einer Objektschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="dcbf2-122">Der Grund für die Unterscheidung von FC \_ OP ist semantisch: In Objektschnittstellen sollte ein \[ In-Out-Zeiger freigegeben werden, bevor ein neues Objekt aus dem \] Smarshaling gemacht und ein neuer Zeigerwert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="dcbf2-123">Zeigerattribute \_<1> können über eines der in der folgenden Tabelle gezeigten Flags verfügen.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="dcbf2-124">attribute</span><span class="sxs-lookup"><span data-stu-id="dcbf2-124">Attribute</span></span> | <span data-ttu-id="dcbf2-125">Flag</span><span class="sxs-lookup"><span data-stu-id="dcbf2-125">Flag</span></span>              | <span data-ttu-id="dcbf2-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dcbf2-126">Description</span></span>                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcbf2-127">01</span><span class="sxs-lookup"><span data-stu-id="dcbf2-127">01</span></span>   | <span data-ttu-id="dcbf2-128">FC \_ ORDNET \_ ALLE KNOTEN ZU \_</span><span class="sxs-lookup"><span data-stu-id="dcbf2-128">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="dcbf2-129">Der Zeiger ist Teil eines \_ Zuordnungsschemas allocate(all nodes).</span><span class="sxs-lookup"><span data-stu-id="dcbf2-129">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="dcbf2-130">02</span><span class="sxs-lookup"><span data-stu-id="dcbf2-130">02</span></span>   | <span data-ttu-id="dcbf2-131">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="dcbf2-131">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="dcbf2-132">Ein allocate(don't \_ free)-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-132">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="dcbf2-133">04</span><span class="sxs-lookup"><span data-stu-id="dcbf2-133">04</span></span>   | <span data-ttu-id="dcbf2-134">FC \_ ALLOCED \_ ON \_ STACK</span><span class="sxs-lookup"><span data-stu-id="dcbf2-134">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="dcbf2-135">Ein Zeiger, dessen Referenz auf dem Stapel des Stubs zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-135">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="dcbf2-136">08</span><span class="sxs-lookup"><span data-stu-id="dcbf2-136">08</span></span>   | <span data-ttu-id="dcbf2-137">FC \_ SIMPLE \_ POINTER</span><span class="sxs-lookup"><span data-stu-id="dcbf2-137">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="dcbf2-138">Ein Zeiger auf einen einfachen Typ oder eine nicht konforme Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-138">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="dcbf2-139">Dieses Flag, das festgelegt wird, gibt das Layout der Zeigerbeschreibung wie das oben beschriebene einfache Zeigerlayout an, andernfalls wird das Deskriptorformat mit dem Offset angegeben.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-139">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="dcbf2-140">10</span><span class="sxs-lookup"><span data-stu-id="dcbf2-140">10</span></span>   | <span data-ttu-id="dcbf2-141">FC \_ POINTER \_ DEREF</span><span class="sxs-lookup"><span data-stu-id="dcbf2-141">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="dcbf2-142">Ein Zeiger, der dereferenziert werden muss, bevor der Verweis des Zeigers verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-142">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="dcbf2-143">Zeiger mit der Größe \_ is(), max \_ is(), length \_ is(), last \_ is() und/oder first \_ is() verfügen über Formatzeichenfolgenbeschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs identisch sind (z. B. ein konformes Array, wenn size \_ is() angewendet wird, ein konformes, variierendes Array, wenn \_ size() und length \_ angewendet werden).</span><span class="sxs-lookup"><span data-stu-id="dcbf2-143">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="dcbf2-144">Schnittstellenzeiger</span><span class="sxs-lookup"><span data-stu-id="dcbf2-144">Interface Pointers</span></span>

<span data-ttu-id="dcbf2-145">Eine Objektschnittstellenzeigerformatzeichenfolge weist eines von zwei Formaten auf, je nachdem, ob dem Compiler die entsprechende IID bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-145">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="dcbf2-146">Ein Schnittstellenzeiger mit einer konstanten IID weist die folgende Beschreibung auf:</span><span class="sxs-lookup"><span data-stu-id="dcbf2-146">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="dcbf2-147">Der iid<16> Teil ist die tatsächliche IID für den Schnittstellenzeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-147">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="dcbf2-148">Die iid wird in die Formatzeichenfolge in einem Format geschrieben, das mit der GUID-Datenstruktur identisch ist: long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="dcbf2-148">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="dcbf2-149">Die Beschreibung eines Schnittstellenzeigers, auf den iid \_ is() angewendet wird, lautet:</span><span class="sxs-lookup"><span data-stu-id="dcbf2-149">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="dcbf2-150">Die \_ iid-Beschreibung<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-150">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="dcbf2-151">Der von der **NdrComputeConformance-Funktion** berechnete Wert ist der IID-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-151">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="dcbf2-152">Byteanzahlzeiger</span><span class="sxs-lookup"><span data-stu-id="dcbf2-152">Byte Count Pointers</span></span>

<span data-ttu-id="dcbf2-153">Byteanzahlzeiger beziehen sich auf ein spezielles Optimierungsattribut namens \[ **\_ Byteanzahl.** \]</span><span class="sxs-lookup"><span data-stu-id="dcbf2-153">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="dcbf2-154">Die folgenden Formate werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="dcbf2-154">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="dcbf2-155">–und –</span><span class="sxs-lookup"><span data-stu-id="dcbf2-155">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="dcbf2-156">Die \_ \_ Byteanzahlbeschreibung<> ist ein Korrelationsdeskriptor und hat 4 oder 6 Bytes, je nachdem, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-156">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="dcbf2-157">Die \_ Pointee-Beschreibung<> ist eine Beschreibung des Pointee-Typs.</span><span class="sxs-lookup"><span data-stu-id="dcbf2-157">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
