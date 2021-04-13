---
title: Prozedur Header Deskriptor
description: Die Kopfzeile wurde im Laufe der Lebensdauer der NDR-Engine mehrmals erweitert. Der aktuelle Compiler generiert abhängig vom Modus des Compilers weiterhin verschiedene Header. Neuere Header sind jedoch eine supermenge der älteren Header.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473901"
---
# <a name="procedure-header-descriptor"></a><span data-ttu-id="bd60b-105">Prozedur Header Deskriptor</span><span class="sxs-lookup"><span data-stu-id="bd60b-105">Procedure Header Descriptor</span></span>

<span data-ttu-id="bd60b-106">Die Kopfzeile wurde im Laufe der Lebensdauer der NDR-Engine mehrmals erweitert.</span><span class="sxs-lookup"><span data-stu-id="bd60b-106">The header has been extended several times over the life of the NDR engine.</span></span> <span data-ttu-id="bd60b-107">Der aktuelle Compiler generiert abhängig vom Modus des Compilers weiterhin verschiedene Header.</span><span class="sxs-lookup"><span data-stu-id="bd60b-107">The current compiler still generates different headers depending on the mode of the compiler.</span></span> <span data-ttu-id="bd60b-108">Neuere Header sind jedoch eine supermenge der älteren Header.</span><span class="sxs-lookup"><span data-stu-id="bd60b-108">However, more recent headers are a superset of the older ones.</span></span>

## <a name="the-old-oi-header"></a><span data-ttu-id="bd60b-109">Der alte – Oi-Header</span><span class="sxs-lookup"><span data-stu-id="bd60b-109">The Old –Oi Header</span></span>

<span data-ttu-id="bd60b-110">Der Header weist das folgende Format auf:</span><span class="sxs-lookup"><span data-stu-id="bd60b-110">The header has the following format:</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="bd60b-111">Where Handle \_ Type<1> kann einer der in der folgenden Tabelle dargestellten Werte sein.</span><span class="sxs-lookup"><span data-stu-id="bd60b-111">Where handle\_type<1> can be one of the values shown in the following table.</span></span>



| <span data-ttu-id="bd60b-112">Hex</span><span class="sxs-lookup"><span data-stu-id="bd60b-112">Hex</span></span> | <span data-ttu-id="bd60b-113">Handle</span><span class="sxs-lookup"><span data-stu-id="bd60b-113">Handle</span></span>               |
|-----|----------------------|
| <span data-ttu-id="bd60b-114">31</span><span class="sxs-lookup"><span data-stu-id="bd60b-114">31</span></span>  | <span data-ttu-id="bd60b-115">Allgemeine FC- \_ Bindung \_</span><span class="sxs-lookup"><span data-stu-id="bd60b-115">FC\_BIND\_GENERIC</span></span>    |
| <span data-ttu-id="bd60b-116">32</span><span class="sxs-lookup"><span data-stu-id="bd60b-116">32</span></span>  | <span data-ttu-id="bd60b-117">FC- \_ Bindungs \_ primitiv</span><span class="sxs-lookup"><span data-stu-id="bd60b-117">FC\_BIND\_PRIMITIVE</span></span>  |
| <span data-ttu-id="bd60b-118">33</span><span class="sxs-lookup"><span data-stu-id="bd60b-118">33</span></span>  | <span data-ttu-id="bd60b-119">Automatisches FC- \_ \_ handle</span><span class="sxs-lookup"><span data-stu-id="bd60b-119">FC\_AUTO\_HANDLE</span></span>     |
| <span data-ttu-id="bd60b-120">34</span><span class="sxs-lookup"><span data-stu-id="bd60b-120">34</span></span>  | <span data-ttu-id="bd60b-121">FC- \_ Rückruf \_ handle</span><span class="sxs-lookup"><span data-stu-id="bd60b-121">FC\_CALLBACK\_HANDLE</span></span> |
| <span data-ttu-id="bd60b-122">0</span><span class="sxs-lookup"><span data-stu-id="bd60b-122">0</span></span>   | <span data-ttu-id="bd60b-123">(explizites handle)</span><span class="sxs-lookup"><span data-stu-id="bd60b-123">(explicit handle)</span></span>    |



 

