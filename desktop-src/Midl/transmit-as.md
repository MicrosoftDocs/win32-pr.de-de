---
title: transmit_as-Attribut
description: Das Attribut \ überträgt \_ As \ weist den Compiler an, Type-ID zuzuordnen, bei dem es sich um einen dargestellten Typ handelt, der von Client-und Server Anwendungen bearbeitet wird, wobei der übertragene Typ xmit-Type ist.
ms.assetid: 3dd1a242-03ec-49b4-ac96-87ef186e41d2
keywords:
- Transmit_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- transmit_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ec0cba27e994f7d77d441aef7bb783cad71cbad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337644"
---
# <a name="transmit_as-attribute"></a><span data-ttu-id="dec46-104">\_als Attribut übertragen</span><span class="sxs-lookup"><span data-stu-id="dec46-104">transmit\_as attribute</span></span>

<span data-ttu-id="dec46-105">Das Attribut "über **\[ tragen \_ als \]** " weist den Compiler an *, \* Type-ID \* \* \* zuzuordnen,* bei dem es sich um einen dargestellten Typ handelt, den Client-und Server Anwendungen mit einem übertragenen Typ " **xmit-Type** " bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="dec46-105">The **\[transmit\_as\]** attribute instructs the compiler to associate \**type-id\*\*\*,* which is a presented type that client and server applications manipulate, with a transmitted type **xmit-type.**</span></span>

``` syntax
typedef [transmit_as(xmit-type) [[ , type-attribute-list ]] ] type-specifier declarator-list; 

void __RPC_USER type-id_to_xmit (
  type-id __RPC_FAR *,
  xmit-type __RPC_FAR * __RPC_FAR *);
void __RPC_USER type-id_from_xmit (
  xmit-type __RPC_FAR *,
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_inst (
  type-id __RPC_FAR *);
void __RPC_USER type-id_free_xmit (
  xmit-type__RPC_FAR *);
```

## <a name="parameters"></a><span data-ttu-id="dec46-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dec46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec46-107">*xmit-Typ*</span><span class="sxs-lookup"><span data-stu-id="dec46-107">*xmit-type*</span></span> 
</dt> <dd>

<span data-ttu-id="dec46-108">Gibt den Datentyp an, der zwischen Client und Server übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="dec46-108">Specifies the data type that is transmitted between client and server.</span></span>

</dd> <dt>

