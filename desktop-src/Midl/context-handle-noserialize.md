---
title: context_handle_noserialize-Attribut
description: Das \ Context \_ handle \_ noserialize \ ACF-Attribut stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.
ms.assetid: aff2484e-639b-41d2-94a9-f34ca4f2343c
keywords:
- context_handle_noserialize Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle_noserialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1394f3f2a72837df5efa3b74bd2672e39c3c3b12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724961"
---
# <a name="context_handle_noserialize-attribute"></a><span data-ttu-id="284cd-104">Kontext \_ handle- \_ noserialize-Attribut</span><span class="sxs-lookup"><span data-stu-id="284cd-104">context\_handle\_noserialize attribute</span></span>

<span data-ttu-id="284cd-105">Das **\[ Kontext \_ \_ handle \]** -ACF-Attribut stellt sicher, dass ein Kontext Handle unabhängig vom Standardverhalten der Anwendung niemals serialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="284cd-105">The **\[context\_handle\_noserialize\]** ACF attribute guarantees that a context handle will never be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_noserialize [ , type-acf-attribute-list ] ] context-handle-type

[context_handle_noserialize [, function-acf-attribute-list ] ] function-name( );

function-name (   [context_handle_noserialize 
  [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="284cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="284cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284cd-107">*Type-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="284cd-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-108">Alle anderen ACF-Attribute, die auf den Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-109">*Context-Handle-type*</span><span class="sxs-lookup"><span data-stu-id="284cd-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-110">Der Bezeichner, der den Typ des Kontext Handles angibt, wie in einer [**typedef**](typedef.md) -Deklaration definiert.</span><span class="sxs-lookup"><span data-stu-id="284cd-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="284cd-111">Dies ist der Typ, der das [**\[ Kontext \_ handle \]**](context-handle.md) -Attribut in der IDL-Datei empfängt.</span><span class="sxs-lookup"><span data-stu-id="284cd-111">This is the type that receives the [**\[context\_handle\]**](context-handle.md) attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-112">*Function-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="284cd-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-113">Alle zusätzlichen ACF-Attribute, die auf die Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-114">*function-name*</span><span class="sxs-lookup"><span data-stu-id="284cd-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-115">Der Name der Funktion, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="284cd-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-116">*Parameter-ACF-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="284cd-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-117">Alle anderen ACF-Attribute, die auf den-Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="284cd-118">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="284cd-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="284cd-119">Der Name des Parameters, wie er in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="284cd-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="284cd-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="284cd-120">Remarks</span></span>

<span data-ttu-id="284cd-121">Das [**\[ Kontext \_ handle \]**](context-handle.md) -Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="284cd-121">The [**\[context\_handle\]**](context-handle.md) attribute identifies a binding handle that maintains context, or state information, on the server between remote procedure calls.</span></span> <span data-ttu-id="284cd-122">Das Attribut kann als IDL [**typedef**](typedef.md) Type-Attribut, als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="284cd-123">Standardmäßig werden Aufrufe für Kontext Handles serialisiert.</span><span class="sxs-lookup"><span data-stu-id="284cd-123">By default, calls on context handles are serialized.</span></span> <span data-ttu-id="284cd-124">Eine Anwendung kann [**rpcssdontserializecontext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) aufgerufen werden, um dieses Standardverhalten zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="284cd-124">An application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="284cd-125">Durch die Verwendung des [**\[ Kontext \_ handle \]**](context-handle.md) -Attributs in einer ACF-Datei wird sichergestellt, dass Aufrufe für dieses Kontext Handle unabhängig vom Verhalten der aufrufenden Anwendung nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-125">Using the [**\[context\_handle\]**](context-handle.md) attribute in an ACF file guarantees that calls on this particular context handle will not be serialized, regardless of the calling application's behavior.</span></span> <span data-ttu-id="284cd-126">Das Bereitstellen einer Kontext-Rundown-Routine ist optional.</span><span class="sxs-lookup"><span data-stu-id="284cd-126">Providing a context rundown routine is optional.</span></span>

<span data-ttu-id="284cd-127">Dieses Attribut ist in der mittleren l-Version 5,0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="284cd-127">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="284cd-128">**Windows Server 2003 und Windows XP oder höher:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert).</span><span class="sxs-lookup"><span data-stu-id="284cd-128">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="284cd-129">Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind.</span><span class="sxs-lookup"><span data-stu-id="284cd-129">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="284cd-130">Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-130">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="284cd-131">Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-131">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="284cd-132">Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="284cd-132">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="284cd-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="284cd-133">Examples</span></span>

``` syntax
typedef [context_handle_noserialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_noserialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="284cd-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="284cd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284cd-135">ACF-Attribute</span><span class="sxs-lookup"><span data-stu-id="284cd-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="284cd-136">**Kontext \_ handle- \_ Serialisierung**</span><span class="sxs-lookup"><span data-stu-id="284cd-136">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="284cd-137">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="284cd-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="284cd-138">Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="284cd-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="284cd-139">**Rpcssdontserializecontext**</span><span class="sxs-lookup"><span data-stu-id="284cd-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="284cd-140">Server Kontext-Lauf-ab-Routine</span><span class="sxs-lookup"><span data-stu-id="284cd-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="284cd-141">Multithread-Clients und Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="284cd-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="284cd-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="284cd-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 