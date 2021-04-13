---
title: Rückruf Attribut
description: Das Attribut \ Callback \ deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist. Rückruf Funktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- Rückruf Attribut-Mittel l
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390253"
---
# <a name="callback-attribute"></a><span data-ttu-id="556a5-105">Rückruf Attribut</span><span class="sxs-lookup"><span data-stu-id="556a5-105">callback attribute</span></span>

<span data-ttu-id="556a5-106">Das **\[ Callback \]** -Attribut deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="556a5-106">The **\[callback\]** attribute declares a static callback function that exists on the client side of the distributed application.</span></span> <span data-ttu-id="556a5-107">Rückruf Funktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="556a5-107">Callback functions provide a way for the server to execute code on the client.</span></span>

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a><span data-ttu-id="556a5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="556a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="556a5-109">*Function-attr-List*</span><span class="sxs-lookup"><span data-stu-id="556a5-109">*function-attr-list*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-110">Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten.</span><span class="sxs-lookup"><span data-stu-id="556a5-110">Specifies zero or more attributes that apply to the function.</span></span> <span data-ttu-id="556a5-111">Gültige Funktions Attribute sind **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="556a5-111">Valid function attributes are **\[**[**local**](local.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the usage attributes **\[**[**string**](string.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, and **\[**[**context\_handle**](context-handle.md)**\]**.</span></span> <span data-ttu-id="556a5-112">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="556a5-112">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="556a5-113">*Typspezifizierer*</span><span class="sxs-lookup"><span data-stu-id="556a5-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-114">Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an.</span><span class="sxs-lookup"><span data-stu-id="556a5-114">Specifies a [base\_type](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type, or type identifier.</span></span> <span data-ttu-id="556a5-115">Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="556a5-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="556a5-116">*PTR-Deklarator*</span><span class="sxs-lookup"><span data-stu-id="556a5-116">*ptr-declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-117">Gibt 0 (null) oder mehr Zeiger Deklaratoren an.</span><span class="sxs-lookup"><span data-stu-id="556a5-117">Specifies zero or more pointer declarators.</span></span> <span data-ttu-id="556a5-118">Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.</span><span class="sxs-lookup"><span data-stu-id="556a5-118">A pointer declarator is the same as the pointer declarator used in C; it is constructed from the \* designator, modifiers such as **far**, and the qualifier [**const**](const.md).</span></span>

</dd> <dt>

<span data-ttu-id="556a5-119">*function-name*</span><span class="sxs-lookup"><span data-stu-id="556a5-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-120">Gibt den Namen der Remote Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="556a5-120">Specifies the name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="556a5-121">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="556a5-121">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-122">Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="556a5-122">Specifies zero or more directional attributes, field attributes, usage attributes, and pointer attributes appropriate for the specified parameter type.</span></span> <span data-ttu-id="556a5-123">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="556a5-123">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="556a5-124">*Deklarator*</span><span class="sxs-lookup"><span data-stu-id="556a5-124">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="556a5-125">Gibt einen Standard-C-Deklarator an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="556a5-125">Specifies a standard C declarator such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="556a5-126">Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="556a5-126">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="556a5-127">Der Parameter-Name-Bezeichner ist optional.</span><span class="sxs-lookup"><span data-stu-id="556a5-127">The parameter-name identifier is optional.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="556a5-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="556a5-128">Remarks</span></span>

<span data-ttu-id="556a5-129">Die **\[ Rückruf \]** Funktion ist hilfreich, wenn der Server Informationen vom Client abrufen muss.</span><span class="sxs-lookup"><span data-stu-id="556a5-129">The **\[callback\]** function is useful when the server must obtain information from the client.</span></span> <span data-ttu-id="556a5-130">, Wenn Server Anwendungen unter Windows 3 unterstützt werden. *x*, der Server kann eine Remote Prozedur auf Windows 3 abrufen. *x* -Server, um die benötigten Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="556a5-130">If server applications were supported on Windows 3.*x*, the server could make a call to a remote procedure on the Windows 3.*x* server to obtain the needed information.</span></span> <span data-ttu-id="556a5-131">Die Rückruffunktion erreicht denselben Zweck und ermöglicht dem Server, Informationen im Kontext des ursprünglichen Aufrufs abzufragen.</span><span class="sxs-lookup"><span data-stu-id="556a5-131">The callback function accomplishes the same purpose and lets the server query the client for information in the context of the original call.</span></span>

<span data-ttu-id="556a5-132">Rückrufe sind Sonderfälle von Remote aufrufen, die als Teil eines einzelnen Threads ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="556a5-132">Callbacks are special cases of remote calls that execute as part of a single thread.</span></span> <span data-ttu-id="556a5-133">Ein Rückruf wird im Kontext eines Remote Aufrufs ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="556a5-133">A callback is issued in the context of a remote call.</span></span> <span data-ttu-id="556a5-134">Alle Remote Prozeduren, die als Teil derselben Schnittstelle wie die statische Rückruffunktion definiert sind, können die Rückruffunktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="556a5-134">Any remote procedure defined as part of the same interface as the static callback function can call the callback function.</span></span>

