---
title: ncacn_dnet_nsp-Attribut
description: Das Schlüsselwort ncacn \_ dnet \_ NSP identifiziert DECnet als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101603"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="f1a6b-105">ncacn \_ dnet \_ NSP-Attribut</span><span class="sxs-lookup"><span data-stu-id="f1a6b-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="f1a6b-106">Das Schlüsselwort **ncacn \_ dnet \_ NSP** identifiziert DECnet als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="f1a6b-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="f1a6b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1a6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a6b-109">*Servername*</span><span class="sxs-lookup"><span data-stu-id="f1a6b-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1a6b-110">Gibt den Namen oder die Internetadresse für den Server oder Host Computer an.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="f1a6b-111">Der Name ist eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="f1a6b-112">*Portname*</span><span class="sxs-lookup"><span data-stu-id="f1a6b-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="f1a6b-113">Gibt den Namen oder die Objekt Nummer eines DECnet-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="f1a6b-114">Der Objektname kann aus bis zu 16 Zeichen bestehen.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="f1a6b-115">Objektnummern kann das Nummern Zeichen () als Präfix vorangestellt werden \# .</span><span class="sxs-lookup"><span data-stu-id="f1a6b-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1a6b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1a6b-116">Remarks</span></span>

<span data-ttu-id="f1a6b-117">Die Syntax der Port Zeichenfolge für den DECnet-Transport wird, wie alle Port Zeichenfolgen, unabhängig von der IDL-Spezifikation definiert.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="f1a6b-118">Der Compiler führt einige Syntax Überprüfungen durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="f1a6b-119">Einige Fehler werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="f1a6b-120">Diese Protokollfamilie wird in Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f1a6b-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f1a6b-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1a6b-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="f1a6b-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f1a6b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a6b-123">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="f1a6b-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="f1a6b-124">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="f1a6b-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 