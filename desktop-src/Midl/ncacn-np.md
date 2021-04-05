---
title: ncacn_np-Attribut
description: Das Schlüsselwort ncacn \_ NP identifiziert Named Pipes als Protokollfamilie für den Endpunkt.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726736"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="70c6d-104">ncacn- \_ NP-Attribut</span><span class="sxs-lookup"><span data-stu-id="70c6d-104">ncacn\_np attribute</span></span>

<span data-ttu-id="70c6d-105">Das Schlüsselwort **ncacn \_ NP** identifiziert Named Pipes als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="70c6d-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="70c6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70c6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c6d-107">*Servername*</span><span class="sxs-lookup"><span data-stu-id="70c6d-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="70c6d-108">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="70c6d-108">Optional.</span></span> <span data-ttu-id="70c6d-109">Gibt den Namen des Servers an.</span><span class="sxs-lookup"><span data-stu-id="70c6d-109">Specifies the name of the server.</span></span> <span data-ttu-id="70c6d-110">Umgekehrte Schrägstriche sind optional.</span><span class="sxs-lookup"><span data-stu-id="70c6d-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="70c6d-111">*Pipename*</span><span class="sxs-lookup"><span data-stu-id="70c6d-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="70c6d-112">Gibt einen gültigen Pipenamen an.</span><span class="sxs-lookup"><span data-stu-id="70c6d-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="70c6d-113">Ein gültiger Pipename ist eine Zeichenfolge, die Bezeichner enthält, die durch umgekehrte Schrägstriche getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="70c6d-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="70c6d-114">Der erste Bezeichner muss eine [**Pipe**](pipe.md)sein.</span><span class="sxs-lookup"><span data-stu-id="70c6d-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="70c6d-115">Jeder Bezeichner muss durch zwei umgekehrte Schrägstriche getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="70c6d-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70c6d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70c6d-116">Remarks</span></span>

<span data-ttu-id="70c6d-117">Ein Server erstellt eine Instanz einer Named Pipe, die dann jedem Client zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="70c6d-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="70c6d-118">Wenn ein Client versucht, eine Verbindung herzustellen, wird die vorhandene Instanz diesem Client zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="70c6d-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="70c6d-119">Bevor ein anderer Client eine Verbindung herstellen kann, muss vom Server eine weitere Instanz des Named Pipe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="70c6d-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="70c6d-120">Wenn ein Client versucht, eine Bindung mit dem Server herzustellen, bevor die neue Instanz erstellt wird, schlägt der Bindungs Aufruf [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)möglicherweise fehl, und die Fehlermeldung RPC \_ S \_ Server ist \_ \_ ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="70c6d-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="70c6d-121">Daher müssen Sie sicherstellen, dass die Client Anwendung den Fall behandelt, in dem der Server zu stark ausgelastet ist, um eine Verbindung zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="70c6d-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="70c6d-122">Der Client sollte automatisch einen Wiederholungsversuch durchführen, den Benutzer zur Eingabe einer Aktion auffordern oder ordnungsgemäß fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="70c6d-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="70c6d-123">Die Syntax der Named Pipe-Port Zeichenfolge, wie alle Port Zeichenfolgen, wird von der Transport Implementierung definiert und ist unabhängig von der IDL-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="70c6d-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="70c6d-124">Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="70c6d-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="70c6d-125">Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="70c6d-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="70c6d-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70c6d-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="70c6d-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="70c6d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c6d-128">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="70c6d-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="70c6d-129">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="70c6d-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="70c6d-130">**ncacn \_ bei \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="70c6d-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-131">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="70c6d-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-132">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="70c6d-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-133">**ncacn \_ NB \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="70c6d-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="70c6d-134">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="70c6d-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="70c6d-135">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="70c6d-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="70c6d-136">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="70c6d-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-137">**ncacn \_ VNS- \_ spp**</span><span class="sxs-lookup"><span data-stu-id="70c6d-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-138">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="70c6d-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="70c6d-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="70c6d-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="70c6d-140">**ncadg \_ -IP- \_ UDP**</span><span class="sxs-lookup"><span data-stu-id="70c6d-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="70c6d-141">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="70c6d-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 