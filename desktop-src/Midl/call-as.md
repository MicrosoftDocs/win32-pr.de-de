---
title: Aufruf als Attribut
description: Mit dem \-Aufruf \_ als \-Attribut können Sie eine Funktion zuordnen, die nicht remote zu einer Remote Funktion aufgerufen werden kann.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- Call_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106337629"
---
# <a name="call_as-attribute"></a><span data-ttu-id="fafe4-104">\_als Attribut aufzurufen</span><span class="sxs-lookup"><span data-stu-id="fafe4-104">call\_as attribute</span></span>

<span data-ttu-id="fafe4-105">Der **\[ Aufruf \_ als \]** -Attribut ermöglicht es Ihnen, eine Funktion zuzuordnen, die nicht remote zu einer Remote Funktion aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="fafe4-105">The **\[call\_as\]** attribute enables you to map a function that cannot be called remotely to a remote function.</span></span>

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a><span data-ttu-id="fafe4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fafe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafe4-107">*local-proc*</span><span class="sxs-lookup"><span data-stu-id="fafe4-107">*local-proc*</span></span> 
</dt> <dd>

<span data-ttu-id="fafe4-108">Gibt eine Vorgangs definierte Routine an.</span><span class="sxs-lookup"><span data-stu-id="fafe4-108">Specifies an operation-defined routine.</span></span>

</dd> <dt>

<span data-ttu-id="fafe4-109">*Operation-Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="fafe4-109">*operation-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="fafe4-110">Gibt ein oder mehrere Attribute an, die für den Vorgang gelten.</span><span class="sxs-lookup"><span data-stu-id="fafe4-110">Specifies one or more attributes that apply to the operation.</span></span> <span data-ttu-id="fafe4-111">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="fafe4-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="fafe4-112">*Vorgangs Name*</span><span class="sxs-lookup"><span data-stu-id="fafe4-112">*operation-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fafe4-113">Gibt den benannten Vorgang an, der der Anwendung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fafe4-113">Specifies the named operation presented to the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fafe4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fafe4-114">Remarks</span></span>

<span data-ttu-id="fafe4-115">Die Möglichkeit, eine Funktion zuzuordnen, die nicht Remote an eine Remote Funktion aufgerufen werden kann, ist besonders hilfreich bei Schnittstellen, die über zahlreiche Parametertypen verfügen, die nicht über das Netzwerk übertragen werden können.</span><span class="sxs-lookup"><span data-stu-id="fafe4-115">The ability to map a function that cannot be called remotely to a remote function is particularly helpful in interfaces that have numerous parameter types that cannot be transmitted across the network.</span></span> <span data-ttu-id="fafe4-116">Anstatt viele **\[** [**\_**](represent-as.md) **\]** Darstellungs-und-über **\[** [**Tragung \_ als**](transmit-as.md) -Typen zu verwenden **\]** , können Sie alle Konvertierungen mithilfe von **\[ \_ Callas \]** -Routinen kombinieren.</span><span class="sxs-lookup"><span data-stu-id="fafe4-116">Rather than using many **\[**[**represent\_as**](represent-as.md)**\]** and **\[**[**transmit\_as**](transmit-as.md)**\]** types, you can combine all the conversions using **\[call\_as\]** routines.</span></span> <span data-ttu-id="fafe4-117">Sie geben die beiden **\[ Aufrufe \_ als \]** Routinen (Client seitig und serverseitig) an, um die Routine zwischen den Anwendungs aufrufen und den Remote aufrufen zu binden.</span><span class="sxs-lookup"><span data-stu-id="fafe4-117">You supply the two **\[call\_as\]** routines (client side and server side) to bind the routine between the application calls and the remote calls.</span></span>

<span data-ttu-id="fafe4-118">Der " **\[ \_ Callas \]** "-Attribut kann für Objekt Schnittstellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fafe4-118">The **\[call\_as\]** attribute can be used for object interfaces.</span></span> <span data-ttu-id="fafe4-119">In diesem Fall kann die Schnittstellen Definition sowohl für lokale Aufrufe als auch für Remote Aufrufe verwendet werden, da **\[ Aufruf \_ als \]** eine Schnittstelle zulässt, auf die nicht remote zugegriffen werden kann, um einer Remote Schnittstelle transparent zugeordnet zu werden.</span><span class="sxs-lookup"><span data-stu-id="fafe4-119">In this case, the interface definition can be used for local calls as well as remote calls because **\[call\_as\]** allows an interface that can't be accessed remotely to be transparently mapped to a remote interface.</span></span> <span data-ttu-id="fafe4-120">Der " **\[ \_ Callas \]** "-Attribut kann nicht im [**/OSF**](-osf.md) -Modus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fafe4-120">The **\[call\_as\]** attribute cannot be used with [**/osf**](-osf.md) mode.</span></span>

