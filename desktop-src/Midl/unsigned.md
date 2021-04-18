---
title: nicht signiertes Attribut
description: Das Ganzzahl ohne Vorzeichen-Schlüsselwort gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Daten Bit anstelle eines signierten Bits darstellt.
ms.assetid: bfcc6bec-895e-45e1-b162-b79651662aa6
keywords:
- Ganzzahl ohne Vorzeichen-Attribut, Mittel l
topic_type:
- apiref
api_name:
- unsigned
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329d638f1b5be97e5b441aa4e84825fe59a4a3f0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339248"
---
# <a name="unsigned-attribute"></a><span data-ttu-id="fc6b2-104">nicht signiertes Attribut</span><span class="sxs-lookup"><span data-stu-id="fc6b2-104">unsigned attribute</span></span>

<span data-ttu-id="fc6b2-105">Das **Ganzzahl ohne Vorzeichen** -Schlüsselwort gibt an, dass das signifikanteste Bit einer ganzzahligen Variablen ein Daten Bit anstelle eines signierten Bits darstellt.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-105">The **unsigned** keyword indicates that the most significant bit of an integer variable represents a data bit rather than a signed bit.</span></span>

``` syntax
[[ unsigned ]] type-qualifier [[ int ]]identifier-name;
```

## <a name="parameters"></a><span data-ttu-id="fc6b2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc6b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6b2-107">*type-qualifier*</span><span class="sxs-lookup"><span data-stu-id="fc6b2-107">*type-qualifier*</span></span> 
</dt> <dd>

<span data-ttu-id="fc6b2-108">Kann " [**char**](char-idl.md)", " [**WCHAR \_ t**](wchar-t.md)", " [**Long**](long.md)", " [**int**](int.md)", " [**Short**](short.md)" und [**klein**](small.md)sein.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-108">Can be any of [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**int**](int.md), [**short**](short.md), and [**small**](small.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc6b2-109">*Bezeichnername*</span><span class="sxs-lookup"><span data-stu-id="fc6b2-109">*identifier-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fc6b2-110">Gibt einen gültigen Mittell-Bezeichner an.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-110">Specifies a valid MIDL identifier.</span></span> <span data-ttu-id="fc6b2-111">Gültige Mittell-Bezeichner bestehen aus bis zu 31 alphanumerischen Zeichen und/oder unterstrichen und müssen mit einem Buchstaben oder einem Unterstrich beginnen.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-111">Valid MIDL identifiers consist of up to 31 alphanumeric and/or underscore characters and must start with an alphabetic or underscore character.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc6b2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc6b2-112">Remarks</span></span>

<span data-ttu-id="fc6b2-113">Dieses Schlüsselwort ist optional und kann mit jedem der Zeichen-und ganzzahligen Typen [**char**](char-idl.md), [**WCHAR \_ t**](wchar-t.md), [**Long**](long.md), [**Short**](short.md)und [**Small**](small.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-113">This keyword is optional and can be used with any of the character and integer types [**char**](char-idl.md), [**wchar\_t**](wchar-t.md), [**long**](long.md), [**short**](short.md), and [**small**](small.md).</span></span> <span data-ttu-id="fc6b2-114">Sie können optional das Schlüsselwort [**int**](int.md) nach den typqualifizierern **Long**, **Short** und **Small** einschließen.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-114">You can optionally include the keyword [**int**](int.md) after the type qualifiers **long**, **short**, and **small**.</span></span>

<span data-ttu-id="fc6b2-115">Wenn Sie den Compilerschalter [**/char**](-char.md)verwenden, können Zeichen-und ganzzahlige Typen, die in der IDL-Datei ohne explizite Vorzeichen vorkommen, mit dem Schlüsselwort [**Signed**](signed.md) oder **Ganzzahl ohne Vorzeichen** in der generierten Header Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-115">When you use the MIDL compiler switch [**/char**](-char.md), character and integer types that appear in the IDL file without explicit sign keywords can appear with the [**signed**](signed.md) or **unsigned** keyword in the generated header file.</span></span> <span data-ttu-id="fc6b2-116">Um Verwirrung zu vermeiden, geben Sie das Vorzeichen der ganzzahligen und Zeichen Typen an.</span><span class="sxs-lookup"><span data-stu-id="fc6b2-116">To avoid confusion, specify the sign of the integer and character types.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc6b2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc6b2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc6b2-118">Mittel l-Basis Typen</span><span class="sxs-lookup"><span data-stu-id="fc6b2-118">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-119">**Char**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-119">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-120">**/Char**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-120">**/char**</span></span>](-char.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-121">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="fc6b2-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-122">**INT**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-122">**int**</span></span>](int.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-123">**lange**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-123">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-124">**short**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-124">**short**</span></span>](short.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-125">**ebenes**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-125">**signed**</span></span>](signed.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-126">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-126">**small**</span></span>](small.md)
</dt> <dt>

[<span data-ttu-id="fc6b2-127">**WCHAR \_ t**</span><span class="sxs-lookup"><span data-stu-id="fc6b2-127">**wchar\_t**</span></span>](wchar-t.md)
</dt> </dl>

 

 




