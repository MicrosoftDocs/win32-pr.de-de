---
title: Attribut zuordnen
description: Mit dem Attribut \ zuordnen \ ACF können Sie die Speicher Belegung und die Freigabe Zuordnung für einen Typ anpassen, der in der IDL-Datei definiert ist.
ms.assetid: 1956b11f-bafa-41c3-9025-5fcbb890d1a2
keywords:
- Attribut-Mittel l zuordnen
topic_type:
- apiref
api_name:
- allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff902e34e07ebd34edcb73797baa131eec8b222
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857271"
---
# <a name="allocate-attribute"></a><span data-ttu-id="3d655-104">Attribut zuordnen</span><span class="sxs-lookup"><span data-stu-id="3d655-104">allocate attribute</span></span>

<span data-ttu-id="3d655-105">Mit dem Attribut " **\[ zuordnen \]** von ACF" können Sie die Speicher Belegung und die Zuordnung für einen in der IDL-Datei definierten Typ anpassen.</span><span class="sxs-lookup"><span data-stu-id="3d655-105">The **\[allocate\]** ACF attribute lets you customize memory allocation and deallocation for a type defined in the IDL file.</span></span>

``` syntax
typedef [allocate (allocate-option-list) [, type-attribute-list] ] type-name;
```

## <a name="parameters"></a><span data-ttu-id="3d655-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d655-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d655-107">*zuordnen-Option-List*</span><span class="sxs-lookup"><span data-stu-id="3d655-107">*allocate-option-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d655-108">Gibt eine oder mehrere Speicher Belegungs Optionen an.</span><span class="sxs-lookup"><span data-stu-id="3d655-108">Specifies one or more memory-allocation options.</span></span> <span data-ttu-id="3d655-109">Wählen Sie entweder einen **einzelnen \_ Knoten** oder **alle \_ Knoten** aus, oder wählen Sie entweder " **frei** " oder " **nicht \_ frei**" oder eines der Paare aus.</span><span class="sxs-lookup"><span data-stu-id="3d655-109">Select one of either **single\_node** or **all\_nodes**, or one of either **free** or **dont\_free**, or one from each pair.</span></span> <span data-ttu-id="3d655-110">Wenn Sie mehr als eine Option angeben, trennen Sie die Optionen durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="3d655-110">When you specify more than one option, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3d655-111">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="3d655-111">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3d655-112">Gibt andere optionale ACF-Typattribute an.</span><span class="sxs-lookup"><span data-stu-id="3d655-112">Specifies other optional ACF-type attributes.</span></span> <span data-ttu-id="3d655-113">Wenn Sie mehr als ein Type-Attribut angeben, trennen Sie die Optionen durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="3d655-113">When you specify more than one type attribute, separate the options with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3d655-114">*Typname*</span><span class="sxs-lookup"><span data-stu-id="3d655-114">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3d655-115">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3d655-115">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d655-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d655-116">Remarks</span></span>

<span data-ttu-id="3d655-117">Das Attribut " **\[ zuordnen \]** " weist die folgenden gültigen Optionen auf.</span><span class="sxs-lookup"><span data-stu-id="3d655-117">The **\[allocate\]** attribute has the following valid options.</span></span>



| <span data-ttu-id="3d655-118">Option</span><span class="sxs-lookup"><span data-stu-id="3d655-118">Option</span></span>           | <span data-ttu-id="3d655-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d655-119">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="3d655-120">**alle \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="3d655-120">**all\_nodes**</span></span>   | <span data-ttu-id="3d655-121">Führt einen-Rückruf aus, um Speicher für alle Knoten zuzuweisen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d655-121">Makes one call to allocate and free memory for all nodes.</span></span>             |
| <span data-ttu-id="3d655-122">**einzelner \_ Knoten**</span><span class="sxs-lookup"><span data-stu-id="3d655-122">**single\_node**</span></span> | <span data-ttu-id="3d655-123">Führt viele einzelne Aufrufe aus, um jeden Knoten des Arbeitsspeichers zuzuordnen und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d655-123">Makes many individual calls to allocate and free each node of memory.</span></span> |
| <span data-ttu-id="3d655-124">**free**</span><span class="sxs-lookup"><span data-stu-id="3d655-124">**free**</span></span>         | <span data-ttu-id="3d655-125">Gibt Arbeitsspeicher bei Rückgabe vom Serverstub frei.</span><span class="sxs-lookup"><span data-stu-id="3d655-125">Frees memory on return from the server stub.</span></span>                          |
| <span data-ttu-id="3d655-126">**nicht \_ kostenlos**</span><span class="sxs-lookup"><span data-stu-id="3d655-126">**dont\_free**</span></span>   | <span data-ttu-id="3d655-127">Von wird vom Serverstub kein Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3d655-127">Does not free memory on return from the server stub.</span></span>                  |



 

<span data-ttu-id="3d655-128">Standardmäßig kann der Stub Speicher für Daten, auf die durch einen eindeutigen oder einen vollständigen Zeiger verwiesen wird, zuordnen, indem er die Benutzer Zuordnungen für die [**\_ Benutzer \_**](midl-user-allocate-1.md) Zuordnungen und die [**mittlere \_ \_ Benutzer**](midl-user-free-1.md) Freigabe für jeden Zeiger aufrufen</span><span class="sxs-lookup"><span data-stu-id="3d655-128">By default, the stubs may allocate storage for data referenced by a unique or full pointer by calling [**midl\_user\_allocate**](midl-user-allocate-1.md) and [**midl\_user\_free**](midl-user-free-1.md) individually for each pointer.</span></span>

