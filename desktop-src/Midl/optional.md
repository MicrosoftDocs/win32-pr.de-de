---
title: Optionales Attribut
description: Das \ optionale \-Attribut gibt einen optionalen Parameter für eine Member-Funktion an.
ms.assetid: 683e5c9e-5b25-4beb-99ce-cfae4fee4ea6
keywords:
- optionales Attribut-Mittel l
topic_type:
- apiref
api_name:
- optional
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b446cf2a7a14e5909d2c99d41fd918147d23c6f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858239"
---
# <a name="optional-attribute"></a><span data-ttu-id="4ae47-104">Optionales Attribut</span><span class="sxs-lookup"><span data-stu-id="4ae47-104">optional attribute</span></span>

<span data-ttu-id="4ae47-105">Das **\[ optionale \]** -Attribut gibt einen optionalen Parameter für eine Member-Funktion an.</span><span class="sxs-lookup"><span data-stu-id="4ae47-105">The **\[optional\]** attribute specifies an optional parameter for a member function.</span></span>

``` syntax
return-type function-name([optional [, other-attributes]] parameter-type parameter-name)
```

## <a name="parameters"></a><span data-ttu-id="4ae47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4ae47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ae47-107">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="4ae47-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae47-108">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="4ae47-108">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="4ae47-109">*function-name*</span><span class="sxs-lookup"><span data-stu-id="4ae47-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae47-110">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="4ae47-110">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="4ae47-111">*andere-Attribute*</span><span class="sxs-lookup"><span data-stu-id="4ae47-111">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae47-112">NULL oder mehr optionale Mittelwert Attribute.</span><span class="sxs-lookup"><span data-stu-id="4ae47-112">Zero or more optional MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="4ae47-113">*Parametertyp*</span><span class="sxs-lookup"><span data-stu-id="4ae47-113">*parameter-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae47-114">Der Datentyp des optionalen Parameters.</span><span class="sxs-lookup"><span data-stu-id="4ae47-114">The data type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4ae47-115">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="4ae47-115">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4ae47-116">Gibt den Namen des optionalen Parameters an.</span><span class="sxs-lookup"><span data-stu-id="4ae47-116">Specifies the name of the optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4ae47-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ae47-117">Remarks</span></span>

<span data-ttu-id="4ae47-118">Das **\[ optionale \]** -Attribut ist nur gültig, wenn der-Parameter vom Typ **Variant** oder **Variant** ist \* .</span><span class="sxs-lookup"><span data-stu-id="4ae47-118">The **\[optional\]** attribute is valid only if the parameter is of type **VARIANT** or **VARIANT** Â \*.</span></span>

<span data-ttu-id="4ae47-119">Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):</span><span class="sxs-lookup"><span data-stu-id="4ae47-119">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="4ae47-120">Erforderliche Parameter (Parameter, die nicht über das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut oder **\[ optionale \]** Attribute verfügen)</span><span class="sxs-lookup"><span data-stu-id="4ae47-120">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[optional\]** attributes),</span></span>
2.  <span data-ttu-id="4ae47-121">Optionale Parameter mit oder ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut</span><span class="sxs-lookup"><span data-stu-id="4ae47-121">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
3.  <span data-ttu-id="4ae47-122">Parameter mit dem **\[ optionalen \]** -Attribut und ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut</span><span class="sxs-lookup"><span data-stu-id="4ae47-122">Parameters with the **\[optional\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute,</span></span>
4.  <span data-ttu-id="4ae47-123">**\[**[**LCID**](lcid.md) - **\]** Parameter (falls vorhanden)</span><span class="sxs-lookup"><span data-stu-id="4ae47-123">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="4ae47-124">**\[**[**retval**](retval.md) **\]** Parame</span><span class="sxs-lookup"><span data-stu-id="4ae47-124">**\[**[**retval**](retval.md)**\]** parameter</span></span>

<span data-ttu-id="4ae47-125">Sie können das **\[ \] optionale** -Attribut nicht auf einen Parameter anwenden, der auch über die **\[** [**LCID**](lcid.md) - **\]** oder **\[** [**retval**](retval.md) -Attribute verfügt **\]** .</span><span class="sxs-lookup"><span data-stu-id="4ae47-125">You cannot apply the **\[optional\]** attribute to a parameter that also has the **\[**[**lcid**](lcid.md)**\]** or **\[**[**retval**](retval.md)**\]** attributes.</span></span>

## <a name="examples"></a><span data-ttu-id="4ae47-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4ae47-126">Examples</span></span>

``` syntax
HRESULT MyFunc([in, optional] VARIANT Param1, 
               [out, optional] VARIANT Param2)
```

## <a name="see-also"></a><span data-ttu-id="4ae47-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4ae47-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae47-128">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="4ae47-128">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="4ae47-129">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="4ae47-129">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4ae47-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="4ae47-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="4ae47-131">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4ae47-131">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4ae47-132">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4ae47-132">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4ae47-133">**retval**</span><span class="sxs-lookup"><span data-stu-id="4ae47-133">**retval**</span></span>](retval.md)
</dt> </dl>

 

 