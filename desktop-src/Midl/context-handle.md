---
title: context_handle-Attribut
description: Das \ Context \_ handle \-Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724960"
---
# <a name="context_handle-attribute"></a><span data-ttu-id="0a6cf-104">Kontext \_ handle-Attribut</span><span class="sxs-lookup"><span data-stu-id="0a6cf-104">context\_handle attribute</span></span>

<span data-ttu-id="0a6cf-105">Das **\[ Kontext \_ handle \]** -Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-105">The **\[context\_handle\]** attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span>

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a><span data-ttu-id="0a6cf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a6cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6cf-107">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-107">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-108">Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-108">Specifies one or more attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-109">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-109">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-110">Gibt einen Zeigertyp oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-110">Specifies a pointer type or a type identifier.</span></span> <span data-ttu-id="0a6cf-111">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-111">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-112">*Deklarator und Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-112">*declarator and declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-113">Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-113">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="0a6cf-114">Der Deklarator für ein Kontext Handle muss mindestens einen zeigerdeklarator enthalten.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-114">The declarator for a context handle must include at least one pointer declarator.</span></span> <span data-ttu-id="0a6cf-115">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="0a6cf-115">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="0a6cf-116">Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-116">The *declarator-list* consists of one or more declarators, separated by commas.</span></span> <span data-ttu-id="0a6cf-117">Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-117">The parameter-name identifier in the function declarator is optional.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-118">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-118">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-119">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-119">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="0a6cf-120">Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[ Kontext \_ handle \]**.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-120">Valid function attributes are **\[**[**callback**](callback.md)**\]**, **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[context\_handle\]**.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-121">*PTR-decl*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-121">*ptr-decl*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-122">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-122">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="0a6cf-123">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn **\*** Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-123">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the **\*** designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-124">*function-name*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-124">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-125">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-125">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-126">*Parameter-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-126">*parameter-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-127">Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-127">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="0a6cf-128">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-128">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="0a6cf-129">*Context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="0a6cf-129">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="0a6cf-130">Gibt den Bezeichner an, der den in einer [**typedef**](typedef.md) -Deklaration definierten Kontext Handle-Typ angibt, der das **\[ Kontext \_ handle \]** -Attribut annimmt.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-130">Specifies the identifier that specifies the context handle type as defined in a [**typedef**](typedef.md) declaration that takes the **\[context\_handle\]** attribute.</span></span> <span data-ttu-id="0a6cf-131">Die Rundown-Routine ist optional.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-131">The rundown routine is optional.</span></span>

<span data-ttu-id="0a6cf-132">**Windows Server 2003 und Windows XP:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert).</span><span class="sxs-lookup"><span data-stu-id="0a6cf-132">**Windows ServerÂ 2003 and WindowsÂ XP:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="0a6cf-133">Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-133">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="0a6cf-134">Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-134">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="0a6cf-135">Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-135">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="0a6cf-136">Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-136">Note that creation methods are implicitly serialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a6cf-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a6cf-137">Remarks</span></span>

<span data-ttu-id="0a6cf-138">Das **\[ Kontext \_ handle \]** -Attribut kann als Attribut vom Typ "IDL [**typedef**](typedef.md) ", als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-138">The **\[context\_handle\]** attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span> <span data-ttu-id="0a6cf-139">Wenn Sie das **\[ Kontext \_ handle \]** -Attribut auf eine Typdefinition anwenden, müssen Sie auch eine Kontext-Rundown-Routine bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-139">When you apply the **\[context\_handle\]** attribute to a type definition, you must also provide a context rundown routine.</span></span> <span data-ttu-id="0a6cf-140">Ausführliche Informationen finden Sie in der ausführungsausführungsroutine des [Server Kontexts](/windows/desktop/Rpc/server-context-run-down-routine)</span><span class="sxs-lookup"><span data-stu-id="0a6cf-140">See [Server Context Run-down Routine](/windows/desktop/Rpc/server-context-run-down-routine) for details.</span></span>

