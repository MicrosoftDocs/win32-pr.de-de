---
title: signiertes Attribut
description: Das Schlüsselwort signed gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Signier Bit anstelle eines Datenbits darstellt.
ms.assetid: 6116089a-647e-485b-8f79-9c9267aa4810
keywords:
- signiertes Attribut "Mittel l"
topic_type:
- apiref
api_name:
- signed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500b87c849f31082a036d605db0947650e914bed
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857084"
---
# <a name="signed-attribute"></a><span data-ttu-id="062be-104">signiertes Attribut</span><span class="sxs-lookup"><span data-stu-id="062be-104">signed attribute</span></span>

<span data-ttu-id="062be-105">Das Schlüsselwort **Signed** gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Signier Bit anstelle eines Datenbits darstellt.</span><span class="sxs-lookup"><span data-stu-id="062be-105">The **signed** keyword indicates the most significant bit of an integer variable represents a sign bit rather than a data bit.</span></span>

``` syntax
[[ signed ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="062be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="062be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="062be-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="062be-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="062be-108">Kann " [**char**](char-idl.md)", " [**WCHAR \_ t**](wchar-t.md)", " [**Long**](long.md)", " [**Short**](short.md)" und " [**Small**](small.md)" lauten.</span><span class="sxs-lookup"><span data-stu-id="062be-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="062be-109">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="062be-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="062be-110">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="062be-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="062be-111">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="062be-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="062be-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="062be-112">Remarks</span></span>

<span data-ttu-id="062be-113">Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen-und ganzzahligen Typen [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)und [**Small**](small.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="062be-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="062be-114">Sie können optional das Schlüsselwort [**int**](int.md) nach den typqualifizierern **Long**, **Short** und **Small** einschließen.</span><span class="sxs-lookup"><span data-stu-id="062be-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="062be-115">Wenn Sie den-Compilerschalter [**char**](char-idl.md)verwenden, können Zeichen-und ganzzahlige Typen, die in der IDL-Datei ohne explizite Vorzeichen vorkommen, mit den Schlüsselwörtern **Signed** oder [**Ganzzahl ohne Vorzeichen**](unsigned.md) in der generierten Header Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="062be-115">When you use the MIDL compiler switch [**char**](char-idl.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the **signed** or [**unsigned**](unsigned.md) keywords in the generated header file.</span></span> <span data-ttu-id="062be-116">Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der ganzzahligen und Zeichen Typen an.</span><span class="sxs-lookup"><span data-stu-id="062be-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="062be-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="062be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="062be-118">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="062be-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="062be-119">**/Char**</span><span class="sxs-lookup"><span data-stu-id="062be-119">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="062be-120">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="062be-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="062be-121">**INT**</span><span class="sxs-lookup"><span data-stu-id="062be-121">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="062be-122">**lange**</span><span class="sxs-lookup"><span data-stu-id="062be-122">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="062be-123">**short**</span><span class="sxs-lookup"><span data-stu-id="062be-123">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="062be-124">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="062be-124">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="062be-125">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="062be-125">**unsigned**</span></span>](unsigned.md)
</dt> <dt>

[<span data-ttu-id="062be-126">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="062be-126">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




