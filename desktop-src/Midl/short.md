---
title: kurzes Attribut
description: Das Short-Schlüsselwort legt eine 16-Bit-Ganzzahl fest.
ms.assetid: 622464a3-0d79-421a-8742-8a3746fe1533
keywords:
- kurzes Attribut-Mittel l
topic_type:
- apiref
api_name:
- short
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b993c830c631b5b95246a7a191388ce897dbaafb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312743"
---
# <a name="short-attribute"></a><span data-ttu-id="0b01c-104">kurzes Attribut</span><span class="sxs-lookup"><span data-stu-id="0b01c-104">short attribute</span></span>

<span data-ttu-id="0b01c-105">Das **Short** -Schlüsselwort legt eine 16-Bit-Ganzzahl fest.</span><span class="sxs-lookup"><span data-stu-id="0b01c-105">The **short** keyword designates a 16-bit integer.</span></span>

``` syntax
[[ signed | unsigned ]] short [[ int ]] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="0b01c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b01c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b01c-107">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="0b01c-107">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="0b01c-108">Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="0b01c-108">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="0b01c-109">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0b01c-109">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="0b01c-110">Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="0b01c-110">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b01c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b01c-111">Remarks</span></span>

<span data-ttu-id="0b01c-112">Dem **Short** -Schlüsselwort kann entweder das Schlüsselwort [**signiert**](signed.md) oder das Schlüsselwort [**unsigniert**](unsigned.md)vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0b01c-112">The **short** keyword can be preceded by either the keyword [**signed**](signed.md) or the keyword [**unsigned**](unsigned.md).</span></span> <span data-ttu-id="0b01c-113">Das [**int**](int.md) -Schlüsselwort ist optional und kann ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="0b01c-113">The [**int**](int.md) keyword is optional and can be omitted.</span></span> <span data-ttu-id="0b01c-114">Für den mittlerer l-Compiler ist standardmäßig eine kurze Ganzzahl signiert und mit einem **Signed short int**-Wert Synonym.</span><span class="sxs-lookup"><span data-stu-id="0b01c-114">To the MIDL compiler, a short integer is signed by default and is synonymous with **signed short int**.</span></span>

<span data-ttu-id="0b01c-115">Der **kurze ganzzahlige** Typ ist einer der Basis Typen der IDL-Sprache.</span><span class="sxs-lookup"><span data-stu-id="0b01c-115">The **short** integer type is one of the base types of the IDL language.</span></span> <span data-ttu-id="0b01c-116">Der **kurze ganzzahlige** Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktions Rückgabetyp-Spezifizierer und Parameter-Typspezifizierer) vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0b01c-116">The **short** integer type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and a parameter-type specifier).</span></span> <span data-ttu-id="0b01c-117">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b01c-117">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b01c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b01c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b01c-119">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="0b01c-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="0b01c-120">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="0b01c-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0b01c-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="0b01c-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="0b01c-122">**lange**</span><span class="sxs-lookup"><span data-stu-id="0b01c-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="0b01c-123">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="0b01c-123">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="0b01c-124">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="0b01c-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="0b01c-125">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="0b01c-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




