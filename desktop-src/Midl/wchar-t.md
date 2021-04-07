---
title: wchar_t-Attribut
description: Das WCHAR \_ t-Schlüsselwort legt einen breit Zeichentyp fest.
ms.assetid: e21b2587-909a-4e2b-8c6d-6cc570bf509f
keywords:
- wchar_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- wchar_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0be9af276a8f87fe5ee7a4dfeb499b864de92f4
ms.sourcegitcommit: 686cb805bed0e89573fc68d145809f50c6b0e6d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "104038648"
---
# <a name="wchar_t-attribute"></a><span data-ttu-id="0b998-104">WCHAR \_ t-Attribut</span><span class="sxs-lookup"><span data-stu-id="0b998-104">wchar\_t attribute</span></span>

<span data-ttu-id="0b998-105">Das **WCHAR \_ t** -Schlüsselwort legt einen breit Zeichentyp fest.</span><span class="sxs-lookup"><span data-stu-id="0b998-105">The **wchar\_t** keyword designates a wide-character type.</span></span>

``` syntax
wchar_t identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="0b998-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b998-107">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="0b998-107">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="0b998-108">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="0b998-108">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="0b998-109">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="0b998-109">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b998-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b998-110">Remarks</span></span>

<span data-ttu-id="0b998-111">Der Typ " **WCHAR \_ t** " wird von "Mittel l" als [**unsigniertes**](unsigned.md) [**kurzes**](short.md) (16-Bit-) Datenobjekt definiert.</span><span class="sxs-lookup"><span data-stu-id="0b998-111">The **wchar\_t** type is defined by MIDL as an [**unsigned**](unsigned.md) [**short**](short.md) (16-bit) data object.</span></span>

<span data-ttu-id="0b998-112">Der mittlerer l-Compiler lässt die Neudefinition von **WCHAR \_ t** zu, jedoch nur, wenn er mit der vorangehenden Definition konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="0b998-112">The MIDL compiler allows redefinition of **wchar\_t**, but only if it is consistent with the preceding definition.</span></span>

<span data-ttu-id="0b998-113">Der breit Zeichentyp ist einer der vordefinierten Typen von "Mittel l".</span><span class="sxs-lookup"><span data-stu-id="0b998-113">The wide-character type is one of the predefined types of MIDL.</span></span> <span data-ttu-id="0b998-114">Der breit Zeichentyp kann als Typspezifizierer in [**Konstanten**](const.md) Deklarationen, [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0b998-114">The wide-character type can appear as a type specifier in [**const**](const.md) declarations, [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function return type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="0b998-115">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="0b998-115">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="0b998-116">Das **\[ String \]** -Attribut kann auf einen Zeiger oder ein Array vom Typ " **WCHAR \_ t**" angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="0b998-116">The **\[string\]** attribute can be applied to a pointer or array of type **wchar\_t**.</span></span>

<span data-ttu-id="0b998-117">Verwenden Sie das **L** -Zeichen vor einem Zeichen oder einer Zeichen folgen Konstante, um die Konstante für den breit Zeichentyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0b998-117">Use the **L** character before a character or a string constant to designate the wide character type constant.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b998-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b998-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b998-119">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="0b998-119">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="0b998-120">**Char**</span><span class="sxs-lookup"><span data-stu-id="0b998-120">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="0b998-121">**const**</span><span class="sxs-lookup"><span data-stu-id="0b998-121">**const**</span></span>](const.md)
</dt> <dt>

[<span data-ttu-id="0b998-122">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="0b998-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="0b998-123">**short**</span><span class="sxs-lookup"><span data-stu-id="0b998-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="0b998-124">**typedef**</span><span class="sxs-lookup"><span data-stu-id="0b998-124">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="0b998-125">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="0b998-125">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