<span data-ttu-id="0a6cf-141">Wenn Sie den Mittelwert Compiler im Standardmodus ([**/MS \_ ext**](-ms-ext.md)) verwenden, kann es sich bei einem Kontext Handle um jeden vom Benutzer ausgewählten Zeigertyp handeln, sofern er die Anforderungen für die hier beschriebenen Kontext Handles erfüllt.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-141">When you use the MIDL compiler in default ([**/ms\_ext**](-ms-ext.md)) mode, a context handle can be any pointer type selected by the user, as long as it complies with the requirements for context handles described here.</span></span> <span data-ttu-id="0a6cf-142">Die Daten, die einem solchen Kontext behandlertyp zugeordnet sind, werden nicht im Netzwerk übertragen und sollten nur von der Serveranwendung bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-142">The data associated with such a context handle type is not transmitted on the network and should only be manipulated by the server application.</span></span> <span data-ttu-id="0a6cf-143">DCE-IDL-Compiler beschränken Kontext Handles auf Zeiger vom Typ " [**void**](void.md) " **\*** .</span><span class="sxs-lookup"><span data-stu-id="0a6cf-143">DCE IDL compilers restrict context handles to pointers of type [**void**](void.md) **\***.</span></span> <span data-ttu-id="0a6cf-144">Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-144">Therefore this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="0a6cf-145">Wie bei anderen handle-Typen ist das Kontext Handle für die Client Anwendung nicht transparent, und alle damit verknüpften Daten werden nicht übertragen.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-145">As with other handle types, the context handle is opaque to the client application, and any data associated with it is not transmitted.</span></span> <span data-ttu-id="0a6cf-146">Auf dem Server dient das Kontext Handle als Handle für den aktiven Kontext, und auf alle Daten, die dem Kontext behandlertyp zugeordnet sind, kann zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-146">On the server, the context handle serves as a handle on active context, and all data associated with the context handle type is accessible.</span></span>

<span data-ttu-id="0a6cf-147">Zum Erstellen eines Kontext Handles übergibt der Client an den Server einen **\[** [**out**](out-idl.md)- **\]** , **\[** [**ref**](ref.md) - **\]** Zeiger auf ein Kontext handle.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-147">To create a context handle, the client passes to the server an **\[**[**out**](out-idl.md)**\]**, **\[**[**ref**](ref.md)**\]** pointer to a context handle.</span></span> <span data-ttu-id="0a6cf-148">(Das Kontext Handle selbst kann einen **null** -Wert oder einen nicht-**null** -Wert haben – solange sein Wert mit seinen Zeiger Attributen konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-148">(The context handle itself can have a **NULL** or non-**NULL** value—as long as its value is consistent with its pointer attributes.</span></span> <span data-ttu-id="0a6cf-149">Wenn z. b. auf den Kontext behandlertyp das **\[** [**ref**](ref.md) - **\]** Attribut angewendet wird, kann er keinen **null** -Wert aufweisen.) Ein weiteres Bindungs Handle muss bereitgestellt werden, um die Bindung zu erreichen, bis das Kontext Handle erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-149">For example, when the context handle type has the **\[**[**ref**](ref.md)**\]** attribute applied to it, it cannot have a **NULL** value.) Another binding handle must be supplied to accomplish the binding until the context handle is created.</span></span> <span data-ttu-id="0a6cf-150">Wenn kein explizites handle angegeben ist, wird eine implizite Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-150">When no explicit handle is specified, implicit binding is used.</span></span> <span data-ttu-id="0a6cf-151">Wenn kein **\[** [**implizites \_ handle**](implicit-handle.md) - **\]** Attribut vorhanden ist, wird ein automatisches Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-151">When no **\[**[**implicit\_handle**](implicit-handle.md)**\]** attribute is present, an auto handle is used.</span></span>

