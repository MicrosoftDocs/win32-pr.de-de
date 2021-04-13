---
title: Pipe-Attribut
description: Der pipetypkonstruktor ermöglicht das übertragen eines geöffneten Datenstroms von typisierten Daten über einen Remote Prozedur Aufrufe.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- Pipe-Attribut-Mittel l
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314762"
---
# <a name="pipe-attribute"></a><span data-ttu-id="60e65-104">Pipe-Attribut</span><span class="sxs-lookup"><span data-stu-id="60e65-104">pipe attribute</span></span>

<span data-ttu-id="60e65-105">Der  pipetypkonstruktor ermöglicht das übertragen eines geöffneten Datenstroms von typisierten Daten über einen Remote Prozedur Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="60e65-105">The **pipe** type constructor makes it possible to transmit an open-ended stream of typed data across a remote procedure call.</span></span>

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a><span data-ttu-id="60e65-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60e65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60e65-107">*Elementtyp*</span><span class="sxs-lookup"><span data-stu-id="60e65-107">*element-type*</span></span> 
</dt> <dd>

<span data-ttu-id="60e65-108">Definiert die Größe eines einzelnen Elements im Übertragungs Puffer.</span><span class="sxs-lookup"><span data-stu-id="60e65-108">Defines the size of a single element in the transfer buffer.</span></span> <span data-ttu-id="60e65-109">Der *Elementtyp* kann ein [Basistyp](midl-base-types.md), ein vordefinierter \_ Typ, eine [**Struktur**](struct.md), eine [**32B-Enumeration**](v1-enum.md)oder ein Typbezeichner sein.</span><span class="sxs-lookup"><span data-stu-id="60e65-109">The *element-type* can be a [base type](midl-base-types.md), predefined\_type, [**struct**](struct.md), [**32b enum**](v1-enum.md), or type identifier.</span></span> <span data-ttu-id="60e65-110">Einige Einschränkungen gelten für *Element \_ Typen*, wie in den Hinweisen weiter unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="60e65-110">Several restrictions apply to *element\_types*, as described in Remarks, below.</span></span>

</dd> <dt>

<span data-ttu-id="60e65-111">*Pipe-declarator*</span><span class="sxs-lookup"><span data-stu-id="60e65-111">*pipe-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="60e65-112">Gibt einen oder mehrere Bezeichner oder Zeiger auf Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="60e65-112">Specifies one or more identifiers or pointers to identifiers.</span></span> <span data-ttu-id="60e65-113">Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="60e65-113">Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60e65-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60e65-114">Remarks</span></span>

<span data-ttu-id="60e65-115">Sie **können den** pipetypkonstruktor verwenden, um Daten in beide Richtungen zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="60e65-115">You can use the **pipe** type constructor to transmit data in both directions.</span></span> <span data-ttu-id="60e65-116">Ein **\[** [**in**](in.md) **\]** Pipe-Parameter ermöglicht dem Server das Abrufen des Datenstroms vom Client während eines Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="60e65-116">An **\[**[**in**](in.md)**\]** pipe parameter allows the server to pull the data stream from the client during a remote procedure call.</span></span> <span data-ttu-id="60e65-117">Ein **\[** [**out**](out-idl.md) - **\]** Pipe-Parameter ermöglicht es dem Server, den Datenstrom an den Client zurückzusenden.</span><span class="sxs-lookup"><span data-stu-id="60e65-117">An **\[**[**out**](out-idl.md)**\]** pipe parameter allows the server to push the data stream back to the client.</span></span> <span data-ttu-id="60e65-118">Sie stellen die Client seitigen Routinen bereit, um den Datenstream per Push und Pull abzurufen und einen globalen Puffer für die Daten zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="60e65-118">You supply the client-side routines to push and pull the data stream and to allocate a global buffer for the data.</span></span> <span data-ttu-id="60e65-119">Die Client-und Serverstub-Routinen Mars Hallen und entsperren Daten und übergeben einen Verweis auf den Puffer zurück an die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="60e65-119">The client and server stub routines marshal and unmarshal data and pass a reference to the buffer back to the application.</span></span>