<span data-ttu-id="bd60b-124">Wenn der Handle- \_ Typ<1> Feld ungleich 0 (null) ist, verwendet die Prozedur ein implizites Handle der bestimmten Art.</span><span class="sxs-lookup"><span data-stu-id="bd60b-124">If the handle\_type<1> field is nonzero, then the procedure uses an implicit handle of the indicated kind.</span></span> <span data-ttu-id="bd60b-125">Weitere Informationen finden Sie im Thema [Handles](handles.md) .</span><span class="sxs-lookup"><span data-stu-id="bd60b-125">See the [Handles](handles.md) topic for a more information.</span></span> <span data-ttu-id="bd60b-126">Wenn der Handle \_ -Typ<1> Feld 0 (null) ist, ist das für die Bindung verwendete Handle einer der Parameter der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="bd60b-126">If the handle\_type<1> field is zero, the handle used for binding is one of the procedure's parameters.</span></span>

<span data-ttu-id="bd60b-127">Explizite Handles können primitiv, generisch und Kontext sein. die letzte hat das folgende FC-Token.</span><span class="sxs-lookup"><span data-stu-id="bd60b-127">Explicit handles can be primitive, generic, and context; the last one has the following FC token.</span></span>



| <span data-ttu-id="bd60b-128">Hex</span><span class="sxs-lookup"><span data-stu-id="bd60b-128">Hex</span></span> | <span data-ttu-id="bd60b-129">Handle</span><span class="sxs-lookup"><span data-stu-id="bd60b-129">Handle</span></span>            |
|-----|-------------------|
| <span data-ttu-id="bd60b-130">30</span><span class="sxs-lookup"><span data-stu-id="bd60b-130">30</span></span>  | <span data-ttu-id="bd60b-131">FC- \_ Bindungs \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="bd60b-131">FC\_BIND\_CONTEXT</span></span> |



 

<span data-ttu-id="bd60b-132">Gemäß der Konvention ist der Handle-Typ für DCOM-Schnittstellen das automatische FC- \_ \_ handle.</span><span class="sxs-lookup"><span data-stu-id="bd60b-132">By convention, the handle type for DCOM interfaces is FC\_AUTO\_HANDLE.</span></span>

<span data-ttu-id="bd60b-133">Das \_> Feld Oi Flags<1 ist eine 8-Bit-Maske der folgenden Flags.</span><span class="sxs-lookup"><span data-stu-id="bd60b-133">The Oi\_flags<1> field is an 8-bit mask of the following flags.</span></span>



