---
title: ncacn_vns_spp-Attribut
description: Das Schlüsselwort ncacn \_ VNS \_ spp identifiziert Banyan VINES SPP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726080"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="403b5-105">ncacn \_ VNS- \_ spp-Attribut</span><span class="sxs-lookup"><span data-stu-id="403b5-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="403b5-106">Das Schlüsselwort **ncacn \_ VNS \_ spp** identifiziert Banyan VINES SPP als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="403b5-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="403b5-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="403b5-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="403b5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="403b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403b5-109">*Servername*</span><span class="sxs-lookup"><span data-stu-id="403b5-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="403b5-110">Gibt den StreetTalk-Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="403b5-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="403b5-111">Der Name hat das Format item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="403b5-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="403b5-112">Das Element kann bis zu 31 Zeichen lang sein, und die Gruppe und die Organisation können bis zu 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="403b5-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="403b5-113">*Portname*</span><span class="sxs-lookup"><span data-stu-id="403b5-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="403b5-114">Gibt einen Banyan VINES-SPP-Port an.</span><span class="sxs-lookup"><span data-stu-id="403b5-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="403b5-115">Der gültige Bereich für statische Endpunkte ist 250 – 511.</span><span class="sxs-lookup"><span data-stu-id="403b5-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="403b5-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="403b5-116">Remarks</span></span>

<span data-ttu-id="403b5-117">Die entsprechende Banyan Enterprise-Client Software muss installiert sein, damit das **ncacn \_ VNS- \_ spp** -Transportprotokoll in verteilten Anwendungen unter Windows 2000 verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="403b5-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="403b5-118">Öffnen Sie nach der Installation die **Systemsteuerung**, wählen Sie **Konfiguration und hinzufügen** aus, und wählen Sie dann **Dienst \| Banyan \| RPC-Dienste für Banyan aus**.</span><span class="sxs-lookup"><span data-stu-id="403b5-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="403b5-119">Die Unterstützung für 16-Bit-Clients erfordert die geeignete rebsoftware.</span><span class="sxs-lookup"><span data-stu-id="403b5-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="403b5-120">Weitere Informationen über das Enterprise Client-Produkt und die 16-Bit-Reben Software finden Sie in der Banyan-Version.</span><span class="sxs-lookup"><span data-stu-id="403b5-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="403b5-121">Die Syntax der spp-Transport Port Zeichenfolge von Banyan Vines, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="403b5-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="403b5-122">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="403b5-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="403b5-123">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="403b5-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="403b5-124">Diese Protokollfamilie wird in Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="403b5-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="403b5-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="403b5-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="403b5-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="403b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="403b5-127">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="403b5-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="403b5-128">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="403b5-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="403b5-129">**ncacn \_ bei \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="403b5-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="403b5-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="403b5-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="403b5-131">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="403b5-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="403b5-132">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="403b5-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="403b5-133">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="403b5-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="403b5-134">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="403b5-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="403b5-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="403b5-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="403b5-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="403b5-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="403b5-137">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="403b5-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="403b5-138">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="403b5-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="403b5-139">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="403b5-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="403b5-140">Zeichen folgen Bindung</span><span class="sxs-lookup"><span data-stu-id="403b5-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 