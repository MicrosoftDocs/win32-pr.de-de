---
title: hyperattribute
description: Das Schlüsselwort hypergibt eine 64-Bit-Ganzzahl an, die als "signiert" oder "nicht signiert" deklariert werden kann.
ms.assetid: cadcacc7-8eea-4ce2-b69f-98a1d8bafeaa
keywords:
- hyperattributmittell
topic_type:
- apiref
api_name:
- hyper
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57da7c0d54e5b9ffcd47f76b22825d13b0a8cff9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718071"
---
# <a name="hyper-attribute"></a><span data-ttu-id="bf851-104">hyperattribute</span><span class="sxs-lookup"><span data-stu-id="bf851-104">hyper attribute</span></span>

<span data-ttu-id="bf851-105">Das Schlüsselwort **hypergibt** eine 64-Bit-Ganzzahl an, die als "signiert" oder "nicht signiert" deklariert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bf851-105">The keyword **hyper** indicates a 64-bit integer that can be declared as either signed or unsigned.</span></span>

``` syntax
[ signed | unsigned ] hyper [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="bf851-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf851-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf851-107">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="bf851-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bf851-108">Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="bf851-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="bf851-109">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="bf851-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="bf851-110">Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="bf851-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf851-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf851-111">Remarks</span></span>

<span data-ttu-id="bf851-112">Der **hypertyp** ist einer der Basis Typen der IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="bf851-112">The **hyper** type is one of the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="bf851-113">Der **hypertyp** kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bf851-113">The **hyper** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="bf851-114">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="bf851-114">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="bf851-115">Für 16-Bit-Plattformen ersetzt der mittlerer l-Compiler nicht signierte hyperintegerwerte durch die **mittlere \_** benutzerdefinierte Funktion.</span><span class="sxs-lookup"><span data-stu-id="bf851-115">For 16-bit platforms, the MIDL compiler replaces unsigned hyper integers with **MIDL\_uhyper**.</span></span> <span data-ttu-id="bf851-116">Dadurch können Schnittstellen mit nicht signierten hyperintegern auf Plattformen definiert werden, die keine direkte Unterstützung von 64-Bit-Ganzzahlen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bf851-116">This allows interfaces with unsigned hyper integers to be defined on platforms that do not directly support 64-bit integers.</span></span> <span data-ttu-id="bf851-117">Die **mittlere \_** benutzerdefinierte Funktion ist in den RPC-Header Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="bf851-117">**MIDL\_uhyper** is defined in the RPC header files.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="bf851-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf851-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf851-119">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="bf851-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="bf851-120">**const**</span><span class="sxs-lookup"><span data-stu-id="bf851-120">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="bf851-121">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="bf851-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="bf851-122">**typedef**</span><span class="sxs-lookup"><span data-stu-id="bf851-122">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