<span data-ttu-id="dec46-109">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="dec46-109">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dec46-110">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dec46-110">Specifies one or more attributes that apply to the type.</span></span> <span data-ttu-id="dec46-111">Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die **\[** [**Zeichenfolge**](string.md) der Verwendungs Attribute **\]** und **\[** [**Ignore**](ignore.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dec46-111">Valid type attributes include **\[**[**handle**](handle.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**.</span></span> <span data-ttu-id="dec46-112">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="dec46-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="dec46-113">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="dec46-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="dec46-114">Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="dec46-114">Specifies a [base type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="dec46-115">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dec46-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="dec46-116">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="dec46-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dec46-117">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="dec46-117">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="dec46-118">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="dec46-118">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="dec46-119">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="dec46-119">The *declarator-list* consists of one or more declarators separated by commas.</span></span> <span data-ttu-id="dec46-120">Der parameterdeklarator im funktionsdedeclarator (z. b. der Parameter Name) ist optional.</span><span class="sxs-lookup"><span data-stu-id="dec46-120">The parameter declarator in the function declarator, such as the parameter name, is optional.</span></span>

</dd> <dt>

<span data-ttu-id="dec46-121">*Typ-ID*</span><span class="sxs-lookup"><span data-stu-id="dec46-121">*type-id*</span></span> 
</dt> <dd>

<span data-ttu-id="dec46-122">Gibt den Namen des Datentyps an, der den Client-und Server Anwendungen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dec46-122">Specifies the name of the data type that is presented to the client and server applications.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dec46-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dec46-123">Remarks</span></span>

<span data-ttu-id="dec46-124">Um das Attribut "über **\[ tragen \_ als \]** " zu verwenden, muss der Benutzer Routinen bereitstellen, mit denen Daten zwischen den dargestellten und übertragenen Typen konvertiert werden. diese Routinen müssen auch Speicher freigeben, der zum Speichern der konvertierten Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dec46-124">To use the **\[transmit\_as\]** attribute, the user must supply routines that convert data between the presented and the transmitted types; these routines must also free memory used to hold the converted data.</span></span> <span data-ttu-id="dec46-125">Das Attribut "über **\[ tragen \_ als \]** " weist die stubzeichen an, die vom Benutzer bereitgestellten Konvertierungs Routinen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="dec46-125">The **\[transmit\_as\]** attribute instructs the stubs to call the user-supplied conversion routines.</span></span>

<span data-ttu-id="dec46-126">Der übertragene Typ " *xmit-Type* " muss in einen mittleren Basistyp, vordefinierten Typ oder einen Typbezeichner aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="dec46-126">The transmitted type *xmit-type* must resolve to a MIDL base type, predefined type, or a type identifier.</span></span> <span data-ttu-id="dec46-127">Weitere Informationen finden Sie unter [Mittel l-Basis Typen](midl-base-types.md).</span><span class="sxs-lookup"><span data-stu-id="dec46-127">For more information, see [MIDL Base Types](midl-base-types.md).</span></span>

<span data-ttu-id="dec46-128">Der Benutzer muss die folgenden Routinen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dec46-128">The user must supply the following routines.</span></span>



| <span data-ttu-id="dec46-129">Routine Name</span><span class="sxs-lookup"><span data-stu-id="dec46-129">Routine name</span></span>              | <span data-ttu-id="dec46-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dec46-130">Description</span></span>                                                                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec46-131">*Type-ID \* \* \* \_ bis \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="dec46-131">*type-id\*\*\*\_to\_xmit*\*</span></span>   | <span data-ttu-id="dec46-132">Konvertiert Daten aus dem dargestellten Typ in den übertragenen Typ.</span><span class="sxs-lookup"><span data-stu-id="dec46-132">Converts data from the presented type to the transmitted type.</span></span> <span data-ttu-id="dec46-133">Diese Routine weist Speicher für den übertragenen Typ und für alle Daten zu, auf die von Zeigern im übertragenen Typ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dec46-133">This routine allocates memory for the transmitted type and for any data referenced by pointers in the transmitted type.</span></span>                            |
| <span data-ttu-id="dec46-134">*Type-ID \* \* \* \_ from \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="dec46-134">*type-id\*\*\*\_from\_xmit*\*</span></span> | <span data-ttu-id="dec46-135">Konvertiert Daten aus dem übertragenen Typ in den dargestellten Typ.</span><span class="sxs-lookup"><span data-stu-id="dec46-135">Converts data from the transmitted type to the presented type.</span></span> <span data-ttu-id="dec46-136">Diese Routine ist für die Zuweisung von Speicher für Daten reserviert, auf die von Zeigern im dargestellten Typ verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="dec46-136">This routine is responsible for allocating memory for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="dec46-137">RPC ordnet Speicher für den Typ selbst zu.</span><span class="sxs-lookup"><span data-stu-id="dec46-137">RPC allocates memory for the type itself.</span></span> |
| <span data-ttu-id="dec46-138">*Type-ID \* \* \* \_ freie \_ inst*\*</span><span class="sxs-lookup"><span data-stu-id="dec46-138">*type-id\*\*\*\_free\_inst*\*</span></span> | <span data-ttu-id="dec46-139">Gibt für Daten, auf die Zeiger im dargestellten Typ verweisen, zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="dec46-139">Frees memory allocated for data referenced by pointers in the presented type.</span></span> <span data-ttu-id="dec46-140">RPC gibt Arbeitsspeicher für den Typ selbst frei.</span><span class="sxs-lookup"><span data-stu-id="dec46-140">RPC frees memory for the type itself.</span></span>                                                                                               |
| <span data-ttu-id="dec46-141">*Type-ID \* \* \* \_ freie \_ xmit*\*</span><span class="sxs-lookup"><span data-stu-id="dec46-141">*type-id\*\*\*\_free\_xmit*\*</span></span> | <span data-ttu-id="dec46-142">Gibt Speicher frei, der vom Aufrufer für den übertragenen Typ verwendet wird, sowie für Daten, auf die Zeiger im übertragenen Typ verweisen.</span><span class="sxs-lookup"><span data-stu-id="dec46-142">Frees storage used by the caller for the transmitted type and for data referenced by pointers in the transmitted type.</span></span>                                                                                            |



 

 

<span data-ttu-id="dec46-143">Der Clientstub ruft *Type-ID \* \* \* \_ in \_ xmit*\* auf, um Speicherplatz für den übertragenen Typ zuzuweisen und die Daten in Objekte vom Typ *xmit-Type* zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="dec46-143">The client stub calls *type-id\*\*\*\_to\_xmit*\* to allocate space for the transmitted type and to translate the data into objects of type *xmit-type.*</span></span> <span data-ttu-id="dec46-144">Der Serverstub ordnet Speicherplatz für den ursprünglichen Datentyp zu und ruft *Type-ID \* \* \* \_ von \_ xmit*\* auf, um die Daten vom übertragenen Typ in den dargestellten Typ zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="dec46-144">The server stub allocates space for the original data type and calls *type-id\*\*\*\_from\_xmit*\* to translate the data from its transmitted type to the presented type.</span></span>

<span data-ttu-id="dec46-145">Bei Rückgabe aus dem Anwendungscode ruft der Server-Stub *Type-ID \* \* \* \_ Free \_ inst*\* auf, um den Speicher für *Type-ID* auf Serverseite freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dec46-145">Upon return from the application code, the server stub calls *type-id\*\*\*\_free\_inst*\* to deallocate the storage for *type-id* on the server side.</span></span> <span data-ttu-id="dec46-146">Der Clientstub ruft *Type-ID \* \* \* \_ Free \_ xmit*\* auf, um den *xmit-Typspeicher* auf der Clientseite freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dec46-146">The client stub calls *type-id\*\*\*\_free\_xmit*\* to deallocate the *xmit-type* storage on the client side.</span></span>

<span data-ttu-id="dec46-147">Die folgenden Typen können kein Attribut "über **\[ tragen \_ als \]** " aufweisen:</span><span class="sxs-lookup"><span data-stu-id="dec46-147">The following types cannot have a **\[transmit\_as\]** attribute:</span></span>

-   <span data-ttu-id="dec46-148">Kontext Handles (Typen mit dem **\[** Kontotyp Attribut des [**Kontext \_ Handles**](context-handle.md) **\]** ) und Typen, die als Parameter mit dem **\[ Kontext \_ \] handle** -Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dec46-148">Context handles (types with the **\[**[**context\_handle**](context-handle.md)**\]** type attribute and types that are used as parameters with the **\[context\_handle\]** attribute)</span></span>
-   <span data-ttu-id="dec46-149">Typen, die Pipes sind oder von Pipes abgeleitet sind</span><span class="sxs-lookup"><span data-stu-id="dec46-149">Types that are pipes or derived from pipes</span></span>
-   <span data-ttu-id="dec46-150">Datentypen, die als Basistyp einer Pipe-Definition verwendet werden</span><span class="sxs-lookup"><span data-stu-id="dec46-150">Data types that are used as the base type of a pipe definition</span></span>
-   <span data-ttu-id="dec46-151">Parameter, die Zeiger sind oder zu Zeigern aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="dec46-151">Parameters that are pointers or resolve to pointers</span></span>
-   <span data-ttu-id="dec46-152">Parameter, die konforme, abweichende oder geöffnete Arrays sind</span><span class="sxs-lookup"><span data-stu-id="dec46-152">Parameters that are conformant, varying, or open arrays</span></span>
-   <span data-ttu-id="dec46-153">Strukturen, die konforme Arrays enthalten</span><span class="sxs-lookup"><span data-stu-id="dec46-153">Structures that contain conformant arrays</span></span>
-   <span data-ttu-id="dec46-154">Das vordefinierte [**Typhandle \_ t**](handle-t.md), [**void**](void.md)</span><span class="sxs-lookup"><span data-stu-id="dec46-154">The predefined type [**handle\_t**](handle-t.md), [**void**](void.md)</span></span>

<span data-ttu-id="dec46-155">Typen, die übertragen werden, müssen den folgenden Einschränkungen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="dec46-155">Types that are transmitted must conform to the following restrictions:</span></span>

-   <span data-ttu-id="dec46-156">Sie dürfen keine Zeiger sein oder Zeiger enthalten.</span><span class="sxs-lookup"><span data-stu-id="dec46-156">They must not be pointers or contain pointers.</span></span>
-   <span data-ttu-id="dec46-157">Sie dürfen keine Pipes sein oder Pipes enthalten.</span><span class="sxs-lookup"><span data-stu-id="dec46-157">They must not be pipes or contain pipes.</span></span>

## <a name="examples"></a><span data-ttu-id="dec46-158">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dec46-158">Examples</span></span>

``` syntax
typedef struct _TREE_NODE_TYPE 
{ 
    unsigned short data; 
    struct _TREE_NODE_TYPE * left; 
    struct _TREE_NODE_TYPE * right; 
} TREE_NODE_TYPE; 
 
typedef [transmit_as(TREE_XMIT_TYPE)] TREE_NODE_TYPE * TREE_TYPE; 
 
void __RPC_USER TREE_TYPE_to_xmit( 
    TREE_TYPE __RPC_FAR * , 
    TREE_XMIT_TYPE __RPC_FAR * __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_from_xmit ( 
    TREE_XMIT_TYPE __RPC_FAR *, 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_inst( 
    TREE_TYPE __RPC_FAR *); 
 
void __RPC_USER TREE_TYPE_free_xmit( 
    TREE_XMIT_TYPE __RPC_FAR *);
```

## <a name="see-also"></a><span data-ttu-id="dec46-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dec46-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec46-160">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="dec46-160">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="dec46-161">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="dec46-161">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="dec46-162">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="dec46-162">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="dec46-163">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="dec46-163">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="dec46-164">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="dec46-164">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="dec46-165">**Handle \_ t**</span><span class="sxs-lookup"><span data-stu-id="dec46-165">**handle\_t**</span></span>](handle-t.md)
</dt> <dt>

[<span data-ttu-id="dec46-166">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="dec46-166">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dec46-167">**lassen**</span><span class="sxs-lookup"><span data-stu-id="dec46-167">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="dec46-168">**ptr**</span><span class="sxs-lookup"><span data-stu-id="dec46-168">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="dec46-169">**ref**</span><span class="sxs-lookup"><span data-stu-id="dec46-169">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="dec46-170">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="dec46-170">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="dec46-171">**struct**</span><span class="sxs-lookup"><span data-stu-id="dec46-171">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="dec46-172">**\_Switchtyp**</span><span class="sxs-lookup"><span data-stu-id="dec46-172">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="dec46-173">**typedef**</span><span class="sxs-lookup"><span data-stu-id="dec46-173">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="dec46-174">**Union**</span><span class="sxs-lookup"><span data-stu-id="dec46-174">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="dec46-175">**gem**</span><span class="sxs-lookup"><span data-stu-id="dec46-175">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="dec46-176">**void**</span><span class="sxs-lookup"><span data-stu-id="dec46-176">**void**</span></span>](void.md)
</dt> </dl>

 

 