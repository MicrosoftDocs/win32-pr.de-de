---
title: Ziehpunkte
description: So viele wie zwei Teile in der Format Zeichenfolgen-Beschreibung einer Prozedur Adress Handles.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316065"
---
# <a name="handles"></a><span data-ttu-id="687ac-103">Ziehpunkte</span><span class="sxs-lookup"><span data-stu-id="687ac-103">Handles</span></span>

<span data-ttu-id="687ac-104">So viele wie zwei Teile in der Format Zeichenfolgen-Beschreibung einer Prozedur Adress Handles.</span><span class="sxs-lookup"><span data-stu-id="687ac-104">As many as two parts in the format string description of a procedure address handles.</span></span> <span data-ttu-id="687ac-105">Der erste Teil ist der Handle \_ -Typ<1> Feld der Beschreibung einer Prozedur, das verwendet wird, um implizite Handles anzugeben.</span><span class="sxs-lookup"><span data-stu-id="687ac-105">The first part is the handle\_type<1> field of a procedure's description, used to indicate implicit handles.</span></span> <span data-ttu-id="687ac-106">Dieser Teil ist immer vorhanden.</span><span class="sxs-lookup"><span data-stu-id="687ac-106">This part is always present.</span></span> <span data-ttu-id="687ac-107">Der zweite Teil ist eine Parameter Beschreibung eines beliebigen expliziten Handles in der Prozedur.</span><span class="sxs-lookup"><span data-stu-id="687ac-107">The second part is a parameter description of any explicit handle in the procedure.</span></span> <span data-ttu-id="687ac-108">Beide werden in den folgenden Abschnitten erläutert, zusammen mit einer Erörterung der zusätzlichen Unterstützung von Unterstützung der stubdeskriptorstruktur für Bindungs handle-Probleme.</span><span class="sxs-lookup"><span data-stu-id="687ac-108">Both are explained in the following sections, along with a discussion of the additional MIDL compiler support of the Stub Descriptor structure for binding handle issues.</span></span>

## <a name="implicit-handles"></a><span data-ttu-id="687ac-109">Implizite Handles</span><span class="sxs-lookup"><span data-stu-id="687ac-109">Implicit Handles</span></span>

<span data-ttu-id="687ac-110">Wenn eine Prozedur ein implizites Handle für die Bindung verwendet, \_ enthält der Handlertyp<1> Feld der Beschreibung eines der Prozeduren einen von drei gültigen Werten, die nicht NULL sind.</span><span class="sxs-lookup"><span data-stu-id="687ac-110">If a procedure uses an implicit handle for binding, the handle\_type<1> field of the procedure's description contains one of three valid nonzero values.</span></span> <span data-ttu-id="687ac-111">Unterstützung für implizite Handles in der \_ Stub-deskriptorstruktur finden Sie unter Unterstützung für implizites Handle für implizite Handles \_ :</span><span class="sxs-lookup"><span data-stu-id="687ac-111">MIDL compiler support for implicit handles is found in the IMPLICIT\_HANDLE\_INFO field of the Stub Descriptor structure:</span></span>

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

<span data-ttu-id="687ac-112">Wenn die Prozedur ein automatisches Handle verwendet, enthält das " **pautohandle** "-Element die Adresse der definierten Stub-Variablen "– Auto Handle".</span><span class="sxs-lookup"><span data-stu-id="687ac-112">If the procedure uses an auto handle, the **pAutoHandle** member contains the address of the stub defined–auto handle variable.</span></span>

<span data-ttu-id="687ac-113">Wenn die Prozedur ein implizites Primitives Handle verwendet, enthält das **pprimitivehandle** -Element die Adresse der definierten Stub-Variable – primitiver handle.</span><span class="sxs-lookup"><span data-stu-id="687ac-113">If the procedure uses an implicit primitive handle, the **pPrimitiveHandle** member contains the address of the stub defined–primitive handle variable.</span></span>

