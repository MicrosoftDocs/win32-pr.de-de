---
title: ncadg_ip_udp-Attribut
description: Das Schlüsselwort ncadg \_ IP \_ UDP identifiziert die Datagramm-Version von TCP/IP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101530"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="3df9a-105">ncadg \_ -IP- \_ UDP-Attribut</span><span class="sxs-lookup"><span data-stu-id="3df9a-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="3df9a-106">Das Schlüsselwort **ncadg \_ IP \_ UDP** identifiziert die Datagramm-Version von TCP/IP als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="3df9a-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="3df9a-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3df9a-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="3df9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3df9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3df9a-109">*Servername*</span><span class="sxs-lookup"><span data-stu-id="3df9a-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3df9a-110">Gibt den Namen oder die Internetadresse für den Server oder Host Computer an.</span><span class="sxs-lookup"><span data-stu-id="3df9a-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="3df9a-111">Der Name ist eine Zeichenfolge und kann ein voll qualifizierter Domänen Name sein.</span><span class="sxs-lookup"><span data-stu-id="3df9a-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="3df9a-112">Die Internetadresse ist eine gängige Internet Adress Notation.</span><span class="sxs-lookup"><span data-stu-id="3df9a-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="3df9a-113">*Portname*</span><span class="sxs-lookup"><span data-stu-id="3df9a-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="3df9a-114">Gibt eine optionale 16-Bit-Zahl an.</span><span class="sxs-lookup"><span data-stu-id="3df9a-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="3df9a-115">Werte, die kleiner als 1024 sind, sind normalerweise reserviert.</span><span class="sxs-lookup"><span data-stu-id="3df9a-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="3df9a-116">Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.</span><span class="sxs-lookup"><span data-stu-id="3df9a-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3df9a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3df9a-117">Remarks</span></span>

<span data-ttu-id="3df9a-118">Die folgenden Einschränkungen gelten für die Datagramm-Protokolle [**ncadg \_ IPX**](ncadg-ipx.md) und **ncadg \_ IP \_ UDP**:</span><span class="sxs-lookup"><span data-stu-id="3df9a-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="3df9a-119">Rückrufe werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3df9a-119">They do not support callbacks.</span></span> <span data-ttu-id="3df9a-120">Alle Funktionen, die das **\[** [**Rückruf**](callback.md) **\]** Attribut verwenden, schlagen fehl.</span><span class="sxs-lookup"><span data-stu-id="3df9a-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="3df9a-121">Die [**Verwendung des pipetypkonstruktors**](pipe.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3df9a-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="3df9a-122">Die Syntax der TCP/IP-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="3df9a-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="3df9a-123">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="3df9a-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="3df9a-124">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="3df9a-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="3df9a-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3df9a-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="3df9a-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3df9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df9a-127">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="3df9a-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="3df9a-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="3df9a-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3df9a-129">**ncacn \_ bei \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="3df9a-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="3df9a-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="3df9a-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="3df9a-131">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3df9a-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="3df9a-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3df9a-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="3df9a-133">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="3df9a-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="3df9a-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="3df9a-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="3df9a-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="3df9a-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="3df9a-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="3df9a-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="3df9a-137">**ncacn \_ VNS- \_ spp**</span><span class="sxs-lookup"><span data-stu-id="3df9a-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="3df9a-138">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="3df9a-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="3df9a-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="3df9a-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="3df9a-140">Zeichen folgen Bindung</span><span class="sxs-lookup"><span data-stu-id="3df9a-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 