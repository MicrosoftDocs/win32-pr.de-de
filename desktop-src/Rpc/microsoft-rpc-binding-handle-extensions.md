---
title: Microsoft RPC-Binding-Handle Erweiterungen
description: Die Microsoft-Erweiterungen der IDL-Sprache unterstützen mehrere handle-Parameter, die in anderen Positionen als dem ersten, äußersten linken Parameter angezeigt werden.
ms.assetid: 084b0d8e-0c8a-43b9-b3ae-4f69cab3a2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a947c10465cb24012be9c3f845fbd874f9de0567
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039753"
---
# <a name="microsoft-rpc-binding-handle-extensions"></a><span data-ttu-id="d3435-103">Microsoft RPC-Binding-Handle Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="d3435-103">Microsoft RPC Binding-Handle Extensions</span></span>

<span data-ttu-id="d3435-104">Die Microsoft-Erweiterungen der IDL-Sprache unterstützen mehrere handle-Parameter, die in anderen Positionen als dem ersten, äußersten linken Parameter angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3435-104">The Microsoft extensions to the IDL language support multiple handle parameters that appear in positions other than the first, leftmost, parameter.</span></span> <span data-ttu-id="d3435-105">In den folgenden Schritten wird die Sequenz beschrieben, die der-Mittelwert Compiler durchläuft, um den Bindungs handle-Parameter im DCE-Kompatibilitätsmodus (/**eines Zertifikats**) und im Standardmodus (Microsoft-erweiterter Modus) aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d3435-105">The following steps describe the sequence that the MIDL compiler goes through to resolve the binding-handle parameter in DCE-compatibility mode (/**osf**), and in default (Microsoft-extended) mode.</span></span>

## <a name="dce-compatibility-mode"></a><span data-ttu-id="d3435-106">DCE-Kompatibilitätsmodus</span><span class="sxs-lookup"><span data-stu-id="d3435-106">DCE-compatibility mode</span></span>

-   <span data-ttu-id="d3435-107">Bindungs handle, das an erster Stelle angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3435-107">Binding handle that appears in first position.</span></span>
-   <span data-ttu-id="d3435-108">Ganz links \[ [**in**](/windows/desktop/Midl/in), [**Kontext \_ handle**](/windows/desktop/Midl/context-handle) - \] Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3435-108">Leftmost \[[**in**](/windows/desktop/Midl/in), [**context\_handle**](/windows/desktop/Midl/context-handle)\] parameter.</span></span>
-   <span data-ttu-id="d3435-109">Implizites Bindungs handle, das vom \[ [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ handle**](/windows/desktop/Midl/auto-handle)angegeben wird \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-109">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="d3435-110">Wenn keine ACF vorhanden ist, wird die Verwendung des \[ **automatischen \_ Handles** standardmäßig verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-110">If no ACF present, default to use of \[**auto\_handle**\].</span></span>

## <a name="default-mode"></a><span data-ttu-id="d3435-111">Standardmodus</span><span class="sxs-lookup"><span data-stu-id="d3435-111">Default mode</span></span>

-   <span data-ttu-id="d3435-112">Ganz links explizites Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-112">Leftmost explicit binding handle.</span></span>
-   <span data-ttu-id="d3435-113">Implizites Bindungs handle, das vom \[ [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ handle**](/windows/desktop/Midl/auto-handle)angegeben wird \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-113">Implicit binding handle specified by \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>
-   <span data-ttu-id="d3435-114">Wenn keine ACF vorhanden ist, wird die Verwendung des \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)standardmäßig verwendet \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-114">If no ACF present, default to use of \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="d3435-115">DCE-IDL-Compiler suchen nach einem expliziten Bindungs Handle als ersten Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3435-115">DCE IDL compilers look for an explicit binding handle as the first parameter.</span></span> <span data-ttu-id="d3435-116">Wenn der erste Parameter kein Bindungs Handle und mindestens ein Kontext Handle angegeben ist, wird das äußerste Kontext Handle als Bindungs Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3435-116">When the first parameter is not a binding handle and one or more context handles are specified, the leftmost context handle is used as the binding handle.</span></span> <span data-ttu-id="d3435-117">Wenn der erste Parameter kein Handle ist und keine Kontext Handles vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des \[ [**impliziten \_ Handles**](/windows/desktop/Midl/implicit-handle) \] oder \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)des ACF-Attributs \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-117">When the first parameter is not a handle and there are no context handles, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="d3435-118">Die Microsoft-Erweiterungen für die IDL ermöglichen, dass das Bindungs Handle an einer anderen Position als der erste Parameter steht.</span><span class="sxs-lookup"><span data-stu-id="d3435-118">The Microsoft extensions to the IDL allow the binding handle to be in a position other than the first parameter.</span></span> <span data-ttu-id="d3435-119">Der am weitesten links stehende \[ [](/windows/desktop/Midl/in) \] Parameter des expliziten Handles – ob es sich um ein Primitives, vom Programmierer definiertes oder Kontext Handle handelt – ist das Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-119">The leftmost \[[**in**](/windows/desktop/Midl/in)\] explicit-handle parameter–whether it is a primitive, programmer-defined, or context handle–is the binding handle.</span></span> <span data-ttu-id="d3435-120">Wenn keine handle-Parameter vorhanden sind, verwendet die Prozedur die implizite Bindung mithilfe des \[ [**impliziten \_ Handles**](/windows/desktop/Midl/implicit-handle) \] oder des \[ [**automatischen \_ Handles**](/windows/desktop/Midl/auto-handle)des ACF-Attributs \] .</span><span class="sxs-lookup"><span data-stu-id="d3435-120">When there are no handle parameters, the procedure uses implicit binding using the ACF attribute \[[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)\] or \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\].</span></span>

<span data-ttu-id="d3435-121">Die folgenden Regeln gelten sowohl für den DCE-Kompatibilitätsmodus (/OSF) als auch für den Standardmodus:</span><span class="sxs-lookup"><span data-stu-id="d3435-121">The following rules apply to both DCE-compatibility (/osf) mode and default mode:</span></span>

-   <span data-ttu-id="d3435-122">Die automatische handle-Bindung wird verwendet, wenn keine ACF vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d3435-122">Auto-handle binding is used when no ACF is present.</span></span>
-   <span data-ttu-id="d3435-123">Explizit \[ [**in**](/windows/desktop/Midl/in) \] oder \[ **in**, [**out**](/windows/desktop/Midl/out-idl) - \] Handles für eine einzelne Funktion vor allen impliziten Bindungen, die für die Schnittstelle angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="d3435-123">Explicit \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, [**out**](/windows/desktop/Midl/out-idl)\] handles for an individual function preempt any implicit binding specified for the interface.</span></span>
-   <span data-ttu-id="d3435-124">Mehrere \[ [](/windows/desktop/Midl/in) \] primitive Handles in oder \[ **in** \] werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3435-124">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] primitive handles are not supported.</span></span>
-   <span data-ttu-id="d3435-125">Mehrere \[ [](/windows/desktop/Midl/in) \] \[ explizite Kontext Handles in oder **in** \] sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="d3435-125">Multiple \[[**in**](/windows/desktop/Midl/in)\] or \[**in**, out\] explicit context handles are allowed.</span></span>
-   <span data-ttu-id="d3435-126">Alle vom Programmierer definierten handle-Parameter Außer dem Parameter für den Bindungs handle werden als Daten behandelt, die für den Programmierer definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d3435-126">All programmer-defined handle parameters except the binding-handle parameter are treated as transmissible data.</span></span>

<span data-ttu-id="d3435-127">Die folgende Tabelle enthält Beispiele, und es wird beschrieben, wie Bindungs Handles in den einzelnen compilermodi zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d3435-127">The following table contains examples and describes how binding handles are assigned in each compiler mode.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3435-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d3435-128">Example</span></span></th>
<th><span data-ttu-id="d3435-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3435-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc1( void );</code></pre></td>
<td><span data-ttu-id="d3435-130">Es wurde kein explizites handle angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3435-130">No explicit handle is specified.</span></span> <span data-ttu-id="d3435-131">Das implizite Bindungs handle, das durch [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] oder [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>] angegeben wird, wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3435-131">The implicit binding handle, specified by [ <a href="/windows/desktop/Midl/implicit-handle">implicit_handle</a>] or [ <a href="/windows/desktop/Midl/auto-handle">auto_handle</a>], is used.</span></span> <span data-ttu-id="d3435-132">Wenn keine ACF vorhanden ist, wird ein automatisches Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3435-132">When no ACF is present, an auto handle is used.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>void proc2([in] handle_t H,
           [in] short s );</code></pre></td>
<td><span data-ttu-id="d3435-133">Es wurde ein explizites Handle vom Typ handle_t angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3435-133">An explicit handle of type handle_t is specified.</span></span> <span data-ttu-id="d3435-134">Der Parameter <em>H</em> ist das Bindungs Handle für die Prozedur.</span><span class="sxs-lookup"><span data-stu-id="d3435-134">The parameter <em>H</em> is the binding handle for the procedure.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>void proc3([in] short s,
           [in] handle_t H );</code></pre></td>
<td><span data-ttu-id="d3435-135">Der erste Parameter ist kein handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-135">The first parameter is not a handle.</span></span> <span data-ttu-id="d3435-136">Im Standardmodus ist der am weitesten links stehende handle-Parameter <em>H</em>, der Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-136">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="d3435-137">Im/OSF-Modus wird die implizite Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3435-137">In /osf mode, implicit binding is used.</span></span> <span data-ttu-id="d3435-138">Ein Fehler wird gemeldet, da der zweite Parameter als nicht zulässig erwartet wird und handle_t nicht übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="d3435-138">An error is reported because the second parameter is expected to be transmissible, and handle_t cannot be transmitted.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>typedef [handle] short * MY_HDL;

void proc1([in] short s,
           [in] MY_HDL H );</code></pre></td>
<td><span data-ttu-id="d3435-139">Der erste Parameter ist kein handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-139">The first parameter is not a handle.</span></span> <span data-ttu-id="d3435-140">Im Standardmodus ist der am weitesten links stehende handle-Parameter <em>H</em>, der Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-140">In default mode, the leftmost handle parameter, <em>H</em>, is the binding handle.</span></span> <span data-ttu-id="d3435-141">Die stufs nennen die vom Benutzer bereitgestellten Routinen MY_HDL_bind und MY_HDL_unbind.</span><span class="sxs-lookup"><span data-stu-id="d3435-141">The stubs call the user-supplied routines MY_HDL_bind and MY_HDL_unbind.</span></span> <span data-ttu-id="d3435-142">Im/OSF-Modus wird die implizite Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3435-142">In/osf mode, implicit binding is used.</span></span> <span data-ttu-id="d3435-143">Der vom Programmierer definierte handle-Parameter <em>H</em> wird als nicht übertragbare Daten behandelt.</span><span class="sxs-lookup"><span data-stu-id="d3435-143">The programmer-defined handle parameter <em>H</em> is treated as transmissible data.</span></span></td>
</tr>
<tr class="odd">
<td><pre class="syntax" data-space="preserve"><code>Typedef [handle] short * MY_HDL;

void proc1([in] MY_HDL H, 
           [in] MY_HDL p );</code></pre></td>
<td><span data-ttu-id="d3435-144">Der erste Parameter ist ein Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-144">The first parameter is a binding handle.</span></span> <span data-ttu-id="d3435-145">Der Parameter <em>H</em> ist der Bindungs handle-Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3435-145">The parameter <em>H</em> is the binding-handle parameter.</span></span> <span data-ttu-id="d3435-146">Der zweite von einem Programmierer definierte handle-Parameter wird als Transaktionsdaten behandelt.</span><span class="sxs-lookup"><span data-stu-id="d3435-146">The second programmer-defined handle parameter is treated as transmissible data.</span></span></td>
</tr>
<tr class="even">
<td><pre class="syntax" data-space="preserve"><code>Typedef [context_handle] 
void * CTXT_HDL;

void proc1([in] short s,
           [in] long l,
           [in] CTXT_HDL H ,
           [in] char c);</code></pre></td>
<td><span data-ttu-id="d3435-147">Das Bindungs Handle ist ein Kontext handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-147">The binding handle is a context handle.</span></span> <span data-ttu-id="d3435-148">Der Parameter <em>H</em> ist das Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="d3435-148">The parameter <em>H</em> is the binding handle.</span></span></td>
</tr>
</tbody>
</table>



 

 

 