---
title: Small-Attribut
description: Das Small-Schlüsselwort gibt eine 8-Bit-Ganzzahl an.
ms.assetid: 368e8836-1baa-4547-a62b-f34ac38bbdb2
keywords:
- Small Attribute-Mittel l
topic_type:
- apiref
api_name:
- small
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a0f106f1be1ba6d0acabf877b5dbefab3eaff6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389002"
---
# <a name="small-attribute"></a><span data-ttu-id="08c1e-104">Small-Attribut</span><span class="sxs-lookup"><span data-stu-id="08c1e-104">small attribute</span></span>

<span data-ttu-id="08c1e-105">Das **Small** -Schlüsselwort gibt eine 8-Bit-Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="08c1e-105">The **small** keyword designates an 8-bit integer number.</span></span>

``` syntax
small identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="08c1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="08c1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08c1e-107">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="08c1e-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="08c1e-108">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="08c1e-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="08c1e-109">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="08c1e-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08c1e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08c1e-110">Remarks</span></span>

<span data-ttu-id="08c1e-111">Dem **Small** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="08c1e-111">The **small** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="08c1e-112">Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="08c1e-112">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="08c1e-113">Für den mittlerer l-Compiler ist standardmäßig eine kleine Ganzzahl **signiert** und ist mit dem Wert " **Signed Small int**" Synonym.</span><span class="sxs-lookup"><span data-stu-id="08c1e-113">To the MIDL compiler, a small integer is **signed** by default and is synonymous with **signed small int**.</span></span>

<span data-ttu-id="08c1e-114">Der **kleine** ganzzahlige Typ ist einer der Basis Typen der IDL-Sprache.</span><span class="sxs-lookup"><span data-stu-id="08c1e-114">The **small** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="08c1e-115">Der **Small** Integer-Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabe –-Typspezifizierer und als Parametertyp Spezifizierer) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="08c1e-115">The **small** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return–type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="08c1e-116">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="08c1e-116">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="08c1e-117">Das Vorzeichen des **kleinen** Typs kann mit dem Mittell-Compilerschalter [**/char**](-char.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="08c1e-117">The sign of the **small** type can be modified by the MIDL compiler switch [**/char**](-char.md).</span></span> <span data-ttu-id="08c1e-118">Um Verwirrung zu vermeiden, geben Sie das Vorzeichen des ganzzahligen Typs mit den Schlüsselwörtern [**signiert**](signed.md) und [**unsigniert**](unsigned.md)an.</span><span class="sxs-lookup"><span data-stu-id="08c1e-118">To avoid confusion, specify the sign of the integer type with the keywords [**signed**](signed.md) and [**unsigned**](unsigned.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="08c1e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08c1e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08c1e-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="08c1e-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="08c1e-121">**const**</span><span class="sxs-lookup"><span data-stu-id="08c1e-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="08c1e-122">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="08c1e-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="08c1e-123">**INT**</span><span class="sxs-lookup"><span data-stu-id="08c1e-123">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="08c1e-124">**lange**</span><span class="sxs-lookup"><span data-stu-id="08c1e-124">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="08c1e-125">**short**</span><span class="sxs-lookup"><span data-stu-id="08c1e-125">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="08c1e-126">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="08c1e-126">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="08c1e-127">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="08c1e-127">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="08c1e-128">**typedef**</span><span class="sxs-lookup"><span data-stu-id="08c1e-128">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