<span data-ttu-id="687ac-114">Wenn die Prozedur schließlich einen impliziten generischen Handle verwendet, enthält das **pgenericbindinginfo** -Element die Adresse des Zeigers zur entsprechenden **generischen \_ Bindungs \_ Informations** Struktur.</span><span class="sxs-lookup"><span data-stu-id="687ac-114">Finally, if the procedure uses an implicit generic handle, the **pGenericBindingInfo** member holds the address of the pointer to the corresponding **GENERIC\_BINDING\_INFO** structure.</span></span> <span data-ttu-id="687ac-115">Die Datenstruktur " **mittlerer l- \_ Stub- \_ DESC** " enthält einen Zeiger auf eine Auflistung **generischer \_ Bindungs \_ paar** Strukturen.</span><span class="sxs-lookup"><span data-stu-id="687ac-115">The data structure **MIDL\_STUB\_DESC** contains a pointer to a collection of **GENERIC\_BINDING\_PAIR** structures.</span></span> <span data-ttu-id="687ac-116">Der Eintrag in der Null-Position dieser Auflistung ist für die **Bind** -und **Bindung** -Routinen reserviert, die dem generischen Bindungs handle entsprechen, auf das **pgenericbindinginfo** in **impliziten \_ \_ Handlerinformationen** verweist.</span><span class="sxs-lookup"><span data-stu-id="687ac-116">The entry in the zero position of this collection is reserved for the **bind** and **unbind** routines corresponding to the generic binding handle referenced by **pGenericBindingInfo** in **IMPLICIT\_HANDLE\_INFO**.</span></span> <span data-ttu-id="687ac-117">Der Typ des impliziten Bindungs Handles wird in der Format Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="687ac-117">The type of implicit binding handle is indicated in the format string.</span></span>

## <a name="explicit-handles"></a><span data-ttu-id="687ac-118">Explizite Handles</span><span class="sxs-lookup"><span data-stu-id="687ac-118">Explicit Handles</span></span>

<span data-ttu-id="687ac-119">Es gibt drei mögliche explizite Handlertypen: Kontext, generisch und primitiv.</span><span class="sxs-lookup"><span data-stu-id="687ac-119">There are three possible explicit handle types: context, generic, and primitive.</span></span> <span data-ttu-id="687ac-120">Im Fall eines expliziten Handles (oder eines reinen \[  \] Kontext Handles, das auf die gleiche Weise behandelt wird), werden die Bindungs handle-Informationen als einer der Parameter der Prozedur angezeigt.</span><span class="sxs-lookup"><span data-stu-id="687ac-120">In the case of an explicit handle (or an \[**out**\] only context handle, which is handled in the same way), the binding handle information appears as one of the procedure's parameters.</span></span> <span data-ttu-id="687ac-121">Die drei möglichen Beschreibungen lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="687ac-121">The three possible descriptions are as follows.</span></span>

<span data-ttu-id="687ac-122">Primitiv</span><span class="sxs-lookup"><span data-stu-id="687ac-122">Primitive</span></span>

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

<span data-ttu-id="687ac-123">Das Flag<1> gibt an, ob das Handle von einem Zeiger übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="687ac-123">The flag<1> indicates whether the handle is passed by a pointer.</span></span>

<span data-ttu-id="687ac-124">Der Offset<2> stellt den Offset vom Anfang des Stapels zum primitiven Handle bereit.</span><span class="sxs-lookup"><span data-stu-id="687ac-124">The offset<2> provides the offset from the beginning of the stack to the primitive handle.</span></span>

> [!Note]  
> <span data-ttu-id="687ac-125">Eine primitive handle-Beschreibung in der Typformat Zeichenfolge wird auf eine einzelne FC- \_ Ignorierung reduziert.</span><span class="sxs-lookup"><span data-stu-id="687ac-125">A primitive handle description in the type format string is reduced to a single FC\_IGNORE.</span></span>

 

<span data-ttu-id="687ac-126">Allgemein</span><span class="sxs-lookup"><span data-stu-id="687ac-126">Generic</span></span>

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

<span data-ttu-id="687ac-127">Das Flag \_ und die \_ Größe<1> die den oberen Flag-Halbbyte und den unteren Halbbyte-Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="687ac-127">The flag\_and \_size<1> has the upper flag nibble and the lower size nibble.</span></span> <span data-ttu-id="687ac-128">Das Flag gibt an, ob das Handle von einem Zeiger übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="687ac-128">The flag indicates whether the handle is passed by a pointer.</span></span> <span data-ttu-id="687ac-129">Das Größen Feld gibt die Größe des benutzerdefinierten – generischen Handle-Typs an.</span><span class="sxs-lookup"><span data-stu-id="687ac-129">The size field provides the size of the user defined–generic handle type.</span></span> <span data-ttu-id="687ac-130">Diese Größe ist auf 32-Bit-Systemen auf 1, 2 oder 4 Bytes und auf 64-Bit-Systemen auf 1, 2, 4 oder 8 Bytes beschränkt.</span><span class="sxs-lookup"><span data-stu-id="687ac-130">This size is limited to be 1, 2 or 4 bytes on 32-bit systems and 1, 2, 4 or 8 bytes on 64-bit systems.</span></span>

