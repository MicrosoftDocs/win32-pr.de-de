---
title: ncacn_nb_tcp-Attribut
description: Das Schlüsselwort ncacn \_ NB \_ TCP wird zum Identifizieren von TCP über NetBIOS als Protokollfamilie für den Endpunkt verwendet. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314997"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="59036-105">ncacn \_ NB \_ TCP-Attribut</span><span class="sxs-lookup"><span data-stu-id="59036-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="59036-106">Das Schlüsselwort **ncacn \_ NB \_ TCP** wird zum Identifizieren von TCP über NetBIOS als Protokollfamilie für den Endpunkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="59036-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="59036-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="59036-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="59036-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59036-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59036-109">*Portname*</span><span class="sxs-lookup"><span data-stu-id="59036-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="59036-110">Gibt einen optionalen 8-Bit-Wert zwischen 1 und 254 an.</span><span class="sxs-lookup"><span data-stu-id="59036-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="59036-111">Werte von weniger als 0x20 sind reserviert.</span><span class="sxs-lookup"><span data-stu-id="59036-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="59036-112">Wenn der *Port-Name-* Wert nicht angegeben wird, wählt der Endpunkt Zuordnung den Portwert aus.</span><span class="sxs-lookup"><span data-stu-id="59036-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59036-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59036-113">Remarks</span></span>

<span data-ttu-id="59036-114">Die Syntax der NetBIOS-Port Zeichenfolge wird wie alle Port Zeichenfolgen durch die Transport Implementierung definiert und ist unabhängig von der IDL-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="59036-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="59036-115">Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="59036-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="59036-116">Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="59036-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="59036-117">Diese Protokollfamilie wird in Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="59036-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="59036-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59036-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="59036-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="59036-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59036-120">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="59036-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="59036-121">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="59036-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="59036-122">**ncacn \_ IP \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="59036-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="59036-123">**ncacn \_ NB \_ NB**</span><span class="sxs-lookup"><span data-stu-id="59036-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="59036-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="59036-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="59036-125">**ncacn- \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="59036-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="59036-126">**Ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="59036-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="59036-127">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="59036-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 