<span data-ttu-id="556a5-135">Beachten Sie, dass die Verwendung von \[ Callback bei der \] Multithreadprogrammierung nicht empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="556a5-135">It is important to note that the use of \[callback\] is not recommended in multi-thread programming.</span></span> <span data-ttu-id="556a5-136">Als Single Thread-Programmierfunktion ist Sie nicht für die Unterstützung der Sicherheitsanforderungen, die eine Multithreadumgebung bereitstellt, bereit.</span><span class="sxs-lookup"><span data-stu-id="556a5-136">As a single-thread programming function, it is not equipped to support the security demands a multi-thread environment provides.</span></span>

<span data-ttu-id="556a5-137">Die **rpccancelthread** -Funktion kann nicht zum Abbrechen eines Aufrufs verwendet werden, der möglicherweise einen statischen Rückruf versendet.</span><span class="sxs-lookup"><span data-stu-id="556a5-137">The **RpcCancelThread** function cannot be used to cancel a call that may dispatch a static callback.</span></span> <span data-ttu-id="556a5-138">Wenn ein bestimmter Remote Prozedur Aufrufs nie zu einem Rückruf führt, kann er abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="556a5-138">If a particular remote procedure call will never result in a callback, then it can be canceled.</span></span> <span data-ttu-id="556a5-139">Andernfalls kann ein-Rückruf nur abgebrochen werden, wenn sichergestellt werden kann, dass kein Rückruf für ihn ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="556a5-139">Otherwise, a call can be canceled only if it can be guaranteed that a callback for it has not been issued.</span></span>

<span data-ttu-id="556a5-140">Nur die Verbindungs orientierten und lokalen Protokoll Sequenzen unterstützen das Rückruf Attribut.</span><span class="sxs-lookup"><span data-stu-id="556a5-140">Only the connection-oriented and local-protocol sequences support the callback attribute.</span></span> <span data-ttu-id="556a5-141">Die Größe der \[ out \] -Daten für Rückrufe über die lokale Protokoll Sequenz ist auf 150 Bytes beschränkt.</span><span class="sxs-lookup"><span data-stu-id="556a5-141">The size of the \[out\] data for callbacks over the local-protocol sequence is limited to 150 bytes.</span></span> <span data-ttu-id="556a5-142">Wenn eine RPC-Schnittstelle eine verbindungslose (Datagram) Protokoll Sequenz verwendet, schlagen Aufrufe von Prozeduren mit dem Rückruf Attribut fehl.</span><span class="sxs-lookup"><span data-stu-id="556a5-142">If an RPC interface uses a connectionless (datagram) protocol sequence, calls to procedures with the callback attribute will fail.</span></span>

<span data-ttu-id="556a5-143">Handles können nicht als Parameter in Rückruf Funktionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="556a5-143">Handles cannot be used as parameters in callback functions.</span></span> <span data-ttu-id="556a5-144">Da Rückrufe immer im Kontext eines-Aufrufes ausgeführt werden, wird das Bindungs handle, das vom Client für den Aufruf des Servers verwendet wird, auch als Bindungs Handle vom Server zum Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="556a5-144">Because callbacks always execute in the context of a call, the binding handle used by the client to make the call to the server is also used as the binding handle from the server to the client.</span></span>

<span data-ttu-id="556a5-145">Rückrufe können in beliebiger Tiefe verschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="556a5-145">Callbacks can nest to any depth.</span></span>

## <a name="examples"></a><span data-ttu-id="556a5-146">Beispiele</span><span class="sxs-lookup"><span data-stu-id="556a5-146">Examples</span></span>

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a><span data-ttu-id="556a5-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="556a5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="556a5-148">**Mikro**</span><span class="sxs-lookup"><span data-stu-id="556a5-148">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="556a5-149">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="556a5-149">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="556a5-150">**const**</span><span class="sxs-lookup"><span data-stu-id="556a5-150">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="556a5-151">**Kontext \_ handle**</span><span class="sxs-lookup"><span data-stu-id="556a5-151">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="556a5-152">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="556a5-152">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="556a5-153">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="556a5-153">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="556a5-154">**lassen**</span><span class="sxs-lookup"><span data-stu-id="556a5-154">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="556a5-155">**nah**</span><span class="sxs-lookup"><span data-stu-id="556a5-155">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="556a5-156">**/osf**</span><span class="sxs-lookup"><span data-stu-id="556a5-156">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="556a5-157">**ref**</span><span class="sxs-lookup"><span data-stu-id="556a5-157">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="556a5-158">**ptr**</span><span class="sxs-lookup"><span data-stu-id="556a5-158">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="556a5-159">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="556a5-159">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="556a5-160">**struct**</span><span class="sxs-lookup"><span data-stu-id="556a5-160">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="556a5-161">**Union**</span><span class="sxs-lookup"><span data-stu-id="556a5-161">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="556a5-162">**gem**</span><span class="sxs-lookup"><span data-stu-id="556a5-162">**unique**</span></span>](unique.md)
</dt> <dt>

[<span data-ttu-id="556a5-163">**Rpccancelthread**</span><span class="sxs-lookup"><span data-stu-id="556a5-163">**RpcCancelThread**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 