<span data-ttu-id="0a6cf-152">Mit der Remote Prozedur auf dem Server wird ein aktives Kontext Handle erstellt.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-152">The remote procedure on the server creates an active context handle.</span></span> <span data-ttu-id="0a6cf-153">Der Client muss dieses Kontext Handle als in- **\[** [](in.md) **\]** oder **\[ in**- **out \]** -Parameter in nachfolgenden Aufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-153">The client must use that context handle as an **\[**[**in**](in.md)**\]** or **\[in**, **out\]** parameter in subsequent calls.</span></span> <span data-ttu-id="0a6cf-154">Ein **\[ in \]**-only-Kontext Handle kann als Bindungs Handle verwendet werden, daher muss es einen Wert aufweisen, der nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-154">An **\[in\]**-only context handle can be used as a binding handle, so it must have a non-**NULL** value.</span></span> <span data-ttu-id="0a6cf-155">Ein **\[ in \]**-only-Kontext Handle reflektiert keine Zustandsänderungen auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-155">An **\[in\]**-only context handle does not reflect state changes on the server.</span></span>

<span data-ttu-id="0a6cf-156">Auf dem Server kann die aufgerufene Prozedur das Kontext Handle nach Bedarf interpretieren.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-156">On the server, the called procedure can interpret the context handle as needed.</span></span> <span data-ttu-id="0a6cf-157">Beispielsweise kann die aufgerufene Prozedur Heap Speicher zuordnen und das Kontext Handle als Zeiger auf diesen Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-157">For example, the called procedure can allocate heap storage and use the context handle as a pointer to this storage.</span></span>

<span data-ttu-id="0a6cf-158">Zum Schließen eines Kontext Handles übergibt der Client das Kontext Handle als in- **\[** [](in.md) **\]** , **\[** [**out**](out-idl.md) - **\]** Argument.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-158">To close a context handle, the client passes the context handle as an **\[**[**in**](in.md)**\]**, **\[**[**out**](out-idl.md)**\]** argument.</span></span> <span data-ttu-id="0a6cf-159">Der Server muss ein **null** -Kontext Handle zurückgeben, wenn er nicht mehr den Kontext im Auftrag des Aufrufers beibehält.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-159">The server must return a **NULL** context handle when it is no longer maintaining context on behalf of the caller.</span></span> <span data-ttu-id="0a6cf-160">Wenn das Kontext Handle z. b. eine geöffnete Datei darstellt und der-Befehl die Datei schließt, muss der Server das Kontext Handle auf **null** festlegen und an den Client zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-160">For example, if the context handle represents an open file and the call closes the file, the server must set the context handle to **NULL** and return it to the client.</span></span> <span data-ttu-id="0a6cf-161">Ein **null** -Wert ist als Bindungs Handle bei nachfolgenden Aufrufen ungültig.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-161">A **NULL** value is invalid as a binding handle on subsequent calls.</span></span>

<span data-ttu-id="0a6cf-162">Ein Kontext Handle ist nur für einen Server gültig.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-162">A context handle is only valid for one server.</span></span> <span data-ttu-id="0a6cf-163">Wenn eine Funktion über zwei handle-Parameter verfügt und das Kontext Handle nicht **null** ist, müssen die Bindungs Handles auf denselben Adressraum verweisen.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-163">When a function has two handle parameters and the context handle is not **NULL**, the binding handles must refer to the same address space.</span></span>

<span data-ttu-id="0a6cf-164">Wenn eine Funktion über ein **\[** [**in**](in.md) - **\]** oder ein **\[ in**-, **out \]** -Kontext Handle verfügt, kann Ihr Kontext Handle als Bindungs Handle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-164">When a function has an **\[**[**in**](in.md)**\]** or an **\[in**, **out\]** context handle, its context handle can be used as the binding handle.</span></span> <span data-ttu-id="0a6cf-165">In diesem Fall wird die implizite Bindung nicht verwendet, und das **\[** [**implizite \_ handle**](implicit-handle.md) - **\]** oder **\[** [**Auto \_ handle**](auto-handle.md) - **\]** Attribut wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-165">In this case, implicit binding is not used and the **\[**[**implicit\_handle**](implicit-handle.md)**\]** or **\[**[**auto\_handle**](auto-handle.md)**\]** attribute is ignored.</span></span>

<span data-ttu-id="0a6cf-166">Für Kontext Handles gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="0a6cf-166">The following restrictions apply to context handles:</span></span>

