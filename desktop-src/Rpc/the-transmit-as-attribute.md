---
title: Das Transmit_as-Attribut
description: Das Attribut "\ \_ übertragen als \" bietet eine Möglichkeit, das Datenmarshalling zu steuern, ohne sich Gedanken über das Marshalling von Daten auf niedriger Ebene \ 8212 zu machen, d. h. ohne sich Gedanken über Datengrößen oder Byte Austausch Vorgänge in einer heterogenen Umgebung zu machen.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- Remote Prozedur Aufruf RPC, Attribute, Transmit_as
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390713"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="69bb2-105">Das Attribut "übertragen \_ als"</span><span class="sxs-lookup"><span data-stu-id="69bb2-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="69bb2-106">Das **\[** Attribut "über [**tragen \_ als**](/windows/desktop/Midl/transmit-as) " **\]** bietet eine Möglichkeit, das Marshalling von Daten zu steuern, ohne sich Gedanken über das Marshalling von Daten auf niedriger Ebene zu machen, d. –., ohne sich Gedanken über Datengrößen oder Byte Austausch Vorgänge in einer heterogenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="69bb2-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="69bb2-107">Wenn Sie die Menge der über das Netzwerk übertragenen Daten reduzieren können, kann das Attribut "über **\[ tragen \_ als \]** " Ihre Anwendung effizienter gestalten.</span><span class="sxs-lookup"><span data-stu-id="69bb2-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="69bb2-108">Verwenden Sie das Attribut "über **\[ tragen \_ als \]** ", um einen Datentyp anzugeben, der von den RPC-Stubdaten über das Netzwerk übertragen wird, anstatt den von der Anwendung bereitgestellten Datentyp zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="69bb2-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="69bb2-109">Sie stellen Routinen bereit, die den Datentyp in und aus dem Typ konvertieren, der für die Übertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69bb2-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="69bb2-110">Sie müssen auch Routinen bereitstellen, um den für den Datentyp und den übertragenen Typ verwendeten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="69bb2-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="69bb2-111">Im folgenden Beispiel wird der **xmit- \_ Typ** als Datentyp definiert, der für alle Anwendungsdaten übertragen wird, die als Typ der **\_ Typspezifikation** angegeben sind:</span><span class="sxs-lookup"><span data-stu-id="69bb2-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="69bb2-112">In der folgenden Tabelle werden die vier von Programmierern bereitgestellten Routine Namen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="69bb2-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="69bb2-113">**Type** ist der Datentyp, der der Anwendung bekannt ist, und der **\_ Typ xmit** ist der Datentyp, der für die Übertragung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69bb2-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="69bb2-114">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="69bb2-114">Routine</span></span>                                                 | <span data-ttu-id="69bb2-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69bb2-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69bb2-116">**\_in \_ xmit eingeben**</span><span class="sxs-lookup"><span data-stu-id="69bb2-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="69bb2-117">Ordnet ein Objekt des übertragenen Typs zu und konvertiert vom Anwendungstyp in den Typ, der über das Netzwerk (Aufrufer und Objekt aufgerufen) übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="69bb2-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="69bb2-118">**Typ \_ von \_ xmit**</span><span class="sxs-lookup"><span data-stu-id="69bb2-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="69bb2-119">Konvertiert einen übertragenen Typ in einen Anwendungstyp (Aufrufer und Objekt mit dem Namen).</span><span class="sxs-lookup"><span data-stu-id="69bb2-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="69bb2-120">**Geben Sie " \_ Free \_ inst**</span><span class="sxs-lookup"><span data-stu-id="69bb2-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="69bb2-121">Gibt Ressourcen frei, die vom Anwendungstyp verwendet werden (nur Objekt aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="69bb2-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="69bb2-122">**Geben Sie "Free" ein. \_ \_**</span><span class="sxs-lookup"><span data-stu-id="69bb2-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="69bb2-123">Gibt den vom Typ zurückgegebenen Speicher \*\*\*\*\*\_\*\*\* für die \_ xmit\*\* -Routine frei (Aufrufer und Objekt aufgerufen).</span><span class="sxs-lookup"><span data-stu-id="69bb2-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="69bb2-124">Mit Ausnahme dieser vier vom Programmierer bereitgestellten Funktionen wird der übertragene Typ nicht von der Anwendung bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="69bb2-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="69bb2-125">Der übertragene Typ wird nur zum Verschieben von Daten über das Netzwerk definiert.</span><span class="sxs-lookup"><span data-stu-id="69bb2-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="69bb2-126">Nachdem die Daten in den von der Anwendung verwendeten Typ konvertiert wurden, wird der vom übertragenen Typ verwendete Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="69bb2-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="69bb2-127">Diese vom Programmierer bereitgestellten Routinen werden entweder vom Client oder von der Serveranwendung basierend auf den direktionalen Attributen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="69bb2-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="69bb2-128">Wenn der-Parameter **\[** nur [**in**](/windows/desktop/Midl/in) ist **\]** , überträgt der Client an den Server.</span><span class="sxs-lookup"><span data-stu-id="69bb2-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="69bb2-129">Der Client benötigt den **Typ \_ , um \_ xmit** -und- **\_ typfreie \_ xmit** -Funktionen zu geben.</span><span class="sxs-lookup"><span data-stu-id="69bb2-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="69bb2-130">Der Server benötigt den **Typ \_ von \_ xmit** und **die \_ typfreien \_ inst** -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="69bb2-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="69bb2-131">Bei einem reinen **\[** [**out**](/windows/desktop/Midl/out-idl) **\]** -Parameter überträgt der Server an den Client.</span><span class="sxs-lookup"><span data-stu-id="69bb2-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="69bb2-132">Die Serveranwendung muss den **Typ \_ in \_ xmit** und den **Typ " \_ freie \_ xmit** -Funktionen" implementieren, während das Client Programm den **Typ aus der \_ \_ xmit** -Funktion bereitstellen muss.</span><span class="sxs-lookup"><span data-stu-id="69bb2-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="69bb2-133">Bei den temporären **xmit- \_ Typobjekten** ruft der Stub den **Typ " ***\_*** Free \_ xmit** " auf, um Speicher freizugeben, der durch einen aufrufungstyp **\_ zu \_ xmit** belegt wird.</span><span class="sxs-lookup"><span data-stu-id="69bb2-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="69bb2-134">Bestimmte Richtlinien gelten für die Anwendungstyp Instanz.</span><span class="sxs-lookup"><span data-stu-id="69bb2-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="69bb2-135">Wenn der Anwendungstyp ein Zeiger ist oder einen Zeiger enthält, muss der **Typ** \_ **aus der \_ xmit** -Routine Speicher für die Daten zuweisen, auf die die Zeiger zeigen (das Anwendungstyp Objekt selbst wird vom Stub auf die übliche Weise manipuliert).</span><span class="sxs-lookup"><span data-stu-id="69bb2-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="69bb2-136">Für **\[ out \]** -und **\[ in-, out- \] out \]** -Parameter oder eine der zugehörigen Komponenten eines Typs, der das Attribut "über **\[ tragen \_ als \]** " enthält, wird die **Type** \_ **Free \_ inst** -Routine automatisch für die Datenobjekte aufgerufen, die über das-Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="69bb2-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="69bb2-137">Bei **in** -Parametern wird die  \_ **typfreie \_ inst** -Routine nur aufgerufen, wenn das über **\[ tragen \_ als \]** -Attribut auf den Parameter angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="69bb2-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="69bb2-138">Wenn das-Attribut auf die Komponenten des-Parameters angewendet wurde,  \_ wird die **typfreie \_ inst** -Routine nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="69bb2-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="69bb2-139">Es gibt keine Freigabe Aufrufe für die eingebetteten Daten und höchstens einen Aufruf (im Zusammenhang mit dem Attribut der obersten Ebene) **für einen nur** -Parameter.</span><span class="sxs-lookup"><span data-stu-id="69bb2-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="69bb2-140">Mit der mittleren l 2,0 müssen sowohl der Client als auch der Server alle vier Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="69bb2-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="69bb2-141">Beispielsweise kann eine verknüpfte Liste als Array mit Größenanpassung übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="69bb2-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="69bb2-142">Der **Typ \_ für die \_ xmit** -Routine durchläuft die verknüpfte Liste und kopiert die geordneten Daten in ein Array.</span><span class="sxs-lookup"><span data-stu-id="69bb2-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="69bb2-143">Die Array Elemente sind so angeordnet, dass die vielen Zeiger, die der Listenstruktur zugeordnet sind, nicht übertragen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="69bb2-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="69bb2-144">Der **Typ \_ aus der \_ xmit** -Routine liest das Array und fügt seine Elemente in eine verknüpfte Listenstruktur ein.</span><span class="sxs-lookup"><span data-stu-id="69bb2-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="69bb2-145">Die Liste mit doppelten Verknüpfungen (Double \_ Link \_ List) enthält Daten und Zeiger auf die vorherigen und nächsten Listenelemente:</span><span class="sxs-lookup"><span data-stu-id="69bb2-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="69bb2-146">Anstatt die komplexe Struktur **\[** zu versenden, kann das [**Übertragungs- \_ As**](/windows/desktop/Midl/transmit-as) - **\]** Attribut verwendet werden, um es über das Netzwerk als Array zu senden.</span><span class="sxs-lookup"><span data-stu-id="69bb2-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="69bb2-147">Die Reihenfolge der Elemente in der Liste wird durch die Reihenfolge der Elemente im Array zu geringeren Kosten beibehalten:</span><span class="sxs-lookup"><span data-stu-id="69bb2-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="69bb2-148">Das Attribut "über **\[ tragen \_ als \]** " wird in der IDL-Datei angezeigt:</span><span class="sxs-lookup"><span data-stu-id="69bb2-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="69bb2-149">Im folgenden Beispiel definiert **modifylistproc** den Parameter vom Typ Double- \_ \_ Linktyp als in- **\[ , \] out** -Parameter:</span><span class="sxs-lookup"><span data-stu-id="69bb2-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="69bb2-150">Die vier vom Programmierer definierten Funktionen verwenden den Namen des Typs in den Funktionsnamen und verwenden die dargestellten und übertragenen Typen wie erforderlich als Parametertypen:</span><span class="sxs-lookup"><span data-stu-id="69bb2-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 