<span data-ttu-id="687ac-131">Das> Feld Offset<2 gibt den Offset vom Anfang des Stapels des Zeigers auf die Daten der angegebenen Größe an.</span><span class="sxs-lookup"><span data-stu-id="687ac-131">The offset<2> field provides the offset from the beginning of the stack of the pointer to the data of the size given.</span></span>

<span data-ttu-id="687ac-132">Der Bindungs \_ Routine- \_ Paar \_ Index<1> Feld gibt den Index im Feld agenericbindingroutinepaars des Stub-Deskriptors an die **Bind** -und **Bindung** -Routine Funktionszeiger für das generische Handle an.</span><span class="sxs-lookup"><span data-stu-id="687ac-132">The binding\_routine\_pair\_index<1> field gives the index into the aGenericBindingRoutinePairs field of the Stub Descriptor to the **bind** and **unbind** routine function pointers for the generic handle.</span></span>

> [!Note]  
> <span data-ttu-id="687ac-133">Eine generische handle-Beschreibung im Typformat ist nur die Beschreibung des zugehörigen Datentyps.</span><span class="sxs-lookup"><span data-stu-id="687ac-133">A generic handle description in the type format is the description of the related data type only.</span></span>

 

<span data-ttu-id="687ac-134">Kontext</span><span class="sxs-lookup"><span data-stu-id="687ac-134">Context</span></span>

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

<span data-ttu-id="687ac-135">Die Flags<1> die Übergabe des Handles und des Typs angeben.</span><span class="sxs-lookup"><span data-stu-id="687ac-135">The flags<1> indicate how the handle is passed and what type it is.</span></span> <span data-ttu-id="687ac-136">Gültige Flags sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="687ac-136">Valid flags are shown in the following table.</span></span>



| <span data-ttu-id="687ac-137">Hex</span><span class="sxs-lookup"><span data-stu-id="687ac-137">Hex</span></span> | <span data-ttu-id="687ac-138">Flag</span><span class="sxs-lookup"><span data-stu-id="687ac-138">Flag</span></span>                                   |
|-----|----------------------------------------|
| <span data-ttu-id="687ac-139">80</span><span class="sxs-lookup"><span data-stu-id="687ac-139">80</span></span>  | <span data-ttu-id="687ac-140">Handle \_ param \_ erfolgt \_ über \_ ptr.</span><span class="sxs-lookup"><span data-stu-id="687ac-140">HANDLE\_PARAM\_IS\_VIA\_PTR</span></span>            |
| <span data-ttu-id="687ac-141">40</span><span class="sxs-lookup"><span data-stu-id="687ac-141">40</span></span>  | <span data-ttu-id="687ac-142">Handle \_ param \_ ist \_ in</span><span class="sxs-lookup"><span data-stu-id="687ac-142">HANDLE\_PARAM\_IS\_IN</span></span>                  |
| <span data-ttu-id="687ac-143">20</span><span class="sxs-lookup"><span data-stu-id="687ac-143">20</span></span>  | <span data-ttu-id="687ac-144">Handle- \_ param \_ ist \_ out</span><span class="sxs-lookup"><span data-stu-id="687ac-144">HANDLE\_PARAM\_IS\_OUT</span></span>                 |
| <span data-ttu-id="687ac-145">21</span><span class="sxs-lookup"><span data-stu-id="687ac-145">21</span></span>  | <span data-ttu-id="687ac-146">Handle \_ param \_ ist \_ Return</span><span class="sxs-lookup"><span data-stu-id="687ac-146">HANDLE\_PARAM\_IS\_RETURN</span></span>              |
| <span data-ttu-id="687ac-147">08</span><span class="sxs-lookup"><span data-stu-id="687ac-147">08</span></span>  | <span data-ttu-id="687ac-148">NDR \_ Strict- \_ Kontext \_ handle</span><span class="sxs-lookup"><span data-stu-id="687ac-148">NDR\_STRICT\_CONTEXT\_HANDLE</span></span>           |
| <span data-ttu-id="687ac-149">04</span><span class="sxs-lookup"><span data-stu-id="687ac-149">04</span></span>  | <span data-ttu-id="687ac-150">der NDR- \_ Kontext \_ handle ist \_ nicht \_ serialisiert.</span><span class="sxs-lookup"><span data-stu-id="687ac-150">NDR\_CONTEXT\_HANDLE\_NO\_SERIALIZE</span></span>    |
| <span data-ttu-id="687ac-151">02</span><span class="sxs-lookup"><span data-stu-id="687ac-151">02</span></span>  | <span data-ttu-id="687ac-152">NDR- \_ Kontext \_ handle \_ serialisieren</span><span class="sxs-lookup"><span data-stu-id="687ac-152">NDR\_CONTEXT\_HANDLE\_SERIALIZE</span></span>        |
| <span data-ttu-id="687ac-153">01</span><span class="sxs-lookup"><span data-stu-id="687ac-153">01</span></span>  | <span data-ttu-id="687ac-154">der NDR- \_ Kontext \_ handle \_ darf nicht \_ \_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="687ac-154">NDR\_CONTEXT\_HANDLE\_CANNOT\_BE\_NULL</span></span> |



 

