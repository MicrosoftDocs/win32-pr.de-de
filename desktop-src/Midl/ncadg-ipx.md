---
title: ncadg_ipx-Attribut
description: Das ncadg- \_ IPX-Schlüsselwort identifiziert IPX als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725377"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="68112-105">ncadg- \_ IPX-Attribut</span><span class="sxs-lookup"><span data-stu-id="68112-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="68112-106">Das **ncadg- \_ IPX** -Schlüsselwort identifiziert IPX als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="68112-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="68112-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68112-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="68112-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68112-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68112-109">*Linkadresse*</span><span class="sxs-lookup"><span data-stu-id="68112-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="68112-110">Gibt den Host Server an.</span><span class="sxs-lookup"><span data-stu-id="68112-110">Specifies the host server.</span></span> <span data-ttu-id="68112-111">Dies kann entweder eine Zeichenfolge (der Servername) oder eine 20-stellige hexadezimal Zahl sein, die aus der Netzwerkadresse des Host Servers (8 Ziffern) besteht, die mit der Knotenadresse (12 Ziffern) verkettet ist.</span><span class="sxs-lookup"><span data-stu-id="68112-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="68112-112">Anweisungen zum Abrufen der Netzwerkadresse und der Knotenadresse finden Sie unter "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="68112-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="68112-113">Eine **null** -Zeichenfolge gibt den lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="68112-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="68112-114">*Portname*</span><span class="sxs-lookup"><span data-stu-id="68112-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="68112-115">Gibt eine optionale 16-Bit-Zahl an, die die Socketadresse darstellt.</span><span class="sxs-lookup"><span data-stu-id="68112-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="68112-116">Die Werte können zwischen 1 und 65535 liegen.</span><span class="sxs-lookup"><span data-stu-id="68112-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="68112-117">Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.</span><span class="sxs-lookup"><span data-stu-id="68112-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68112-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68112-118">Remarks</span></span>

<span data-ttu-id="68112-119">Die folgenden Einschränkungen gelten für die Datagramm-Protokolle **ncadg \_ IPX** und [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):</span><span class="sxs-lookup"><span data-stu-id="68112-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="68112-120">Rückrufe werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68112-120">They do not support callbacks.</span></span> <span data-ttu-id="68112-121">Alle Funktionen, die das **\[** [**Rückruf**](callback.md) **\]** Attribut verwenden, schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="68112-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="68112-122">Die [**Verwendung des pipetypkonstruktors**](pipe.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68112-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="68112-123">Wenn Sie den **ncadg- \_ IPX** -Transport verwenden, ist der Servername genau mit dem 32-Bit-Windows-Servernamen identisch.</span><span class="sxs-lookup"><span data-stu-id="68112-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="68112-124">Da die Namen jedoch mithilfe von Novell-Protokollen verteilt werden, müssen Sie den Novell-Benennungs Konventionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="68112-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="68112-125">Wenn ein Servername kein gültiger Novell-Name ist, können Server mit dem **ncadg- \_ IPX** -Transport keine Endpunkte erstellen.</span><span class="sxs-lookup"><span data-stu-id="68112-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="68112-126">Im folgenden finden Sie eine unvollständige Liste von Zeichen, die in Novell-Servernamen nicht zulässig sind:</span><span class="sxs-lookup"><span data-stu-id="68112-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="68112-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="68112-127">" \* + .</span></span> <span data-ttu-id="68112-128">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="68112-128">/ : ; < = > ?</span></span> <span data-ttu-id="68112-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="68112-129">\[ \] \\ \|</span></span>

<span data-ttu-id="68112-130">Der **ncadg \_ IPX** -Transport wird von der Version von NWLink unterstützt, die mit MS Client 3,0 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="68112-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="68112-131">für 16-Bit-Windows-Client Anwendungen, die den **ncadg- \_ IPX** -Transport verwenden, muss die Datei Nwipxspx.dll installiert werden, damit Sie im WOW-Subsystem ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="68112-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="68112-132">Wenden Sie sich an Novell, um diese Datei zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="68112-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="68112-133">Verwenden Sie zum Abrufen der Netzwerk-und Knoten Adressen das **com** -Hilfsprogramm von Novell oder die Novell-definierte API **ipxgetinternetaddress**.</span><span class="sxs-lookup"><span data-stu-id="68112-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="68112-134">Unter Windows können Sie diese Adressen auch mit dem Befehl " **ipxroute config** " abrufen.</span><span class="sxs-lookup"><span data-stu-id="68112-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="68112-135">Die Syntax der TCP/IP-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="68112-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="68112-136">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="68112-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="68112-137">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="68112-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="68112-138">Diese Protokollfamilie wird in Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68112-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="68112-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68112-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="68112-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="68112-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68112-141">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="68112-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="68112-142">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="68112-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="68112-143">**ncacn \_ bei \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="68112-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="68112-144">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="68112-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="68112-145">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="68112-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="68112-146">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="68112-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="68112-147">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="68112-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="68112-148">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="68112-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="68112-149">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="68112-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="68112-150">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="68112-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="68112-151">**ncacn \_ VNS- \_ spp**</span><span class="sxs-lookup"><span data-stu-id="68112-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="68112-152">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="68112-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="68112-153">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="68112-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="68112-154">Zeichen folgen Bindung</span><span class="sxs-lookup"><span data-stu-id="68112-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 