<span data-ttu-id="60e65-120">Für Pipes gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="60e65-120">The following restrictions apply to pipes:</span></span>

-   <span data-ttu-id="60e65-121">Ein Pipe-Element darf weder einen Zeiger, ein konformes-Array noch ein unterschiedliches Array, ein Handle oder ein Kontext Handle enthalten.</span><span class="sxs-lookup"><span data-stu-id="60e65-121">A pipe element cannot be or contain a pointer, a conformant or varying array, a handle, or a context handle.</span></span> <span data-ttu-id="60e65-122">Außerdem kann ein Pipe-Element in der Microsoft-Implementierung von Pipes weder eine [**Union**](union.md), eine [**16B-Enumeration**](enum.md)noch eine [**\_ \_ int3264**](--int3264.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="60e65-122">Also, in the Microsoft implementation of pipes, a pipe element cannot be or contain a [**union**](union.md), a [**16b enum**](enum.md), or an [**\_\_int3264**](--int3264.md).</span></span>
-   <span data-ttu-id="60e65-123">Die Attribute "über **\[** [**Tragung \_ als**](transmit-as.md)", " **\]** **\[** [**darstellen \_ als**](represent-as.md)" **\]** , " **\[** [**Wire \_ Marshal**](wire-marshal.md)" oder " **\]** **\[** [**User \_ Marshal**](user-marshal.md) " können nicht **\]** auf einen Pipetyp oder auf den *Elementtyp* angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e65-123">You cannot apply the **\[**[**transmit\_as**](transmit-as.md)**\]**, **\[**[**represent\_as**](represent-as.md)**\]**, **\[**[**wire\_marshal**](wire-marshal.md)**\]**, or **\[**[**user\_marshal**](user-marshal.md)**\]** attributes to a pipe type or to the *element-type*.</span></span>
-   <span data-ttu-id="60e65-124">Ein Pipetyp kann kein Member einer Struktur oder Union, des Ziels eines Zeigers oder des Basistyps eines Arrays sein.</span><span class="sxs-lookup"><span data-stu-id="60e65-124">A pipe type cannot be a member of a structure or union, the target of a pointer, or the base type of an array.</span></span>
-   <span data-ttu-id="60e65-125">Ein als Pipetyp deklarierter Datentyp kann nur als Parameter eines Remote Aufrufes verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e65-125">A data type declared to be a pipe type can only be used as a parameter of a remote call.</span></span>
-   <span data-ttu-id="60e65-126">Sie können einen Pipe-Parameter in beide Richtungen als Wert oder als Verweis übergeben **\[** [**(Verweis**](ref.md) **\]** Zeiger).</span><span class="sxs-lookup"><span data-stu-id="60e65-126">You can pass a pipe parameter in either direction by value or by reference (**\[**[**ref**](ref.md)**\]** pointer).</span></span> <span data-ttu-id="60e65-127">Allerdings können Sie das **\[** [**ptr**](ptr.md) - **\]** Attribut nicht auf eine Pipe anwenden, die als Verweis übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="60e65-127">However you cannot apply the **\[**[**ptr**](ptr.md)**\]** attribute to a pipe that is passed by reference.</span></span> <span data-ttu-id="60e65-128">Es ist nicht möglich, einen Pipe-Parameter mit einem **\[** [**eindeutigen**](unique.md) **\]** oder einem vollständigen Zeiger anzugeben, unabhängig von der Richtung.</span><span class="sxs-lookup"><span data-stu-id="60e65-128">You cannot specify a pipe parameter with a **\[**[**unique**](unique.md)**\]** or a full pointer, regardless of direction.</span></span>
-   <span data-ttu-id="60e65-129">Pipes können nicht in **\[** [**Objekt**](object.md) **\]** Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60e65-129">You cannot use pipes in **\[**[**object**](object.md)**\]** interfaces.</span></span>
-   <span data-ttu-id="60e65-130">Sie können das **\[** [**idempotente**](idempotent.md) - **\]** Attribut nicht auf eine Routine anwenden, die über einen Pipe-Parameter verfügt.</span><span class="sxs-lookup"><span data-stu-id="60e65-130">You cannot apply the **\[**[**idempotent**](idempotent.md)**\]** attribute to a routine that has a pipe parameter.</span></span>
-   <span data-ttu-id="60e65-131">Sie können die Serialisierungsattribute nicht verwenden, **\[** [**Codieren**](encode.md) **\]** und **\[** mit Pipes [**decodieren**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="60e65-131">You cannot use the serialization attributes, **\[**[**encode**](encode.md)**\]** and **\[**[**decode**](decode.md)**\]** with pipes.</span></span>
-   <span data-ttu-id="60e65-132">Sie können automatische Handles weder standardmäßig noch mit dem **\[** [**Auto \_ handle**](auto-handle.md) - **\]** Attribut mit Pipes verwenden.</span><span class="sxs-lookup"><span data-stu-id="60e65-132">You cannot use automatic handles, either by default, or with the **\[**[**auto\_handle**](auto-handle.md)**\]** attribute, with pipes.</span></span>

> [!Note]  
> <span data-ttu-id="60e65-133">Der mittlerer l-Compiler unterstützt Pipes nur im [**/OIF**](-oi.md) -Modus.</span><span class="sxs-lookup"><span data-stu-id="60e65-133">The MIDL compiler supports pipes in [**/Oif**](-oi.md) mode only.</span></span>

 

<span data-ttu-id="60e65-134">Weitere Informationen zum Implementieren von Routinen mit Pipe-Parametern finden Sie unter [Pipes](/windows/desktop/Rpc/pipes) im RPC-Programmier Handbuch und in der Referenz.</span><span class="sxs-lookup"><span data-stu-id="60e65-134">For more information on implementing routines with pipe parameters, see [Pipes](/windows/desktop/Rpc/pipes) in the RPC Programmer's Guide and Reference.</span></span>

## <a name="examples"></a><span data-ttu-id="60e65-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60e65-135">Examples</span></span>

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a><span data-ttu-id="60e65-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="60e65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e65-137">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="60e65-137">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="60e65-138">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="60e65-138">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="60e65-139">**Decodieren**</span><span class="sxs-lookup"><span data-stu-id="60e65-139">**decode**</span></span>](decode.md)
</dt> <dt>

[<span data-ttu-id="60e65-140">**Codieren**</span><span class="sxs-lookup"><span data-stu-id="60e65-140">**encode**</span></span>](encode.md)
</dt> <dt>

[<span data-ttu-id="60e65-141">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="60e65-141">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="60e65-142">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="60e65-142">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="60e65-143">**in**</span><span class="sxs-lookup"><span data-stu-id="60e65-143">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="60e65-144">**Objekt (object)**</span><span class="sxs-lookup"><span data-stu-id="60e65-144">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="60e65-145">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="60e65-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="60e65-146">**ptr**</span><span class="sxs-lookup"><span data-stu-id="60e65-146">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="60e65-147">**ref**</span><span class="sxs-lookup"><span data-stu-id="60e65-147">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="60e65-148">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="60e65-148">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="60e65-149">**struct**</span><span class="sxs-lookup"><span data-stu-id="60e65-149">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="60e65-150">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="60e65-150">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="60e65-151">**gem**</span><span class="sxs-lookup"><span data-stu-id="60e65-151">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="60e65-152">**Benutzer \_ Mars Hall**</span><span class="sxs-lookup"><span data-stu-id="60e65-152">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="60e65-153">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="60e65-153">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> </dl>

 

 