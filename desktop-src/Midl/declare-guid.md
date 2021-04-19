---
title: declare_guid-Schlüsselwort
description: Das DECLARE \_ GUID-Schlüsselwort weist die Mitte an, eine GUID-Variable in der generierten Header Datei auszugeben.
keywords:
- declare_guid-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- declare_guid
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 495acd64e79544d067ff124a88289219919a7fb6
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "106355096"
---
# <a name="declare_guid-keyword"></a><span data-ttu-id="97bce-104">DECLARE \_ GUID-Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="97bce-104">declare\_guid keyword</span></span>

<span data-ttu-id="97bce-105">Das **Declare \_ GUID** -Schlüsselwort weist die Mitte an, eine GUID-Variable in der generierten Header Datei auszugeben.</span><span class="sxs-lookup"><span data-stu-id="97bce-105">The **declare\_guid** keyword instructs MIDL to emit a GUID variable into the generated header file.</span></span>

``` syntax
declare_guid(variable-name, guid)
```

## <a name="parameters"></a><span data-ttu-id="97bce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="97bce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97bce-107">*Variablenname*</span><span class="sxs-lookup"><span data-stu-id="97bce-107">*variable-name*</span></span> 
</dt> <dd>

<span data-ttu-id="97bce-108">Gibt einen Variablennamen für den Bezeichner in der generierten Header Datei an.</span><span class="sxs-lookup"><span data-stu-id="97bce-108">Specifies a variable name for the identifier in the generated header file.</span></span>

</dd> <dt>

<span data-ttu-id="97bce-109">*guid*</span><span class="sxs-lookup"><span data-stu-id="97bce-109">*guid*</span></span>
</dt> <dd>

<span data-ttu-id="97bce-110">Gibt die [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) an, die auf den Variablennamen in der generierten Header Datei angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="97bce-110">Specifies the [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) that will apply to the variable name in the generated header file.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="97bce-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97bce-111">Examples</span></span>

``` syntax
declare_guid(SID_Widget, 5144C348-169E-4359-A79D-5482461D9929)  
```

## <a name="remarks"></a><span data-ttu-id="97bce-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97bce-112">Remarks</span></span>

<span data-ttu-id="97bce-113">`declare_guid` `cpp_quote` Die Verwendung von entspricht der Verwendung von, um einen Aufruf des `EXTERN_GUID` Makros zu generieren.</span><span class="sxs-lookup"><span data-stu-id="97bce-113">Using `declare_guid` is equivalent to using `cpp_quote` to generate an invocation of the `EXTERN_GUID` macro.</span></span>

<span data-ttu-id="97bce-114">Im obigen Beispiel wird die folgende Ausgabe angezeigt:</span><span class="sxs-lookup"><span data-stu-id="97bce-114">The above example results in the following output:</span></span>

```C
cpp_quote("EXTERN_GUID(SID_Widget, 0x5144c348, 0x169e, 0x4359, 0xa7, 0x9d, 0x54, 0x82, 0x46, 0x1d, 0x99, 0x29);")
```

<span data-ttu-id="97bce-115">Die- `declare_guid` Anweisung wird als praktische Hilfe bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="97bce-115">The `declare_guid` statement is provided as a convenience.</span></span> <span data-ttu-id="97bce-116">Es hat den Vorteil, dass die gleiche GUID-Syntax wie das- [ `uuid` Attribut](uuid.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97bce-116">It has the advantage of using the same GUID syntax as the [`uuid` attribute](uuid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="97bce-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97bce-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bce-118">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="97bce-118">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="97bce-119">**cpp_quote**</span><span class="sxs-lookup"><span data-stu-id="97bce-119">**cpp_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="97bce-120">**uuid-Attribut**</span><span class="sxs-lookup"><span data-stu-id="97bce-120">**uuid attribute**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="97bce-121">**GUID-Struktur**</span><span class="sxs-lookup"><span data-stu-id="97bce-121">**GUID structure**</span></span>](/windows/win32/api/guiddef/ns-guiddef-guid)
</dt> </dl>