<span data-ttu-id="3d655-129">Sie können die Geschwindigkeit der Anwendung optimieren, indem Sie die Option **alle \_ Knoten** angeben.</span><span class="sxs-lookup"><span data-stu-id="3d655-129">You can optimize the speed of your application by specifying the option **all\_nodes**.</span></span> <span data-ttu-id="3d655-130">Diese Option weist den Stub an, die Größe des gesamten Speichers zu berechnen, auf den über den Zeiger des angegebenen Typs verwiesen wird, und um einen einzelnen aufzurufenden [**Mittel l- \_ Benutzer \_ zuzuordnen**](midl-user-allocate-1.md).</span><span class="sxs-lookup"><span data-stu-id="3d655-130">This option directs the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](midl-user-allocate-1.md).</span></span> <span data-ttu-id="3d655-131">Der Stub gibt den Arbeitsspeicher frei, indem er einen [**\_ Benutzer \_ kostenlos**](midl-user-free-1.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="3d655-131">The stub releases the memory by making one call to [**midl\_user\_free**](midl-user-free-1.md).</span></span>

<span data-ttu-id="3d655-132">Die Option " **nicht \_ frei** gegeben" weist den Mittelwert Compiler an, einen Serverstub zu generieren, der für den angegebenen Typ keinen [**mittleren \_ Benutzer \_**](midl-user-free-1.md) Namen aufruft.</span><span class="sxs-lookup"><span data-stu-id="3d655-132">The **dont\_free** option directs the MIDL compiler to generate a server stub that does not call [**midl\_user\_free**](midl-user-free-1.md) for the specified type.</span></span> <span data-ttu-id="3d655-133">Die **Option \_ nicht** verfügbar ermöglicht, dass die-Zeiger Strukturen für die Serveranwendung zugänglich bleiben, nachdem der Remote Prozedur Aufruf abgeschlossen und an den Client zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3d655-133">The **dont\_free** option allows the pointer structures to remain accessible to the server application after the remote procedure call has completed and returned to the client.</span></span>

<span data-ttu-id="3d655-134">Das Attribut " **\[ zuordnen \]** " bewirkt, dass jeder **\[ in-, out \]** -Parameter, der ein Zeiger auf einen Typ ist, der mit der Option **alle \_ Knoten** qualifiziert ist, den Speicher neu zuordnen kann, wenn die Daten gemarshallt werden</span><span class="sxs-lookup"><span data-stu-id="3d655-134">The **\[allocate\]** attribute will cause any **\[in, out\]** parameter that is a pointer to a type qualified with the **all\_nodes** option to reallocate memory when the data is unmarshaled.</span></span> <span data-ttu-id="3d655-135">Es liegt in der Verantwortung der Anwendung, den zuvor zugeordneten Arbeitsspeicher für diesen Parameter freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d655-135">It is the responsibility of the application to free the memory allocated previously for this parameter.</span></span> <span data-ttu-id="3d655-136">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3d655-136">For example:</span></span>

``` syntax
typedef struct thistype 
{ 
    [string] char * PTHISTYPE;  
} * PTHISTYPE
HRESULT proc1 ( [in,out] PTHISTYPE * ppthistype);
```

<span data-ttu-id="3d655-137">Der Datentyp "pthistype" wird vom Stub vor dem Aufheben des Marshalling erneut in der [**\[ out \]**](out-idl.md) -Richtung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3d655-137">The data type PTHISTYPE will be reallocated in the [**\[out\]**](out-idl.md) direction by the stub before unmarshaling.</span></span> <span data-ttu-id="3d655-138">Daher muss die Anwendung den Arbeitsspeicher freigeben, den Sie zuvor für die Daten dieses Parameters reserviert haben, oder es tritt ein Speicherplatz auf.</span><span class="sxs-lookup"><span data-stu-id="3d655-138">Therefore, the application must free the memory it previously allocated for this parameter's data, or a memory leak will occur.</span></span>

## <a name="examples"></a><span data-ttu-id="3d655-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d655-139">Examples</span></span>

``` syntax
/* ACF file */ 
typedef [allocate(all_nodes, dont_free)] PTYPE1; 
typedef [allocate(all_nodes)] PTYPE2; 
typedef [allocate(dont_free)] PTYPE3;
```

## <a name="see-also"></a><span data-ttu-id="3d655-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3d655-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d655-141">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="3d655-141">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="3d655-142">**in**</span><span class="sxs-lookup"><span data-stu-id="3d655-142">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="3d655-143">**mittlere Benutzer Zuordnungen \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d655-143">**midl\_user\_allocate**</span></span>](midl-user-allocate-1.md)
</dt> <dt>

[<span data-ttu-id="3d655-144">**mittlerer l- \_ Benutzer \_ kostenlos**</span><span class="sxs-lookup"><span data-stu-id="3d655-144">**midl\_user\_free**</span></span>](midl-user-free-1.md)
</dt> <dt>

[<span data-ttu-id="3d655-145">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="3d655-145">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="3d655-146">**typedef**</span><span class="sxs-lookup"><span data-stu-id="3d655-146">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




