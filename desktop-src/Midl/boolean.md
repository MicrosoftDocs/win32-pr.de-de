---
title: boolesches Attribut
description: Das Schlüsselwort boolescher Wert gibt an, dass der Ausdruck oder konstanter Ausdruck, der mit dem Bezeichner verknüpft ist, nur die Werte true und false annimmt.
ms.assetid: ed3b00a4-880f-4674-9f6d-8f5faf1eea66
keywords:
- boolesches Attribut, Mittel l
topic_type:
- apiref
api_name:
- boolean
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68959cabcef1f439ffb6df30b77aeee7056f4fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389224"
---
# <a name="boolean-attribute"></a><span data-ttu-id="14591-104">boolesches Attribut</span><span class="sxs-lookup"><span data-stu-id="14591-104">boolean attribute</span></span>

<span data-ttu-id="14591-105">Das Schlüsselwort **boolescher** Wert gibt an, dass der Ausdruck oder konstanter Ausdruck, der mit dem Bezeichner verknüpft ist, nur die Werte **true** und **false** annimmt.</span><span class="sxs-lookup"><span data-stu-id="14591-105">The keyword **boolean** indicates that the expression or constant expression associated with the identifier takes only the values **TRUE** and **FALSE**.</span></span>

``` syntax
boolean identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="14591-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14591-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14591-107">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="14591-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="14591-108">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="14591-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="14591-109">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="14591-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14591-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14591-110">Remarks</span></span>

<span data-ttu-id="14591-111">Der **boolesche** Typ ist einer der Basis Typen der IDL-Sprache.</span><span class="sxs-lookup"><span data-stu-id="14591-111">The **boolean** type is one of the base types of the IDL language.</span></span> <span data-ttu-id="14591-112">Der **boolesche** Typ kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="14591-112">The **boolean** type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="14591-113">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="14591-113">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

> [!Note]  
> <span data-ttu-id="14591-114">Der **boolesche** Basistyp ist nicht kompatibel mit dem [**oleautomation**](oleautomation.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="14591-114">The **boolean** base type is not compatible with the [**oleautomation**](oleautomation.md) attribute.</span></span> <span data-ttu-id="14591-115">Verwenden \_ Sie Variant bool in ihren Automation-kompatiblen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="14591-115">Use VARIANT\_BOOL in your Automation-compatible interfaces.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="14591-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14591-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14591-117">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="14591-117">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="14591-118">**const**</span><span class="sxs-lookup"><span data-stu-id="14591-118">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="14591-119">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="14591-119">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="14591-120">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="14591-120">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="14591-121">**typedef**</span><span class="sxs-lookup"><span data-stu-id="14591-121">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 




