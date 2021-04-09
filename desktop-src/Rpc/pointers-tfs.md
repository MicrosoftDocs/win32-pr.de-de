---
title: Zeiger (RPC)
description: Zeiger
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102651"
---
# <a name="pointers-rpc"></a><span data-ttu-id="1b38b-103">Zeiger (RPC)</span><span class="sxs-lookup"><span data-stu-id="1b38b-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="1b38b-104">Allgemeine Zeiger</span><span class="sxs-lookup"><span data-stu-id="1b38b-104">Common Pointers</span></span>

<span data-ttu-id="1b38b-105">Ein allgemeiner Zeiger ist als alles andere als Schnittstellen Zeiger und Byte Anzahl Zeiger definiert.</span><span class="sxs-lookup"><span data-stu-id="1b38b-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="1b38b-106">Es gibt zwei mögliche Layouts für die Beschreibung:</span><span class="sxs-lookup"><span data-stu-id="1b38b-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="1b38b-107">– oder –</span><span class="sxs-lookup"><span data-stu-id="1b38b-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="1b38b-108">Das erste Format wird verwendet, wenn der Zeiger ein Zeiger auf einen einfachen Typ oder einen Zeichen folgen Zeiger ohne Größenanpassung ist.</span><span class="sxs-lookup"><span data-stu-id="1b38b-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="1b38b-109">Das zweite Format wird für Zeiger auf alle anderen Typen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b38b-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="1b38b-110">Zeiger Attribute geben an, welches Beschreibungs Layout Sie mit dem FC \_ Simple \_ Pointer-Flag hat.</span><span class="sxs-lookup"><span data-stu-id="1b38b-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="1b38b-111">der \_ Zeigertyp<1> einer der folgenden ist.</span><span class="sxs-lookup"><span data-stu-id="1b38b-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="1b38b-112">Zeichen formatieren</span><span class="sxs-lookup"><span data-stu-id="1b38b-112">Format character</span></span> | <span data-ttu-id="1b38b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b38b-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="1b38b-114">FC- \_ RP</span><span class="sxs-lookup"><span data-stu-id="1b38b-114">FC\_RP</span></span>           | <span data-ttu-id="1b38b-115">Ein Verweis Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b38b-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="1b38b-116">FC nach \_ oben</span><span class="sxs-lookup"><span data-stu-id="1b38b-116">FC\_UP</span></span>           | <span data-ttu-id="1b38b-117">Ein eindeutiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b38b-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="1b38b-118">FC \_ fp</span><span class="sxs-lookup"><span data-stu-id="1b38b-118">FC\_FP</span></span>           | <span data-ttu-id="1b38b-119">Ein vollständiger-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b38b-119">A full pointer.</span></span>                          |
| <span data-ttu-id="1b38b-120">FC- \_ op</span><span class="sxs-lookup"><span data-stu-id="1b38b-120">FC\_OP</span></span>           | <span data-ttu-id="1b38b-121">Ein eindeutiger Zeiger in einer Objektschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1b38b-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="1b38b-122">Der Grund für die Unterscheidung von FC \_ op ist Semantik: in Objekt Schnittstellen \[ sollte ein in-, out \] -Zeiger freigegeben werden, bevor ein neues-Objekt gemarshallert und ein neuer Zeiger Wert zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="1b38b-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="1b38b-123">Zeiger \_ Attribute<1> können eines der in der folgenden Tabelle gezeigten Flags aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1b38b-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="1b38b-124">Flag</span><span class="sxs-lookup"><span data-stu-id="1b38b-124">Flag</span></span> | <span data-ttu-id="1b38b-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b38b-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b38b-126">01</span><span class="sxs-lookup"><span data-stu-id="1b38b-126">01</span></span>   | <span data-ttu-id="1b38b-127">FC \_ \_ alle \_ Knoten zuordnen</span><span class="sxs-lookup"><span data-stu-id="1b38b-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="1b38b-128">Der Zeiger ist Teil eines \_ Zuordnungs Schemas (alle Knoten).</span><span class="sxs-lookup"><span data-stu-id="1b38b-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1b38b-129">02</span><span class="sxs-lookup"><span data-stu-id="1b38b-129">02</span></span>   | <span data-ttu-id="1b38b-130">FC \_ nicht \_ kostenlos</span><span class="sxs-lookup"><span data-stu-id="1b38b-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="1b38b-131">Ein Zuordnungs Zeiger (kein \_ freier Zeiger).</span><span class="sxs-lookup"><span data-stu-id="1b38b-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="1b38b-132">04</span><span class="sxs-lookup"><span data-stu-id="1b38b-132">04</span></span>   | <span data-ttu-id="1b38b-133">FC- \_ Zuweisung \_ im \_ Stapel</span><span class="sxs-lookup"><span data-stu-id="1b38b-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="1b38b-134">Ein Zeiger, dessen Referent im Stapel des Stubs zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1b38b-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="1b38b-135">08</span><span class="sxs-lookup"><span data-stu-id="1b38b-135">08</span></span>   | <span data-ttu-id="1b38b-136">einfacher FC- \_ \_ Zeiger</span><span class="sxs-lookup"><span data-stu-id="1b38b-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="1b38b-137">Ein Zeiger auf einen einfachen Typ oder eine konforme Zeichenfolge ohne Größenanpassung.</span><span class="sxs-lookup"><span data-stu-id="1b38b-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="1b38b-138">Dieses Flag, das festgelegt wird, gibt das Layout der Zeiger Beschreibung als einfaches Zeiger Layout an, das oben beschrieben wird. andernfalls wird das deskriptorformat mit dem Offset angegeben.</span><span class="sxs-lookup"><span data-stu-id="1b38b-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="1b38b-139">10</span><span class="sxs-lookup"><span data-stu-id="1b38b-139">10</span></span>   | <span data-ttu-id="1b38b-140">FC- \_ Zeiger- \_ Deref</span><span class="sxs-lookup"><span data-stu-id="1b38b-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="1b38b-141">Ein Zeiger, der dereferenziert werden muss, bevor der Referenten des Zeigers verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="1b38b-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="1b38b-142">Zeiger mit der Größe \_ (), Max \_ ist (), length \_ is (), Last \_ is () und/oder First \_ is (), auf die Sie angewendet werden, haben Format Zeichenfolgen-Beschreibungen, die mit einem Zeiger auf ein Array des entsprechenden Typs identisch sind (z. b. ein konformes Array, wenn Size () \_ \_ und length) \_ angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b38b-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="1b38b-143">Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="1b38b-143">Interface Pointers</span></span>