-   <span data-ttu-id="0a6cf-167">Kontext Handles können keine Array Elemente, Strukturmember oder Union-Member sein.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-167">Context handles cannot be array elements, structure members, or union members.</span></span> <span data-ttu-id="0a6cf-168">Sie können nur Parameter sein.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-168">They can only be parameters.</span></span>
-   <span data-ttu-id="0a6cf-169">Kontext Handles können nicht über die über **\[** [**Tragung \_ als**](transmit-as.md) **\]** oder das **\[** [**\_ As**](represent-as.md) - **\]** Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-169">Context handles cannot have the **\[**[**transmit\_as**](transmit-as.md)**\]** or **\[**[**represent\_as**](represent-as.md)**\]** attribute.</span></span>
-   <span data-ttu-id="0a6cf-170">Parameter, die Zeiger auf **\[** [**out**](out-idl.md) - **\]** Kontext Handles sind, müssen **\[** [**ref**](ref.md) - **\]** Zeiger sein.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-170">Parameters that are pointers to **\[**[**out**](out-idl.md)**\]** context handles must be **\[**[**ref**](ref.md)**\]** pointers.</span></span>
-   <span data-ttu-id="0a6cf-171">Ein **\[** [**im**](in.md) **\]** Kontext Handle kann als Bindungs Handle verwendet werden und darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-171">An **\[**[**in**](in.md)**\]** context handle can be used as the binding handle and cannot be **NULL**.</span></span>
-   <span data-ttu-id="0a6cf-172">Ein **\[ in**-, [**out**](out-idl.md) -Kontext Handle kann bei Eingabe **null** sein, aber nur, wenn die Prozedur einen anderen expliziten handle-Parameter aufweist.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-172">An **\[in**, [**out**](out-idl.md) context handle can be **NULL** on input, but only if the procedure has another explicit handle parameter.</span></span> <span data-ttu-id="0a6cf-173">Wenn keine anderen expliziten nicht-**null** -Kontext handle-Parameter vorhanden sind, darf der **\[ in**-, **out \]** -Kontext Handle nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-173">If there are no other explicit non-**NULL** context handle parameters, the **\[in**, **out\]** context handle cannot be **NULL**.</span></span>
-   <span data-ttu-id="0a6cf-174">Ein Kontext Handle kann nicht für Rückrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a6cf-174">A context handle cannot be used with callbacks.</span></span>

## <a name="examples"></a><span data-ttu-id="0a6cf-175">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a6cf-175">Examples</span></span>

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a><span data-ttu-id="0a6cf-176">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a6cf-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6cf-177">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-177">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-178">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-178">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-179">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-179">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-180">Client Kontext Zurücksetzung</span><span class="sxs-lookup"><span data-stu-id="0a6cf-180">Client Context Reset</span></span>](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[<span data-ttu-id="0a6cf-181">**const**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-181">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-182">Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="0a6cf-182">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="0a6cf-183">**bewältigen**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-183">**handle**</span></span>](handle.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-184">Bindung und Handles</span><span class="sxs-lookup"><span data-stu-id="0a6cf-184">Binding and Handles</span></span>](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[<span data-ttu-id="0a6cf-185">**lassen**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-185">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-186">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-186">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-187">**in**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-187">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-188">**nah**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-188">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-189">Multithread-Clients und Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="0a6cf-189">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="0a6cf-190">**/MS \_ ext**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-190">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-191">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-191">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-192">**ptr**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-192">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-193">**ref**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-193">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-194">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-194">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-195">**Rpcssdestroyclientcontext**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-195">**RpcSsDestroyClientContext**</span></span>](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[<span data-ttu-id="0a6cf-196">Server Kontext-Lauf-ab-Routine</span><span class="sxs-lookup"><span data-stu-id="0a6cf-196">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="0a6cf-197">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-197">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-198">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-198">**transmit\_as**</span></span>](transmit-as.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-199">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-199">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-200">**gem**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-200">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="0a6cf-201">**void**</span><span class="sxs-lookup"><span data-stu-id="0a6cf-201">**void**</span></span>](void.md)
</dt> </dl>

 

 