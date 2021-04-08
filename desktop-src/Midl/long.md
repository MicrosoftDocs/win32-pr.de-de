---
title: Long-Attribut
description: Das Long-Schlüsselwort gibt eine 32-Bit-Ganzzahl an.
ms.assetid: 5619e482-e3c3-4898-a70b-afd337d2749a
keywords:
- Long-Attribut-Mittel l
topic_type:
- apiref
api_name:
- long
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47ea9af3bfac85ff375f6d5433b4e9f3ed37d8f7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948165"
---
# <a name="long-attribute"></a><span data-ttu-id="c0630-104">Long-Attribut</span><span class="sxs-lookup"><span data-stu-id="c0630-104">long attribute</span></span>

<span data-ttu-id="c0630-105">Das **Long** -Schlüsselwort gibt eine 32-Bit-Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="c0630-105">The **long** keyword designates a 32-bit integer.</span></span>

``` syntax
[ signed | unsigned ] long [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="c0630-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0630-107">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="c0630-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c0630-108">Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="c0630-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="c0630-109">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c0630-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="c0630-110">Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="c0630-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0630-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0630-111">Remarks</span></span>

<span data-ttu-id="c0630-112">Dem **Long** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c0630-112">The **long** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="c0630-113">Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="c0630-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="c0630-114">Für den mittlerer l-Compiler ist eine lange ganze Zahl standardmäßig signiert und mit **Signed long int** Synonym. Auf 32-Bit-Plattformen ist **Long** gleichbedeutend mit **int**.</span><span class="sxs-lookup"><span data-stu-id="c0630-114">To the MIDL compiler, a long integer is signed by default and is synonymous with **signed long int**. On 32-bit platforms, **long** is synonymous with **int**.</span></span>

<span data-ttu-id="c0630-115">Der **Long** Integer-Typ ist einer der Basis Typen der IDL-Sprache.</span><span class="sxs-lookup"><span data-stu-id="c0630-115">The **long** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="c0630-116">Der **Long** Integer-Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabe –-Typspezifizierer und als Parametertyp Spezifizierer) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c0630-116">The **long** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="c0630-117">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="c0630-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c0630-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0630-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0630-119">**const**</span><span class="sxs-lookup"><span data-stu-id="c0630-119">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="c0630-120">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="c0630-120">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="c0630-121">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="c0630-121">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="c0630-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="c0630-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="c0630-123">**short**</span><span class="sxs-lookup"><span data-stu-id="c0630-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="c0630-124">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="c0630-124">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="c0630-125">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="c0630-125">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="c0630-126">**typedef**</span><span class="sxs-lookup"><span data-stu-id="c0630-126">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="c0630-127">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="c0630-127">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