<span data-ttu-id="687ac-155">Die ersten vier Flags sind immer vorhanden, die letzten vier wurden in Windows 2000 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="687ac-155">The first four flags have always been present, the last four were added in Windows 2000.</span></span>

<span data-ttu-id="687ac-156">Das> Feld Offset<2 gibt den Offset vom Anfang des Stapels bis zum Kontext Handle an.</span><span class="sxs-lookup"><span data-stu-id="687ac-156">The offset<2> field provides the offset from the start of the stack to the context handle.</span></span>

<span data-ttu-id="687ac-157">Der Context- \_ Rundown- \_ Routine \_ Index<1> stellt einen Index im **apfnndrrundownroutinen** -Feld des Stub-Deskriptors für die für dieses Kontext Handle verwendete rundownroutine bereit.</span><span class="sxs-lookup"><span data-stu-id="687ac-157">The context\_rundown\_routine\_index<1> provides an index into the **apfnNdrRundownRoutines** field of the Stub Descriptor to the rundown routine used for this context handle.</span></span> <span data-ttu-id="687ac-158">Der Compiler generiert immer einen Index.</span><span class="sxs-lookup"><span data-stu-id="687ac-158">The compiler always generates an index.</span></span> <span data-ttu-id="687ac-159">Bei Routinen, die keine Rundown-Routine aufweisen, handelt es sich hierbei um einen Index für eine Tabellenposition, die NULL enthält.</span><span class="sxs-lookup"><span data-stu-id="687ac-159">For routines that do not have a rundown routine, this is an index to a table position that holds null.</span></span>

<span data-ttu-id="687ac-160">Für in **– Oi2** integrierte stubwerte gibt die param- \_ Zahl<1> die Ordinalzahl an, beginnend bei Null, um anzugeben, welcher Kontext Handle in der angegebenen Prozedur enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="687ac-160">For stubs built in **–Oi2**, the param\_num<1> provides the ordinal count, starting at zero, specifying which context handle it is in the given procedure.</span></span>

<span data-ttu-id="687ac-161">Bei früheren Versionen des interpreters stellt die param- \_ Zahl<1> die Parameter Nummer des Kontext Handles in der Prozedur bereit, beginnend bei Null.</span><span class="sxs-lookup"><span data-stu-id="687ac-161">For previous versions of the interpreter, the param\_num<1> provides the context handle's parameter number, starting at zero, in its procedure.</span></span>

> [!Note]  
> <span data-ttu-id="687ac-162">Die Beschreibung des Kontext Handles in der typformatzeichenfolge weist nicht den Offset<2> in der Beschreibung auf.</span><span class="sxs-lookup"><span data-stu-id="687ac-162">A context handle description in the type format string will not have the offset<2> in the description.</span></span>

 

## <a name="the-new-oif-header"></a><span data-ttu-id="687ac-163">Der neue – OIF-Header</span><span class="sxs-lookup"><span data-stu-id="687ac-163">The New –Oif Header</span></span>

<span data-ttu-id="687ac-164">Wie bereits erwähnt, wird der [**– OIF**](/windows/desktop/Midl/-oi) -Header auf den **– Oi** -Header erweitert.</span><span class="sxs-lookup"><span data-stu-id="687ac-164">As mentioned previously, the [**–Oif**](/windows/desktop/Midl/-oi) header expands on the **–Oi** header.</span></span> <span data-ttu-id="687ac-165">Aus praktischer Gründen werden alle Felder hier angezeigt:</span><span class="sxs-lookup"><span data-stu-id="687ac-165">For convenience, all fields are shown here:</span></span>

<span data-ttu-id="687ac-166">(Der alte Header)</span><span class="sxs-lookup"><span data-stu-id="687ac-166">(The old header)</span></span>

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

