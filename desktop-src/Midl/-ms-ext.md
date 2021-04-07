---
title: /ms_ext Schalter
description: Ab der mittleren l-Version 3,0 sind die vom MS ext-Schalter aktivierten Funktionen \_ nun der Standardmodus für den Mittelwert Compiler.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038846"
---
# <a name="ms_ext-switch"></a><span data-ttu-id="1e5ca-104">/MS \_ ext-Schalter</span><span class="sxs-lookup"><span data-stu-id="1e5ca-104">/ms\_ext switch</span></span>

<span data-ttu-id="1e5ca-105">Ab der mittleren l-Version 3,0 sind die vom **MS \_ ext** -Schalter aktivierten Funktionen nun der Standardmodus für den Mittelwert Compiler.</span><span class="sxs-lookup"><span data-stu-id="1e5ca-105">Effective with MIDL version 3.0, the features enabled by the **ms\_ext** switch are now the default mode for the MIDL compiler.</span></span>

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a><span data-ttu-id="1e5ca-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="1e5ca-106">Switch Options</span></span>

<span data-ttu-id="1e5ca-107">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e5ca-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e5ca-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-108">Remarks</span></span>

<span data-ttu-id="1e5ca-109">Wenn Sie den Schalter verwenden, wird kein Compilerfehler generiert, sodass Sie keine Verweise auf **/MS \_ ext** oder [**/c \_ ext**](-c-ext.md) aus einem vorhandenen Makefile entfernen müssen.</span><span class="sxs-lookup"><span data-stu-id="1e5ca-109">Using the switch will not generate a compiler error, so you do not have to remove references to **/ms\_ext** or [**/c\_ext**](-c-ext.md) from an existing makefile.</span></span>

<span data-ttu-id="1e5ca-110">Die folgenden Microsoft-Erweiterungen für OSF-DCE sind nun standardmäßig verfügbar:</span><span class="sxs-lookup"><span data-stu-id="1e5ca-110">The following Microsoft extensions to OSF DCE are now available by default:</span></span>

-   <span data-ttu-id="1e5ca-111">Schnittstellendefinitionen für OLE-Objekte.</span><span class="sxs-lookup"><span data-stu-id="1e5ca-111">Interface definitions for OLE objects.</span></span> <span data-ttu-id="1e5ca-112">Weitere Informationen zu den für OLE-Schnittstellen generierten Dateien finden Sie unter für [eine COM-Schnittstelle generierte Dateien](files-generated-for-a-com-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="1e5ca-112">For more information on the files generated for OLE interfaces, see [Files Generated for a COM Interface](files-generated-for-a-com-interface.md)</span></span>
-   <span data-ttu-id="1e5ca-113">Ein [**\[ Rückruf \]**](callback.md) Attribut, das eine statische Rückruffunktion auf dem Client angibt.</span><span class="sxs-lookup"><span data-stu-id="1e5ca-113">A [**\[callback\]**](callback.md) attribute specifying a static callback function on the client</span></span>
-   <span data-ttu-id="1e5ca-114">[**cpp- \_ Zitat**](cpp-quote.md)(*\_ Zeichenfolge* in Anführungszeichen) und [**\# pragma-Mittell- \_ Echo**](pragma.md)</span><span class="sxs-lookup"><span data-stu-id="1e5ca-114">[**cpp\_quote**](cpp-quote.md)(*quoted\_string*) and [**\#pragma midl\_echo**](pragma.md)</span></span>
-   <span data-ttu-id="1e5ca-115">[**WCHAR \_ t**](wchar-t.md) -breit Zeichen Typen,-Konstanten und-Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-115">[**wchar\_t**](wchar-t.md) wide-character types, constants, and strings</span></span>
-   <span data-ttu-id="1e5ca-116">[**enumerationsinitialisierung**](enum.md) (Sparse-Enumeratoren)</span><span class="sxs-lookup"><span data-stu-id="1e5ca-116">[**enum initialization**](enum.md) (sparse enumerators)</span></span>
-   <span data-ttu-id="1e5ca-117">Ausdrücke als Größen-und diskriminatorspezifiker</span><span class="sxs-lookup"><span data-stu-id="1e5ca-117">Expressions as size and discriminator specifiers</span></span>
-   [<span data-ttu-id="1e5ca-118">Behandeln von Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-118">Handle extensions</span></span>](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [<span data-ttu-id="1e5ca-119">Vererbung von Attributtypen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-119">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [<span data-ttu-id="1e5ca-120">Mehrere Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-120">Multiple interfaces</span></span>](/windows/desktop/Rpc/registering-interfaces)
-   <span data-ttu-id="1e5ca-121">Definitionen außerhalb des Schnittstellen Blocks</span><span class="sxs-lookup"><span data-stu-id="1e5ca-121">Definitions outside of the interface block</span></span>
-   <span data-ttu-id="1e5ca-122">Sie können [direktionale Attribute](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**in**](in.md), [**out**](out-idl.md) weglassen.\]</span><span class="sxs-lookup"><span data-stu-id="1e5ca-122">You can omit [directional attributes](/windows/desktop/Rpc/directional-parameter-attributes) \[[**in**](in.md), [**out**](out-idl.md)\]</span></span>

## <a name="see-also"></a><span data-ttu-id="1e5ca-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e5ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5ca-124">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1e5ca-124">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="1e5ca-125">Vererbung von Attributtypen</span><span class="sxs-lookup"><span data-stu-id="1e5ca-125">Pointer-attribute type inheritance</span></span>](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[<span data-ttu-id="1e5ca-126">**/APP- \_ Konfiguration**</span><span class="sxs-lookup"><span data-stu-id="1e5ca-126">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="1e5ca-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="1e5ca-127">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 