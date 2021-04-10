---
title: Das represent_as-Attribut
description: Mit dem Attribut \ wird \_ als \ dargestellt können Sie angeben, wie ein bestimmter, transaktionier baren Datentyp für die Anwendung dargestellt wird.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Remote Prozedur Aufruf RPC, Attribute, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102223"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="bbaf8-105">Das \_ As-Attribut.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-105">The represent\_as Attribute</span></span>

<span data-ttu-id="bbaf8-106">Mithilfe des \[ Attributs [ \_ As](/windows/desktop/Midl/represent-as) \] können Sie angeben, wie ein bestimmter, transaktionier baren Datentyp für die Anwendung dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="bbaf8-107">Dies erfolgt durch Angabe des Namens des dargestellten Typs für einen bekannten transaktionablen Typ und Bereitstellen der Konvertierungs Routinen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="bbaf8-108">Sie müssen auch die Routinen bereitstellen, um den von den Datentyp Objekten genutzten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="bbaf8-109">Verwenden Sie das Attribut **\[ \_ As \]** , um eine Anwendung mit einem anderen, möglicherweise nicht transaktionablen Datentyp und nicht mit dem Typ darzustellen, der tatsächlich zwischen Client und Server übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="bbaf8-110">Es ist auch möglich, dass der Typ, der von der Anwendung bearbeitet wird, zum Zeitpunkt der mittleren Kompilierung unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="bbaf8-111">Wenn Sie einen klar definierten transaktionablen Typ auswählen, müssen Sie sich keine Gedanken über die Datendarstellung in der heterogenen Umgebung machen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="bbaf8-112">Das Attribut " **\[ \_ As \]** " kann die Anwendung effizienter machen, indem die Menge der über das Netzwerk übertragenen Daten reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="bbaf8-113">Das Attribut " **\[ \_ As \]** " ähnelt dem \[ [Übertragungs- \_ As](/windows/desktop/Midl/transmit-as) - \] Attribut.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="bbaf8-114">Bei der **\[ \_ \]** **\[ \_ Übertragung als können Sie jedoch einen Datentyp angeben, der für die Übertragung verwendet wird. Sie können jedoch angeben, wie ein Datentyp für die Anwendung dargestellt wird. \]**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="bbaf8-115">Der dargestellte Typ muss nicht in den in der Mitte verarbeiteten Dateien definiert werden. Sie kann zu dem Zeitpunkt definiert werden, zu dem die Stub mit dem C-Compiler kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="bbaf8-116">Verwenden Sie hierzu die include-Direktive in der [Anwendungs Konfigurationsdatei (ACF)](the-application-configuration-file-acf-.md) , um die entsprechende Header Datei zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="bbaf8-117">Die folgende ACF definiert z. b. einen lokalen Typ für die Anwendung ( **repr- \_ Typ**) für den transaktionalen Typ **namens \_ Type:**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="bbaf8-118">In der folgenden Tabelle werden die vier von Programmierern bereitgestellten Routinen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="bbaf8-119">-Routine zurückgegebener Wert</span><span class="sxs-lookup"><span data-stu-id="bbaf8-119">Routine</span></span>                      | <span data-ttu-id="bbaf8-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbaf8-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaf8-121">**benannter \_ Typ \_ aus \_ lokalem**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="bbaf8-122">Weist eine Instanz des Netzwerk Typs zu und konvertiert vom lokalen Typ in den Netzwerktyp.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="bbaf8-123">**benannter \_ Typ \_ zu \_ lokal**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="bbaf8-124">Konvertiert den Netzwerktyp in den lokalen Typ.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="bbaf8-125">**benannte \_ \_ typfreie \_ lokale**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="bbaf8-126">Gibt Arbeitsspeicher frei, der durch einen-Befehl für den benannten Typ zugeordnet ist, jedoch nicht **\_ \_ für \_** den Typ selbst.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="bbaf8-127">**benannter \_ Typ \_ ohne \_ inst**</span><span class="sxs-lookup"><span data-stu-id="bbaf8-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="bbaf8-128">Gibt Speicher für den Netzwerktyp frei (beide Seiten).</span><span class="sxs-lookup"><span data-stu-id="bbaf8-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="bbaf8-129">Der benannte Typ wird von der Anwendung nicht bearbeitet, außer von diesen vier vom Programmierer bereitgestellten Routinen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="bbaf8-130">Der einzige für die Anwendung sichtbare Typ ist der dargestellte Typ.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="bbaf8-131">Die Anwendung verwendet den dargestellten Typnamen anstelle des übertragenen Typnamens in den Prototypen und vom Compiler generierten Stub.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="bbaf8-132">Sie müssen den Satz von Routinen für beide Seiten angeben.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="bbaf8-133">Für temporäre **benannte \_ Typobjekte** ruft der Stub den **benannten \_ Typ " \_ Free \_ inst** " auf, um Speicher freizugeben, der durch einen aufzurufenden **\_ CallType \_ from \_ local** zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="bbaf8-134">Wenn der dargestellte Typ ein Zeiger ist oder einen Zeiger enthält, muss der **benannte Typ für die \_ \_ \_ lokale** Routine Speicher für die Daten zuweisen, auf die der Zeiger verweist (das dargestellte Typobjekt selbst wird vom Stub auf die übliche Weise manipuliert).</span><span class="sxs-lookup"><span data-stu-id="bbaf8-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="bbaf8-135">Für \[ [out](/windows/desktop/Midl/out-idl) \] -und \[ [in](/windows/desktop/Midl/in)-out- \] Parameter eines Typs, die **\[ \_ als** oder eine Komponente von darstellen, wird **die \_ benannte \_ typfreie \_ lokale** Routine automatisch für die Datenobjekte aufgerufen, die das-Attribut enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="bbaf8-136">Bei **\[ in \]** -Parametern wird die **benannte \_ \_ \_ lokale** Routine für den Typ nur aufgerufen, wenn das Attribut **\[ \_ As als \]** Attribut auf den Parameter angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="bbaf8-137">Wenn das-Attribut auf die Komponenten des-Parameters angewendet wurde, wird die \*\* \*\*\* \_ Kostenlose \_ local\*\*-Routine nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="bbaf8-138">Das Freigeben von Routinen wird nicht für die eingebetteten Daten und den at-most-Once-Aufruf (im Zusammenhang mit dem Attribut der obersten Ebene) **\[ \] für einen only** -Parameter aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="bbaf8-139">Es ist möglich, die über **\[ Tragung \_ als \]** und **\[ \_ als \]** Attribute für denselben Typ zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="bbaf8-140">Beim Marshalling von Daten wird die **\[ Darstellung \_ als \]** Typkonvertierung zuerst angewendet. Anschließend wird die über **\[ Tragung \_ als \]** Konvertierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="bbaf8-141">Die Reihenfolge wird beim Marshalling von Daten rückgängig gemacht.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="bbaf8-142">Folglich ordnet beim Marshalling \* **\_ von \_ local** eine Instanz eines benannten Typs zu und übersetzt Sie von einem lokalen Typobjekt in das temporäre benannte Typobjekt.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="bbaf8-143">Dieses Objekt ist das präsentierte Typobjekt, das für die- \* **\_ to- \_ xmit** -Routine verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="bbaf8-144">Die \* **\_ to \_ xmit** -Routine ordnet dann ein übertragener Typobjekt zu und übersetzt es vom dargestellten (benannten) Objekt in das übertragene Objekt.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="bbaf8-145">Ein Array von Long-Integer-Werten kann verwendet werden, um eine verknüpfte Liste darzustellen.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="bbaf8-146">Auf diese Weise wird die Liste von der Anwendung bearbeitet, und die Übertragung verwendet ein Array von langen ganzen Zahlen, wenn eine Liste dieses Typs übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="bbaf8-147">Sie können mit einem Array beginnen, aber es ist bequemer, ein Konstrukt mit einem geöffneten Array von langen ganzen Zahlen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="bbaf8-148">Das folgende Beispiel zeigt die erforderliche Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="bbaf8-149">Beachten Sie, dass die Prototypen der Routinen, die den **longarr** -Typ verwenden, tatsächlich in den Stub. h-Dateien als **ploc- \_ Feld** anstelle des **longarr** -Typs angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="bbaf8-150">Dasselbe gilt für die geeigneten Stubs in der Datei "Stub \_ c. c".</span><span class="sxs-lookup"><span data-stu-id="bbaf8-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="bbaf8-151">Sie müssen die folgenden vier Funktionen bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="bbaf8-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="bbaf8-152">Die oben gezeigten Routinen gehen wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="bbaf8-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="bbaf8-153">Die **longarr \_ from \_ local** -Routine zählt die Knoten der Liste, ordnet ein longarr-Objekt mit der Größe **sizeof**(**longarr**) + count \* **sizeof**(**Long**) zu, legt das **Größen** Feld auf count fest und kopiert die Daten in das **dataarr** -Feld.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="bbaf8-154">Die Routine **longarr \_ to \_ local** erstellt eine Liste mit Größen Knoten und überträgt das Array an die entsprechenden Knoten.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="bbaf8-155">Die Routine " **longarr \_ Free \_ inst** " gibt in diesem Fall nichts frei.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="bbaf8-156">Die **\_ Kostenlose \_ lokale longarr** -Routine gibt alle Knoten der Liste frei.</span><span class="sxs-lookup"><span data-stu-id="bbaf8-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 