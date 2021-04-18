---
title: context_handle_serialize-Attribut
description: Das Attribut \ Kontext \_ handle \_ serialize \ ACF stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340260"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="b96c2-104">\_Attribut zum \_ Serialisieren des Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="b96c2-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="b96c2-105">Das Kontext Handle-Attribut für die **\[ \_ \_ Serialisierung \]** von ACF stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung immer serialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b96c2-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="b96c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b96c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b96c2-107">*Type-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b96c2-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-108">Alle anderen ACF-Attribute, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="b96c2-109">*Context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="b96c2-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-110">Der Bezeichner, der den Typ des Kontext Handles angibt, wie in einer [**typedef**](typedef.md) -Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="b96c2-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="b96c2-111">Dies ist der Typ, der das **\[ \_ \_ serialisierungsattribut \] des Kontext Handles** in der IDL-Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="b96c2-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="b96c2-112">*Function-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b96c2-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-113">Alle zusätzlichen ACF-Attribute, die auf die Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="b96c2-114">*function-name*</span><span class="sxs-lookup"><span data-stu-id="b96c2-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-115">Der Name der Funktion, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="b96c2-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="b96c2-116">*Parameter-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b96c2-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-117">Alle anderen ACF-Attribute, die auf den-Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b96c2-118">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="b96c2-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b96c2-119">Der Name des Parameters, wie er in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b96c2-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b96c2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b96c2-120">Remarks</span></span>

<span data-ttu-id="b96c2-121">Das Attribut zum **\[ \_ \_ serialisieren \] des Kontext Handles** identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="b96c2-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="b96c2-122">Das Attribut kann als IDL [**typedef**](typedef.md) Type-Attribut, als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="b96c2-123">Standardmäßig werden Aufrufe für Kontext Handles serialisiert, aber eine Anwendung kann [**rpcssdontserializecontext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufrufen, um dieses Standardverhalten zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b96c2-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="b96c2-124">Durch die Verwendung des **\[ Kontext \_ Handles \_ serialisieren \]** -Attributs in einer ACF-Datei wird sichergestellt, dass Aufrufe für dieses Kontext Handle serialisiert werden, auch wenn die aufrufende Anwendung die Standardserialisierung überschrieben hat.</span><span class="sxs-lookup"><span data-stu-id="b96c2-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="b96c2-125">Eine Context-Rundown-Routine ist optional.</span><span class="sxs-lookup"><span data-stu-id="b96c2-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="b96c2-126">Dieses Attribut ist in der mittleren l-Version 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b96c2-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="b96c2-127">**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert).</span><span class="sxs-lookup"><span data-stu-id="b96c2-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="b96c2-128">Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind.</span><span class="sxs-lookup"><span data-stu-id="b96c2-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="b96c2-129">Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="b96c2-130">Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="b96c2-131">Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b96c2-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="b96c2-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b96c2-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="b96c2-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b96c2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96c2-134">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="b96c2-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="b96c2-135">ACF-Attribute</span><span class="sxs-lookup"><span data-stu-id="b96c2-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="b96c2-136">**Kontext \_ handle \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="b96c2-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="b96c2-137">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="b96c2-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="b96c2-138">Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="b96c2-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="b96c2-139">**Rpcssdontserializecontext**</span><span class="sxs-lookup"><span data-stu-id="b96c2-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="b96c2-140">Server Kontext-Lauf-ab-Routine</span><span class="sxs-lookup"><span data-stu-id="b96c2-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="b96c2-141">Multithread-Clients und Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="b96c2-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="b96c2-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="b96c2-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 