<span data-ttu-id="1b38b-144">Eine Objekt Schnittstellen Zeiger-Format Zeichenfolge hat eines von zwei Formaten, abhängig davon, ob die entsprechende IID dem Compiler bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="1b38b-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="1b38b-145">Ein Schnittstellen Zeiger mit einer Konstanten IID weist die folgende Beschreibung auf:</span><span class="sxs-lookup"><span data-stu-id="1b38b-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="1b38b-146">Der IID-<16> Teil ist die tatsächliche IID für den Schnittstellen Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b38b-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="1b38b-147">Die IID wird in der Format Zeichenfolge in einem Format geschrieben, das mit der GUID-Datenstruktur identisch ist: Long, Short, Short, Char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="1b38b-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="1b38b-148">Die Beschreibung eines Schnittstellen Zeigers mit IID \_ () wird darauf angewendet:</span><span class="sxs-lookup"><span data-stu-id="1b38b-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="1b38b-149">Der IID \_ -Beschreibungs<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="1b38b-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="1b38b-150">Der von der **ndrcomputeconformance** -Funktion berechnete Wert ist der IID-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b38b-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="1b38b-151">Byte Anzahl Zeiger</span><span class="sxs-lookup"><span data-stu-id="1b38b-151">Byte Count Pointers</span></span>

<span data-ttu-id="1b38b-152">Byte Anzahl Zeiger beziehen sich auf ein spezielles Optimierungs Attribut mit dem Namen \[ **Byte \_ Anzahl** \] .</span><span class="sxs-lookup"><span data-stu-id="1b38b-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="1b38b-153">Die folgenden Formate werden verwendet:</span><span class="sxs-lookup"><span data-stu-id="1b38b-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="1b38b-154">immer</span><span class="sxs-lookup"><span data-stu-id="1b38b-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="1b38b-155">Die Beschreibung der Byte \_ Anzahl \_<> ist ein Korrelations Deskriptor, der abhängig davon, ob [**/robust**](/windows/desktop/Midl/-robust) verwendet wird, 4 oder 6 Bytes hat.</span><span class="sxs-lookup"><span data-stu-id="1b38b-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="1b38b-156">Der pointee- \_ Beschreibungs<> ist eine Beschreibung des pointtyps.</span><span class="sxs-lookup"><span data-stu-id="1b38b-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