| <span data-ttu-id="bd60b-134">Hex</span><span class="sxs-lookup"><span data-stu-id="bd60b-134">Hex</span></span> | <span data-ttu-id="bd60b-135">Flag</span><span class="sxs-lookup"><span data-stu-id="bd60b-135">Flag</span></span>                         | <span data-ttu-id="bd60b-136">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bd60b-136">Meaning</span></span>                                  |
|-----|------------------------------|------------------------------------------|
| <span data-ttu-id="bd60b-137">01</span><span class="sxs-lookup"><span data-stu-id="bd60b-137">01</span></span>  | <span data-ttu-id="bd60b-138">Oi \_ Full \_ ptr \_ verwendet</span><span class="sxs-lookup"><span data-stu-id="bd60b-138">Oi\_FULL\_PTR\_USED</span></span>          | <span data-ttu-id="bd60b-139">Verwendet das vollständige Zeiger Paket.</span><span class="sxs-lookup"><span data-stu-id="bd60b-139">Uses the full pointer package.</span></span>           |
| <span data-ttu-id="bd60b-140">02</span><span class="sxs-lookup"><span data-stu-id="bd60b-140">02</span></span>  | <span data-ttu-id="bd60b-141">\_Verwendete Oi RPCSS- \_ Zuweisung \_</span><span class="sxs-lookup"><span data-stu-id="bd60b-141">Oi\_RPCSS\_ALLOC\_USED</span></span>       | <span data-ttu-id="bd60b-142">Verwendet das RPCSS-Speicher Paket.</span><span class="sxs-lookup"><span data-stu-id="bd60b-142">Uses the RpcSs memory package.</span></span>           |
| <span data-ttu-id="bd60b-143">04</span><span class="sxs-lookup"><span data-stu-id="bd60b-143">04</span></span>  | <span data-ttu-id="bd60b-144">Oi- \_ Objekt Prozedur \_</span><span class="sxs-lookup"><span data-stu-id="bd60b-144">Oi\_OBJECT\_PROC</span></span>             | <span data-ttu-id="bd60b-145">Eine Prozedur in einer Objektschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bd60b-145">A procedure in an object interface.</span></span>      |
| <span data-ttu-id="bd60b-146">08</span><span class="sxs-lookup"><span data-stu-id="bd60b-146">08</span></span>  | <span data-ttu-id="bd60b-147">Oi \_ hat \_ rpcflags</span><span class="sxs-lookup"><span data-stu-id="bd60b-147">Oi\_HAS\_RPCFLAGS</span></span>            | <span data-ttu-id="bd60b-148">Die Prozedur verfügt über nicht-NULL-RPC-Flags.</span><span class="sxs-lookup"><span data-stu-id="bd60b-148">The procedure has nonzero Rpc flags.</span></span>     |
| <span data-ttu-id="bd60b-149">10</span><span class="sxs-lookup"><span data-stu-id="bd60b-149">10</span></span>  | <span data-ttu-id="bd60b-150">Zählen\_\*</span><span class="sxs-lookup"><span data-stu-id="bd60b-150">Oi\_\*</span></span>                       | <span data-ttu-id="bd60b-151">Überladen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-151">Overloaded.</span></span>                              |
| <span data-ttu-id="bd60b-152">20</span><span class="sxs-lookup"><span data-stu-id="bd60b-152">20</span></span>  | <span data-ttu-id="bd60b-153">Zählen\_\*</span><span class="sxs-lookup"><span data-stu-id="bd60b-153">Oi\_\*</span></span>                       | <span data-ttu-id="bd60b-154">Überladen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-154">Overloaded.</span></span>                              |
| <span data-ttu-id="bd60b-155">40</span><span class="sxs-lookup"><span data-stu-id="bd60b-155">40</span></span>  | <span data-ttu-id="bd60b-156">Oi \_ verwenden \_ neuer \_ Init- \_ Routinen</span><span class="sxs-lookup"><span data-stu-id="bd60b-156">Oi\_USE\_NEW\_INIT\_ROUTINES</span></span> | <span data-ttu-id="bd60b-157">Verwendet Windows NT 3.5 Beta2 + init-Routinen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-157">Uses Windows NT3.5 Beta2+ init routines.</span></span> |
| <span data-ttu-id="bd60b-158">80</span><span class="sxs-lookup"><span data-stu-id="bd60b-158">80</span></span>  |                              | <span data-ttu-id="bd60b-159">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd60b-159">Unused.</span></span>                                  |



 

<span data-ttu-id="bd60b-160">Die folgenden Flags sind überladen.</span><span class="sxs-lookup"><span data-stu-id="bd60b-160">The following flags are overloaded.</span></span>