<span data-ttu-id="687ac-167">(Die [**– OIF**](/windows/desktop/Midl/-oi) -Erweiterungen)</span><span class="sxs-lookup"><span data-stu-id="687ac-167">(The [**–Oif**](/windows/desktop/Midl/-oi) extensions)</span></span>

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

<span data-ttu-id="687ac-168">Die Konstante \_ Client \_ Puffer \_ Größe<2> gibt die Größe des marshallingpuffers an, der vom Compiler vorab berechnet werden könnte.</span><span class="sxs-lookup"><span data-stu-id="687ac-168">The constant\_client\_buffer\_size<2> provides the size of the marshaling buffer that could have been pre-computed by the compiler.</span></span> <span data-ttu-id="687ac-169">Dies kann nur eine partielle Größe sein, da das clientmustsize-Flag die Größenänderung auslöst.</span><span class="sxs-lookup"><span data-stu-id="687ac-169">This may be only a partial size, as the ClientMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="687ac-170">Die Konstante \_ Server \_ Puffer \_ Größe<2> gibt die Größe des marshallingpuffers an, der vom Compiler voraus berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="687ac-170">The constant\_server\_buffer\_size<2> provides the size of the marshaling buffer as precomputed by the compiler.</span></span> <span data-ttu-id="687ac-171">Dies kann nur eine partielle Größe sein, da das servermustsize-Flag die Größenänderung auslöst.</span><span class="sxs-lookup"><span data-stu-id="687ac-171">This may be only a partial size, as the ServerMustSize flag triggers the sizing.</span></span>

<span data-ttu-id="687ac-172">Die \_ interpreteropt- \_ Flags sind in ndrtypes. h definiert:</span><span class="sxs-lookup"><span data-stu-id="687ac-172">The INTERPRETER\_OPT\_FLAGS are defined in Ndrtypes.h:</span></span>

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   <span data-ttu-id="687ac-173">Das "servermustsize"-Bit wird festgelegt, wenn der Server einen Puffergrößen Durchlauf ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="687ac-173">The ServerMustSize bit is set if the server needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="687ac-174">Das clientmustsize-Bit wird festgelegt, wenn der Client einen Puffergrößen Durchlauf ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="687ac-174">The ClientMustSize bit is set if the client needs to perform a buffer sizing pass.</span></span>
-   <span data-ttu-id="687ac-175">Das hasreturn-Bit wird festgelegt, wenn die Prozedur über einen Rückgabewert verfügt.</span><span class="sxs-lookup"><span data-stu-id="687ac-175">The HasReturn bit is set if the procedure has a return value.</span></span>
-   <span data-ttu-id="687ac-176">Das haspipes-Bit wird festgelegt, wenn das pipepaket zur Unterstützung eines Pipe-Arguments verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="687ac-176">The HasPipes bit is set if the pipe package needs to be used to support a pipe argument.</span></span>
-   <span data-ttu-id="687ac-177">Das hasasyncuuid-Bit ist festgelegt, wenn es sich bei der Prozedur um eine asynchrone DCOM-Prozedur handelt.</span><span class="sxs-lookup"><span data-stu-id="687ac-177">The HasAsyncUuid bit is set if the procedure is an asynchronous DCOM procedure.</span></span>
-   <span data-ttu-id="687ac-178">Das hasExtensions-Bit gibt an, dass Windows 2000-Erweiterungen und spätere Erweiterungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="687ac-178">The HasExtensions bit indicates that Windows 2000 and later extensions are used.</span></span>
-   <span data-ttu-id="687ac-179">Das hasasynchandle-Bit gibt eine asynchrone RPC-Prozedur an.</span><span class="sxs-lookup"><span data-stu-id="687ac-179">The HasAsyncHandle bit indicates an asynchronous RPC procedure.</span></span>

<span data-ttu-id="687ac-180">Das hasasynchandle-Bit wurde anfänglich für eine andere DCOM-Implementierung der async-Unterstützung verwendet und konnte daher nicht für die asynchrone Unterstützung im aktuellen Stil in DCOM verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="687ac-180">The HasAsyncHandle bit has been initially used for a different DCOM implementation of async support, and hence could not be used for the current style async support in DCOM.</span></span> <span data-ttu-id="687ac-181">Das hasasyncuuid-Bit gibt dies derzeit an.</span><span class="sxs-lookup"><span data-stu-id="687ac-181">The HasAsyncUuid bit currently indicates this.</span></span>

 

 