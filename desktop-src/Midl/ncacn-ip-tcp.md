---
title: ncacn_ip_tcp-Attribut
description: Das ncacn \_ IP- \_ TCP-Schlüsselwort identifiziert TCP/IP als Protokollfamilie für den Endpunkt.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340706"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="c7a11-104">ncacn \_ -IP- \_ TCP-Attribut</span><span class="sxs-lookup"><span data-stu-id="c7a11-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="c7a11-105">Das **ncacn \_ IP- \_ TCP** -Schlüsselwort identifiziert TCP/IP als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="c7a11-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="c7a11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7a11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7a11-107">*Servername*</span><span class="sxs-lookup"><span data-stu-id="c7a11-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c7a11-108">Gibt den Namen oder die Internet Adresse für den Server oder Host Computer an.</span><span class="sxs-lookup"><span data-stu-id="c7a11-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="c7a11-109">Der Name ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c7a11-109">The name is a character string.</span></span> <span data-ttu-id="c7a11-110">Die Internetadresse ist eine gängige Internet Adress Notation.</span><span class="sxs-lookup"><span data-stu-id="c7a11-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="c7a11-111">*Portname*</span><span class="sxs-lookup"><span data-stu-id="c7a11-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c7a11-112">Gibt eine optionale 16-Bit-Zahl an.</span><span class="sxs-lookup"><span data-stu-id="c7a11-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="c7a11-113">Werte, die kleiner als 1024 sind, sind normalerweise reserviert.</span><span class="sxs-lookup"><span data-stu-id="c7a11-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="c7a11-114">Wenn kein Wert angegeben wird, wählt der Endpunkt Zuordnung einen gültigen *Portnamen* Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c7a11-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7a11-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7a11-115">Remarks</span></span>

<span data-ttu-id="c7a11-116">Die Syntax der TCP/IP-Transport Port Zeichenfolge, wie alle Port Zeichenfolgen, wird unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="c7a11-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="c7a11-117">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="c7a11-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c7a11-118">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="c7a11-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="c7a11-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7a11-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="c7a11-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7a11-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a11-121">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="c7a11-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c7a11-122">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="c7a11-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c7a11-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="c7a11-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="c7a11-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="c7a11-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="c7a11-125">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="c7a11-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="c7a11-126">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="c7a11-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="c7a11-127">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="c7a11-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 