| <span data-ttu-id="bd60b-161">Hex</span><span class="sxs-lookup"><span data-stu-id="bd60b-161">Hex</span></span> | <span data-ttu-id="bd60b-162">Flag</span><span class="sxs-lookup"><span data-stu-id="bd60b-162">Flag</span></span>                                    | <span data-ttu-id="bd60b-163">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bd60b-163">Meaning</span></span>                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="bd60b-164">10</span><span class="sxs-lookup"><span data-stu-id="bd60b-164">10</span></span>  | <span data-ttu-id="bd60b-165">Codieren \_ wird \_ verwendet</span><span class="sxs-lookup"><span data-stu-id="bd60b-165">ENCODE\_IS\_USED</span></span>                        | <span data-ttu-id="bd60b-166">Wird nur in Pickeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd60b-166">Used only in pickling.</span></span>                              |
| <span data-ttu-id="bd60b-167">20</span><span class="sxs-lookup"><span data-stu-id="bd60b-167">20</span></span>  | <span data-ttu-id="bd60b-168">Decodieren \_ wird \_ verwendet</span><span class="sxs-lookup"><span data-stu-id="bd60b-168">DECODE\_IS\_USED</span></span>                        | <span data-ttu-id="bd60b-169">Wird nur in Pickeln verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd60b-169">Used only in pickling.</span></span>                              |
| <span data-ttu-id="bd60b-170">10</span><span class="sxs-lookup"><span data-stu-id="bd60b-170">10</span></span>  | <span data-ttu-id="bd60b-171">Oi \_ - \_ \_ Ausnahme \_ Behandlung beim ignorieren von Objekten</span><span class="sxs-lookup"><span data-stu-id="bd60b-171">Oi\_IGNORE\_OBJECT\_EXCEPTION\_HANDLING</span></span> | <span data-ttu-id="bd60b-172">Nicht mehr verwendet (altes OLE).</span><span class="sxs-lookup"><span data-stu-id="bd60b-172">Not used anymore (old OLE).</span></span>                         |
| <span data-ttu-id="bd60b-173">20</span><span class="sxs-lookup"><span data-stu-id="bd60b-173">20</span></span>  | <span data-ttu-id="bd60b-174">Oi hat eine Kommunikations- \_ \_ \_ oder \_ Fehlermeldung</span><span class="sxs-lookup"><span data-stu-id="bd60b-174">Oi\_HAS\_COMM\_OR\_FAULT</span></span>                | <span data-ttu-id="bd60b-175">Nur in unformatierten RPC, \[ comm \_ und Fehler \_ Status \] .</span><span class="sxs-lookup"><span data-stu-id="bd60b-175">In raw RPC only, \[comm \_, fault\_status\].</span></span>        |
| <span data-ttu-id="bd60b-176">20</span><span class="sxs-lookup"><span data-stu-id="bd60b-176">20</span></span>  | <span data-ttu-id="bd60b-177">Oi \_ obj \_ verwendet \_ v2- \_ INTERPRETER</span><span class="sxs-lookup"><span data-stu-id="bd60b-177">Oi\_OBJ\_USE\_V2\_INTERPRETER</span></span>           | <span data-ttu-id="bd60b-178">Verwenden Sie in DCOM nur den [**– OIF**](/windows/desktop/Midl/-oi) -Interpreter.</span><span class="sxs-lookup"><span data-stu-id="bd60b-178">In DCOM only, use [**–Oif**](/windows/desktop/Midl/-oi) interpreter.</span></span> |



 

<span data-ttu-id="bd60b-179">Im Feld RPC- \_ Flags<4> wird beschrieben, wie das **rpcflags** -Feld der [**RPC- \_ Nachrichten**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) Struktur festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd60b-179">The rpc\_flags<4> field describes how to set the **RpcFlags** field of the [**RPC\_MESSAGE**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) structure.</span></span> <span data-ttu-id="bd60b-180">Dieses Feld ist nur vorhanden, wenn für die Oi- \_ Flags<1> Feld Oi \_ \_ rpcflags festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="bd60b-180">This field is only present if the Oi\_flags<1> field has Oi\_HAD\_RPCFLAGS set.</span></span> <span data-ttu-id="bd60b-181">Wenn dieses Feld nicht vorhanden ist, sind die RPC-Flags für die Remote Prozedur 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bd60b-181">If this field is not present, then the RPC flags for the remote procedure are zero.</span></span>

> [!Note]  
> <span data-ttu-id="bd60b-182">Aus Leistungsgründen verfügen die Async-Interpreter immer über die RPC- \_ Flags<4> Feld vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="bd60b-182">For performance, the async interpreters always have the rpc\_flags<4> field present.</span></span>

 

<span data-ttu-id="bd60b-183">Das \_ Feld proc num<2> stellt die Prozedur Nummer der Prozedur bereit.</span><span class="sxs-lookup"><span data-stu-id="bd60b-183">The proc\_num<2> field provides the procedure's procedure number.</span></span>

<span data-ttu-id="bd60b-184">Die Stapel \_ Größe<2> liefert die Gesamtgröße aller Parameter im Stapel, einschließlich dieses Zeigers und/oder Rückgabewerts.</span><span class="sxs-lookup"><span data-stu-id="bd60b-184">The stack\_size<2> provides the total size of all parameters on the stack, including any this pointer and/or return value.</span></span>

<span data-ttu-id="bd60b-185">Die \_ Beschreibung<> Feld für explizites Handle wird weiter unten \_ in diesem Dokument beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd60b-185">The explicit\_handle\_description<> field is described later in this document.</span></span> <span data-ttu-id="bd60b-186">Dieses Feld ist nicht vorhanden, wenn die Prozedur ein implizites Handle verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd60b-186">This field is not present if the procedure uses an implicit handle.</span></span>

 

 