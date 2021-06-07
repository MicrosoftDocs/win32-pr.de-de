---
title: ncalrpc-Attribut
description: Das Schlüsselwort ncalrpc identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt. Dieses Schlüsselwort ist einer der gültigen Protokollfamiliennamen, die mit dem Attribut \endpoint\ verwendet werden müssen.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- ncalrpc-Attribut MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386879"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="8550a-105">ncalrpc-Attribut</span><span class="sxs-lookup"><span data-stu-id="8550a-105">ncalrpc attribute</span></span>

<span data-ttu-id="8550a-106">Das **Schlüsselwort ncalrpc** identifiziert die lokale prozessübergreifende Kommunikation als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="8550a-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="8550a-107">Dieses Schlüsselwort ist einer der gültigen Protokollfamiliennamen, die mit dem **\[** [](endpoint.md) **\]** Endpunktattribut verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8550a-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="8550a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8550a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8550a-109">*Portname*</span><span class="sxs-lookup"><span data-stu-id="8550a-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8550a-110">Eine Zeichenfolge, die den Kommunikationsport (eine Anwendung, einen Dienst oder eine Instanz eines Diensts) angibt, den ein Client verwendet, um prozessübergreifende Aufrufe an einen Server zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="8550a-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="8550a-111">Die Zeichenfolge kann bis zu 53 Zeichen enthalten und darf keinen umgekehrten Schrägstrich \\ () enthalten.</span><span class="sxs-lookup"><span data-stu-id="8550a-111">The string can contain up to 53 characters and should not contain any backslash (\\) characters.</span></span> <span data-ttu-id="8550a-112">Der Computername darf nicht mit dem **Schlüsselwort ncalrpc** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8550a-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8550a-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8550a-113">Remarks</span></span>

<span data-ttu-id="8550a-114">Die Syntax der lokalen Interprocess-Communication-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementation definiert und ist unabhängig von der IDL-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="8550a-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="8550a-115">Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="8550a-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="8550a-116">Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="8550a-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="8550a-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8550a-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="8550a-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8550a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8550a-119">**Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="8550a-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="8550a-120">IDL-Datei (Interface Definition)</span><span class="sxs-lookup"><span data-stu-id="8550a-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8550a-121">**ncacn \_ bei \_ dsp**</span><span class="sxs-lookup"><span data-stu-id="8550a-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="8550a-122">**ncacn \_ dnet \_ nsp**</span><span class="sxs-lookup"><span data-stu-id="8550a-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="8550a-123">**ncacn \_ ip \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="8550a-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="8550a-124">**ncacn \_ nb \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="8550a-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="8550a-125">**ncacn \_ spx**</span><span class="sxs-lookup"><span data-stu-id="8550a-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="8550a-126">**ncacn \_ nb \_ nb**</span><span class="sxs-lookup"><span data-stu-id="8550a-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="8550a-127">**ncacn \_ nb \_ tcp**</span><span class="sxs-lookup"><span data-stu-id="8550a-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="8550a-128">**ncacn \_ np**</span><span class="sxs-lookup"><span data-stu-id="8550a-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="8550a-129">**ncacn \_ vns \_ spp**</span><span class="sxs-lookup"><span data-stu-id="8550a-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="8550a-130">**ncadg \_ ip \_ udp**</span><span class="sxs-lookup"><span data-stu-id="8550a-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="8550a-131">**ncadg \_ ipx**</span><span class="sxs-lookup"><span data-stu-id="8550a-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="8550a-132">Zeichenfolgenbindung</span><span class="sxs-lookup"><span data-stu-id="8550a-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 