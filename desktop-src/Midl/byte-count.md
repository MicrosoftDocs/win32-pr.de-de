---
title: byte_count-Attribut
description: Das Attribut \ Byte \_ count \ ACF ist ein Parameter Attribut, das eine Größe (in Bytes) mit dem durch den Zeiger gekennzeichneten Speicherbereich verknüpft.
ms.assetid: 7e146888-fe7c-461c-8615-70da1e3b12cd
keywords:
- byte_count Attribut-Mittel l
topic_type:
- apiref
api_name:
- byte_count
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d82d34a60ea736d10c8ec5ee8a001370c6b64c6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312851"
---
# <a name="byte_count-attribute"></a><span data-ttu-id="37132-104">Byte \_ Anzahl Attribut</span><span class="sxs-lookup"><span data-stu-id="37132-104">byte\_count attribute</span></span>

<span data-ttu-id="37132-105">Das ACF-Attribut **\[ Byte \_ Count \]** ist ein Parameter Attribut, das eine Größe (in Bytes) mit dem durch den Zeiger gekennzeichneten Speicherbereich verknüpft.</span><span class="sxs-lookup"><span data-stu-id="37132-105">The **\[byte\_count\]** ACF attribute is a parameter attribute that associates a size, in bytes, with the memory area indicated by the pointer.</span></span>

``` syntax
[ function-attribute-list ] function-name(
    [byte_count(length-variable-name)] parameter-name);
    ...);
```

## <a name="parameters"></a><span data-ttu-id="37132-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="37132-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37132-107">*Function-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="37132-107">*function-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="37132-108">Gibt 0 (null) oder mehr ACF-Funktions Attribute an.</span><span class="sxs-lookup"><span data-stu-id="37132-108">Specifies zero or more ACF function attributes.</span></span>

</dd> <dt>

<span data-ttu-id="37132-109">*function-name*</span><span class="sxs-lookup"><span data-stu-id="37132-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="37132-110">Gibt den Namen der Funktion an, die in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="37132-110">Specifies the name of the function defined in the IDL file.</span></span> <span data-ttu-id="37132-111">Der Funktionsname ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="37132-111">The function name is required.</span></span>

</dd> <dt>

<span data-ttu-id="37132-112">*Length-Variable-Name*</span><span class="sxs-lookup"><span data-stu-id="37132-112">*length-variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="37132-113">Gibt den Namen des [**\[ \] reinen Parameters an,**](in.md)der die Größe (in Bytes) des Speicherbereichs angibt, auf den durch *Parameter Name* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="37132-113">Specifies the name of the [**\[in\]**](in.md)-only parameter that specifies the size, in bytes, of the memory area referenced by *parameter-name*.</span></span>

</dd> <dt>

<span data-ttu-id="37132-114">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="37132-114">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="37132-115">Gibt den Namen des reinen Zeiger Parameters an [**\[ , \]**](out-idl.md)der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="37132-115">Specifies the name of the [**\[out\]**](out-idl.md)-only pointer parameter defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37132-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37132-116">Remarks</span></span>

