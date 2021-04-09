---
title: ncacn_at_dsp-Attribut
description: Das Schlüsselwort ncacn \_ unter \_ DSP identifiziert AppleTalk DSP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9149cd7270c2e82e760c24b4af1fed54c2c08622
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948703"
---
# <a name="ncacn_at_dsp-attribute"></a><span data-ttu-id="e54ba-105">ncacn \_ beim \_ DSP-Attribut</span><span class="sxs-lookup"><span data-stu-id="e54ba-105">ncacn\_at\_dsp attribute</span></span>

<span data-ttu-id="e54ba-106">Das Schlüsselwort **ncacn \_ unter \_ DSP** identifiziert AppleTalk DSP als Protokollfamilie für den Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="e54ba-106">The **ncacn\_at\_dsp** keyword identifies AppleTalk DSP as the protocol family for the endpoint.</span></span> <span data-ttu-id="e54ba-107">Diese Protokollfamilie ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e54ba-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="e54ba-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e54ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54ba-109">*Portname*</span><span class="sxs-lookup"><span data-stu-id="e54ba-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="e54ba-110">Gibt eine Zeichenfolge mit einer Länge von bis zu 22 Bytes an.</span><span class="sxs-lookup"><span data-stu-id="e54ba-110">Specifies a character string up to 22 bytes long.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e54ba-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e54ba-111">Remarks</span></span>

<span data-ttu-id="e54ba-112">Die Syntax der Port Zeichenfolge für den AppleTalk-DSP wird, wie alle Port Zeichenfolgen, von der Transport Implementierung definiert und ist von der IDL-Spezifikation unabhängig.</span><span class="sxs-lookup"><span data-stu-id="e54ba-112">The syntax of the AppleTalk DSP port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="e54ba-113">Der mittlerer l-Compiler führt eine eingeschränkte Syntax Überprüfung durch, gewährleistet jedoch nicht, dass die Endpunkt Spezifikation korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="e54ba-113">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="e54ba-114">Einige Klassen von Fehlern können zur Laufzeit und nicht zur Kompilierzeit gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="e54ba-114">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="e54ba-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e54ba-115">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="e54ba-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e54ba-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54ba-117">**Dreher**</span><span class="sxs-lookup"><span data-stu-id="e54ba-117">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="e54ba-118">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="e54ba-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e54ba-119">**Zeichen folgen Bindung**</span><span class="sxs-lookup"><span data-stu-id="e54ba-119">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 