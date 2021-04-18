---
title: ncacn_spx-Attribut
description: Das ncacn- \_ SPX-Schlüsselwort identifiziert SPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339880"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="a9d12-105">ncacn- \_ SPX-Attribut</span><span class="sxs-lookup"><span data-stu-id="a9d12-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="a9d12-106">Das **ncacn- \_ SPX** -Schlüsselwort identifiziert SPX als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="a9d12-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="a9d12-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9d12-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="a9d12-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9d12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d12-109">*Linkadresse*</span><span class="sxs-lookup"><span data-stu-id="a9d12-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d12-110">Gibt den Host Server an.</span><span class="sxs-lookup"><span data-stu-id="a9d12-110">Specifies the host server.</span></span> <span data-ttu-id="a9d12-111">Dies kann entweder eine Zeichenfolge (der Servername) oder eine 20-stellige hexadezimal Zahl sein, die aus der Netzwerkadresse des Host Servers (8 Ziffern) besteht, die mit der Knotenadresse (12 Ziffern) verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="a9d12-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="a9d12-112">Anweisungen zum Abrufen der Netzwerkadresse und der Knotenadresse finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="a9d12-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="a9d12-113">Eine **null** -Zeichenfolge gibt den lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="a9d12-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="a9d12-114">*Portname*</span><span class="sxs-lookup"><span data-stu-id="a9d12-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d12-115">Gibt eine optionale 16-Bit-Zahl an, die die Socketadresse darstellt.</span><span class="sxs-lookup"><span data-stu-id="a9d12-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="a9d12-116">Die Werte können zwischen 1 und 65.535 liegen.</span><span class="sxs-lookup"><span data-stu-id="a9d12-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="a9d12-117">Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.</span><span class="sxs-lookup"><span data-stu-id="a9d12-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9d12-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9d12-118">Remarks</span></span>

<span data-ttu-id="a9d12-119">Wenn Sie den **ncacn- \_ SPX** -Transport verwenden, ist der Servername genau mit dem 32-Bit-Windows-Namen identisch.</span><span class="sxs-lookup"><span data-stu-id="a9d12-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="a9d12-120">Da die Namen jedoch mithilfe von Novell-Protokollen verteilt werden, müssen Sie den Novell-Benennungs Konventionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a9d12-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="a9d12-121">Wenn ein Servername kein gültiger Novell-Name ist, können Server mit dem **ncacn- \_ SPX** -Transport keine Endpunkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9d12-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="a9d12-122">Im folgenden finden Sie eine unvollständige Liste von Zeichen, die in Novell-Servernamen nicht zulässig sind:</span><span class="sxs-lookup"><span data-stu-id="a9d12-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="a9d12-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="a9d12-123">" \* + .</span></span> <span data-ttu-id="a9d12-124">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="a9d12-124">/ : ; < = > ?</span></span> <span data-ttu-id="a9d12-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="a9d12-125">\[ \] \\ \|</span></span>

<span data-ttu-id="a9d12-126">Der **ncacn- \_ SPX** -Transport wird von der mit MS Client 3,0 bereitgestellten NWLink-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a9d12-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="a9d12-127">für 16-Bit-Windows-Client Anwendungen, die den **ncacn- \_ SPX** -Transport verwenden, muss die Datei Nwipxspx.dll installiert werden, um unter dem wow-Subsystem ausgeführt werden zu können.</span><span class="sxs-lookup"><span data-stu-id="a9d12-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="a9d12-128">Wenden Sie sich an Novell, um diese Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9d12-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="a9d12-129">Verwenden Sie zum Abrufen der Netzwerk-und Knoten Adressen das **com** -Hilfsprogramm von Novell oder die Novell-definierte API **ipxgetinternetaddress**.</span><span class="sxs-lookup"><span data-stu-id="a9d12-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="a9d12-130">Unter Windows können Sie diese Adressen auch mit dem Befehl " **ipxroute config** " abrufen.</span><span class="sxs-lookup"><span data-stu-id="a9d12-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="a9d12-131">Die Syntax der SPX-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="a9d12-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="a9d12-132">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="a9d12-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a9d12-133">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="a9d12-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="a9d12-134">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9d12-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="a9d12-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a9d12-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d12-136">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="a9d12-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a9d12-137">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="a9d12-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a9d12-138">**ncacn \_ bei \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-139">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-140">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-141">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a9d12-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="a9d12-142">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="a9d12-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="a9d12-143">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-144">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="a9d12-145">**ncacn \_ VNS- \_ spp**</span><span class="sxs-lookup"><span data-stu-id="a9d12-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-146">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="a9d12-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="a9d12-147">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a9d12-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="a9d12-148">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="a9d12-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="a9d12-149">Zeichen folgen Bindung</span><span class="sxs-lookup"><span data-stu-id="a9d12-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 