<span data-ttu-id="37132-117">Die **\[ Byte \_ Anzahl \]** der ACF-Attribute stellt eine Microsoft-Erweiterung für DCE-IDL dar.</span><span class="sxs-lookup"><span data-stu-id="37132-117">The ACF attribute **\[byte\_count\]** represents a Microsoft extension to DCE IDL.</span></span> <span data-ttu-id="37132-118">Daher ist dieses Attribut nicht verfügbar, wenn Sie den Mittelwert-Compilerschalter [**/OSF**](-osf.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="37132-118">Therefore, this attribute is not available when you use the MIDL compiler switch [**/osf**](-osf.md).</span></span>

> [!Note]  
> <span data-ttu-id="37132-119">Das **\[ Byte Count \]** -Attribut wird in der NDR64-Syntax nicht mehr unterstützt, da die für alle [**\[ out \]**](out-idl.md) -Parameter erforderliche Größe nicht zu schätzen ist.</span><span class="sxs-lookup"><span data-stu-id="37132-119">The **\[byte count\]** attribute is no longer supported in NDR64 syntax due to the difficulty in estimating the size required for all [**\[out\]**](out-idl.md) parameters.</span></span>

 

<span data-ttu-id="37132-120">Der Arbeitsspeicher, auf den der Zeiger Parameter verweist, ist zusammenhängend und wird nicht von den Client-stubden zugewiesen oder freigegeben.</span><span class="sxs-lookup"><span data-stu-id="37132-120">Memory referenced by the pointer parameter is contiguous and is not allocated or freed by the client stubs.</span></span> <span data-ttu-id="37132-121">Mit dieser Funktion des **\[ Byte \_ Count \]** -Attributs können Sie einen persistenten Pufferbereich im Client Speicher erstellen, der bei mehr als einem Remote Prozedur Abruf wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="37132-121">This feature of the **\[byte\_count\]** attribute lets you create a persistent buffer area in client memory that can be reused during more than one call to the remote procedure.</span></span>

<span data-ttu-id="37132-122">Durch die Möglichkeit, die Speicher Belegung für den Client-Stub zu deaktivieren, können Sie die Anwendung auf Effizienz optimieren.</span><span class="sxs-lookup"><span data-stu-id="37132-122">The ability to turn off the client stub memory allocation lets you tune the application for efficiency.</span></span> <span data-ttu-id="37132-123">Beispielsweise kann das **\[ Byte \_ Count \]** -Attribut von Dienstanbieter Funktionen verwendet werden, die Microsoft RPC verwenden.</span><span class="sxs-lookup"><span data-stu-id="37132-123">For example, the **\[byte\_count\]** attribute can be used by service-provider functions that use Microsoft RPC.</span></span> <span data-ttu-id="37132-124">Wenn eine Benutzeranwendung die Dienstanbieter-API aufruft und einen Zeiger an einen Puffer sendet, kann der Dienstanbieter den Puffer Zeiger an die Remote Funktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="37132-124">When a user application calls the service-provider API and sends a pointer to a buffer, the service provider can pass the buffer pointer on to the remote function.</span></span> <span data-ttu-id="37132-125">Der Dienstanbieter kann den Puffer bei mehreren Remote aufrufen wieder verwenden, ohne den Benutzer zu zwingen, den Speicherbereich neu zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="37132-125">The service provider can reuse the buffer during multiple remote calls without forcing the user to reallocate the memory area.</span></span>

<span data-ttu-id="37132-126">Der Arbeitsspeicher Bereich kann komplexe Datenstrukturen enthalten, die aus mehreren Zeigern bestehen.</span><span class="sxs-lookup"><span data-stu-id="37132-126">The memory area can contain complex data structures that consist of multiple pointers.</span></span> <span data-ttu-id="37132-127">Da der Speicherbereich zusammenhängend ist, muss die Anwendung nicht mehrere Aufrufe durchführen, um jeden Zeiger und jede Struktur einzeln freizugeben.</span><span class="sxs-lookup"><span data-stu-id="37132-127">Because the memory area is contiguous, the application does not have to make several calls to individually free each pointer and structure.</span></span> <span data-ttu-id="37132-128">Stattdessen kann der Speicherbereich mit einem Rückruf der Speicher Belegung oder der kostenlosen Routine zugeordnet oder freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="37132-128">Instead, it can allocate or free the memory area with one call to the memory allocation or free routine.</span></span>

<span data-ttu-id="37132-129">Bei dem Puffer muss es sich um einen reinen [**\[ out \]**](out-idl.md)-Parameter handeln, während die Pufferlänge in [**\[ \] Byte einen reinen**](in.md)Parameter aufweisen muss.</span><span class="sxs-lookup"><span data-stu-id="37132-129">The buffer must be an [**\[out\]**](out-idl.md)-only parameter, while the buffer length in bytes must be an [**\[in\]**](in.md)-only parameter.</span></span>

<span data-ttu-id="37132-130">Geben Sie einen Puffer an, der groß genug ist, um alle [**\[ out \]**](out-idl.md) -Parameter zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="37132-130">Specify a buffer that is large enough to contain all the [**\[out\]**](out-idl.md) parameters.</span></span> <span data-ttu-id="37132-131">Verwenden Sie wegen ausgeblendeter Auffüll Zeichen anstelle von exakten Anzahlen eine Überschätzung.</span><span class="sxs-lookup"><span data-stu-id="37132-131">Because of hidden padding, use overestimates rather than exact counts.</span></span> <span data-ttu-id="37132-132">Beispielsweise werden 4-Byte-Zeiger auf eine 4-Byte-Ausrichtung auf 32-Bit-Plattformen und 8-Byte-Zeiger auf eine 8-Byte-Grenze auf 64-Bit-Plattformen gemarshallt.</span><span class="sxs-lookup"><span data-stu-id="37132-132">For example, 4-byte pointers are unmarshaled on a 4-byte aligned boundary on 32-bit platforms and 8-byte pointers on an 8-byte boundary on 64-bit platforms.</span></span> <span data-ttu-id="37132-133">Daher muss die Ausrichtungs Auffüllung, die die stubvorgänge ausführen, im Speicherplatz für den Puffer berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="37132-133">Therefore, the alignment padding the stubs will perform must be accounted for in the space for the buffer.</span></span> <span data-ttu-id="37132-134">Außerdem können die während der Kompilierung der C-Sprache verwendeten Verpackungs Ebenen variieren.</span><span class="sxs-lookup"><span data-stu-id="37132-134">In addition, packing levels used during C-language compilation can vary.</span></span> <span data-ttu-id="37132-135">Verwenden Sie einen Byte Zählerwert, der zusätzliche Komprimierungs Bytes für den während der Kompilierung in der C-Sprache verwendeten Verpackungs Grad berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="37132-135">Use a byte count value that accounts for additional packing bytes added for the packing level used during C-language compilation.</span></span> <span data-ttu-id="37132-136">Ein sicheres Verfahren, das sowohl 32-Bit-als auch 64-Bit-Plattformen abdeckt, besteht darin, dass jedes Objekt, das in den großen Speicherblock geht, an einer Adresse beginnt, die ein Vielfaches von 8 ist.</span><span class="sxs-lookup"><span data-stu-id="37132-136">A safe practice that covers both 32 bit platforms and 64 bit platforms is to assume that each object going into the big memory block starts at an address that is a multiple of 8.</span></span>

## <a name="examples"></a><span data-ttu-id="37132-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37132-137">Examples</span></span>

``` syntax
/* IDL file */ 
HRESULT proc1([in] unsigned long length, 
              [out] struct my_struct * pMyStruct); 
 
/* ACF file */ 
proc1([byte_count(length)] pMyStruct);
```

## <a name="see-also"></a><span data-ttu-id="37132-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="37132-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37132-139">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="37132-139">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="37132-140">**in**</span><span class="sxs-lookup"><span data-stu-id="37132-140">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="37132-141">**Länge \_ ist**</span><span class="sxs-lookup"><span data-stu-id="37132-141">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="37132-142">**/osf**</span><span class="sxs-lookup"><span data-stu-id="37132-142">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="37132-143">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="37132-143">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="37132-144">**Größe \_ :**</span><span class="sxs-lookup"><span data-stu-id="37132-144">**size\_is**</span></span>](size-is.md)
</dt> </dl>

 

 