<span data-ttu-id="fafe4-121">Nehmen wir beispielsweise an, dass für die Routine **F1** in Object Interface **iface** zahlreiche Konvertierungen zwischen den Benutzer aufrufen und den tatsächlich übertragenen Inhalt erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fafe4-121">For example, assume that the routine **f1** in object interface **IFace** requires numerous conversions between the user calls and what is actually transmitted.</span></span> <span data-ttu-id="fafe4-122">In den folgenden Beispielen werden die IDL-und ACF-Dateien für die Schnittstelle **iface** beschrieben:</span><span class="sxs-lookup"><span data-stu-id="fafe4-122">The following examples describe the IDL and ACF files for interface **IFace**:</span></span>

<span data-ttu-id="fafe4-123">In der IDL-Datei für Interface **iface**:</span><span class="sxs-lookup"><span data-stu-id="fafe4-123">In the IDL file for interface **IFace**:</span></span>

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

<span data-ttu-id="fafe4-124">In der ACF für Schnittstelle **iface**:</span><span class="sxs-lookup"><span data-stu-id="fafe4-124">In the ACF for interface **IFace**:</span></span>

``` syntax
[call_as( f1 )] Remf1();
```

<span data-ttu-id="fafe4-125">Dies bewirkt, dass die generierte Header Datei die-Schnittstelle mithilfe der Definition von **F1** definiert, aber auch stusb für **Remf1** bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fafe4-125">This causes the generated header file to define the interface using the definition of **f1**, yet it also provides stubs for **Remf1**.</span></span>

<span data-ttu-id="fafe4-126">Der mittlerer l-Compiler generiert die folgende Vtable in der Header Datei für die Schnittstelle **iface**:</span><span class="sxs-lookup"><span data-stu-id="fafe4-126">The MIDL compiler will generate the following Vtable in the header file for interface **IFace**:</span></span>

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

<span data-ttu-id="fafe4-127">Der Client seitige Proxy verfügt dann über einen typischen, von der Mitte generierten Proxy für **Remf1**, während der serverseitige Stub für **Remf1** mit dem typischen, von der Mittel l generierten Stub identisch ist:</span><span class="sxs-lookup"><span data-stu-id="fafe4-127">The client-side proxy would then have a typical MIDL-generated proxy for **Remf1**, while the server side stub for **Remf1** would be the same as the typical MIDL-generated stub:</span></span>

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

<span data-ttu-id="fafe4-128">Anschließend müssen die beiden **\[ Aufrufe \_ als \]** Bindungs Routinen (Clientseite und serverseitig) manuell codiert werden:</span><span class="sxs-lookup"><span data-stu-id="fafe4-128">Then, the two **\[call\_as\]** bond routines (client side and server side) must be manually coded:</span></span>

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

<span data-ttu-id="fafe4-129">Bei Objekt Schnittstellen sind dies die Prototypen für die Bindungs Routinen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-129">For object interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="fafe4-130">Client seitig:</span><span class="sxs-lookup"><span data-stu-id="fafe4-130">For client side:</span></span>

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

<span data-ttu-id="fafe4-131">Für serverseitig:</span><span class="sxs-lookup"><span data-stu-id="fafe4-131">For server side:</span></span>

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

<span data-ttu-id="fafe4-132">Bei nicht-Objekt Schnittstellen sind dies die Prototypen für die Bindungs Routinen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-132">For nonobject interfaces, these are the prototypes for the bond routines.</span></span>

<span data-ttu-id="fafe4-133">Client seitig:</span><span class="sxs-lookup"><span data-stu-id="fafe4-133">For client side:</span></span>

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

<span data-ttu-id="fafe4-134">Für serverseitig:</span><span class="sxs-lookup"><span data-stu-id="fafe4-134">For server side:</span></span>

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a><span data-ttu-id="fafe4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fafe4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafe4-136">**/osf**</span><span class="sxs-lookup"><span data-stu-id="fafe4-136">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="fafe4-137">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="fafe4-137">**represent\_as**</span></span>](represent-as.md)
</dt> <dt>

[<span data-ttu-id="fafe4-138">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="fafe4-138">**transmit\_as**</span></span>](transmit-as.md)
</dt> </dl>

 

 




