---
title: int-Attribut
description: Das Schlüsselwort int gibt eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an. Auf 16-Bit-Plattformen ist das Schlüsselwort int ein optionales Schlüsselwort, das die Schlüsselwörter Small, Short und Long begleitet.
ms.assetid: ad6ce0ff-e87b-4701-b9d2-a69c34e0339b
keywords:
- int-Attribut-Mittel l
topic_type:
- apiref
api_name:
- int
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f916c4f03023c756b71a2e3cbb38acd9f41f1e8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718065"
---
# <a name="int-attribute"></a><span data-ttu-id="3326e-105">int-Attribut</span><span class="sxs-lookup"><span data-stu-id="3326e-105">int attribute</span></span>

<span data-ttu-id="3326e-106">Das Schlüsselwort **int** gibt eine 32-Bit-Ganzzahl mit Vorzeichen auf 32-Bit-Plattformen an.</span><span class="sxs-lookup"><span data-stu-id="3326e-106">The keyword **int** specifies a 32-bit signed integer on 32-bit platforms.</span></span> <span data-ttu-id="3326e-107">Auf 16-Bit-Plattformen ist das Schlüsselwort **int** ein optionales Schlüsselwort, das die Schlüsselwörter [**Small**](small.md), [**Short**](short.md)und [**Long**](long.md)begleitet.</span><span class="sxs-lookup"><span data-stu-id="3326e-107">On 16-bit platforms, the keyword **int** is an optional keyword that can accompany the keywords [**small**](small.md), [**short**](short.md), and [**long**](long.md).</span></span>

``` syntax
[ signed | unsigned ] integer-modifier [ int ] declarator-list;
```

## <a name="parameters"></a><span data-ttu-id="3326e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3326e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3326e-109">*ganzzahliger Modifizierer*</span><span class="sxs-lookup"><span data-stu-id="3326e-109">*integer-modifier*</span></span> 
</dt> <dd>

<span data-ttu-id="3326e-110">Gibt das Schlüsselwort [**Small**](small.md), [**Short**](short.md), [**Long**](long.md), [**Hyper**](hyper.md), [**\_ \_ int3264**](--int3264.md)oder [**\_ \_ Int64**](--int64.md)an, mit dem die Größe der ganzzahligen Daten ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="3326e-110">Specifies the keyword [**small**](small.md), [**short**](short.md), [**long**](long.md), [**hyper**](hyper.md), [**\_\_int3264**](--int3264.md), or [**\_\_int64**](--int64.md),which selects the size of the integer data.</span></span> <span data-ttu-id="3326e-111">Auf 16-Bit-Plattformen muss der Größen Qualifizierer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3326e-111">On 16-bit platforms, the size qualifier must be present.</span></span>

</dd> <dt>

<span data-ttu-id="3326e-112">*Deklarator-List*</span><span class="sxs-lookup"><span data-stu-id="3326e-112">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3326e-113">Gibt einen oder mehrere Standard-C-Deklaratoren an, z. b. Bezeichner, zeigerdeklaratoren und Array Deklaratoren.</span><span class="sxs-lookup"><span data-stu-id="3326e-113">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3326e-114">(Funktions Deklaratoren und Bitfeld Deklarationen sind in Strukturen, die in Remote Prozedur aufrufen übertragen werden, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3326e-114">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="3326e-115">Diese Deklaratoren sind in Strukturen zulässig, die nicht übertragen werden.) Trennen Sie mehrere Deklaratoren durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="3326e-115">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3326e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3326e-116">Remarks</span></span>

<span data-ttu-id="3326e-117">Ganzzahlige Typen gehören zu den Basis Typen der Schnittstellen Definitions Sprache (IDL).</span><span class="sxs-lookup"><span data-stu-id="3326e-117">Integer types are among the base types of the interface definition language (IDL).</span></span> <span data-ttu-id="3326e-118">Sie können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (als Funktionsrückgabetyp-Spezifizierer und als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3326e-118">They can appear as type specifiers in [**typedef**](typedef.md) declarations, general declarations, and function declarators (as a function-return-type specifier and as a parameter-type specifier).</span></span> <span data-ttu-id="3326e-119">Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="3326e-119">For the context in which type specifiers appear, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

<span data-ttu-id="3326e-120">Wenn keine ganzzahlige Vorzeichen Angabe bereitgestellt wird, ist der ganzzahlige Typ standardmäßig [**signiert**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="3326e-120">If no integer sign specification is provided, the integer type defaults to [**signed**](signed.md).</span></span>

<span data-ttu-id="3326e-121">DCE-IDL-Compiler lassen nicht zu, dass das Schlüsselwort [**signiert**](signed.md) ist, um das Vorzeichen von ganzzahligen Typen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3326e-121">DCE IDL compilers do not allow the keyword [**signed**](signed.md) to specify the sign of integer types.</span></span> <span data-ttu-id="3326e-122">Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.</span><span class="sxs-lookup"><span data-stu-id="3326e-122">Therefore, this feature is not available when you use the MIDL compiler [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="3326e-123">Microsoft empfiehlt nicht die Verwendung von \_ \_ int3264 für Remoting, wenn dies vermieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="3326e-123">Microsoft does not recommend the use of \_\_int3264 for remoting if it can be avoided.</span></span> <span data-ttu-id="3326e-124">Weitere Informationen zur Verwendung und zu den Einschränkungen finden Sie im Thema zu [**\_ \_ int3264**](--int3264.md) .</span><span class="sxs-lookup"><span data-stu-id="3326e-124">Please see the topic on [**\_\_int3264**](--int3264.md) for more information regarding it's use and limitations.</span></span>

## <a name="examples"></a><span data-ttu-id="3326e-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3326e-125">Examples</span></span>

``` syntax
signed short int i = 0; 
int j = i; 
typedef struct 
{ 
    small int         i1; 
    short             i2; 
    unsigned long int i3; 
} INTSIZETYPE; 
 
HRESULT MyFunc([in] long int lCount);
```

## <a name="see-also"></a><span data-ttu-id="3326e-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3326e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3326e-127">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="3326e-127">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="3326e-128">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="3326e-128">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="3326e-129">**Hyper**</span><span class="sxs-lookup"><span data-stu-id="3326e-129">**hyper**</span></span>](hyper.md)
</dt> <dt>

[<span data-ttu-id="3326e-130">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="3326e-130">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3326e-131">**lange**</span><span class="sxs-lookup"><span data-stu-id="3326e-131">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="3326e-132">**/osf**</span><span class="sxs-lookup"><span data-stu-id="3326e-132">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="3326e-133">**short**</span><span class="sxs-lookup"><span data-stu-id="3326e-133">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="3326e-134">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="3326e-134">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="3326e-135">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="3326e-135">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="3326e-136">**struct**</span><span class="sxs-lookup"><span data-stu-id="3326e-136">**struct**</span></span>](struct.md)
</dt> <dt>

[<span data-ttu-id="3326e-137">**typedef**</span><span class="sxs-lookup"><span data-stu-id="3326e-137">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="3326e-138">**Union**</span><span class="sxs-lookup"><span data-stu-id="3326e-138">**union**</span></span>](union.md)
</dt> </dl>

 

 




