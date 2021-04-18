---
title: vararg-Attribut
description: Das Attribut \ vararg \ gibt an, dass die Funktion eine Variable Anzahl von Parametern annimmt. Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom Variant-Typ sein, das alle verbleibenden Parameter enthält.
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- vararg-Attribut-Mittel l
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337224"
---
# <a name="vararg-attribute"></a><span data-ttu-id="4574a-105">vararg-Attribut</span><span class="sxs-lookup"><span data-stu-id="4574a-105">vararg attribute</span></span>

<span data-ttu-id="4574a-106">Das **\[ vararg \]** -Attribut gibt an, dass die Funktion eine Variable Anzahl von Parametern annimmt.</span><span class="sxs-lookup"><span data-stu-id="4574a-106">The **\[vararg\]** attribute specifies that the function takes a variable number of parameters.</span></span> <span data-ttu-id="4574a-107">Um dies zu erreichen, muss der letzte Parameter ein sicheres Array vom **Variant** -Typ sein, das alle verbleibenden Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="4574a-107">To accomplish this, the last parameter must be a safe array of **VARIANT** type that contains all the remaining parameters.</span></span>

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a><span data-ttu-id="4574a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4574a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4574a-109">*optionale Attribute*</span><span class="sxs-lookup"><span data-stu-id="4574a-109">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-110">Gibt 0 (null) oder mehr Attribute an, die auf die Funktion angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4574a-110">Specifies zero or more attributes to be applied to the function.</span></span> <span data-ttu-id="4574a-111">Trennen Sie mehrere Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="4574a-111">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="4574a-112">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="4574a-112">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-113">Der Typ der Daten, die von der Remote Prozedur nach Abschluss des Vorgangs zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4574a-113">The type of the data returned by the remote procedure upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="4574a-114">*function-name*</span><span class="sxs-lookup"><span data-stu-id="4574a-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-115">Der Name der Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="4574a-115">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="4574a-116">*optional-param-Attribute*</span><span class="sxs-lookup"><span data-stu-id="4574a-116">*optional-param-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-117">Gibt 0 (null) oder mehr Attribute an, die auf den Funktionsparameter direkt nach der Attribut Auflistung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4574a-117">Specifies zero or more attributes to be applied to the function parameter immediately following the attribute listing.</span></span>

</dd> <dt>

<span data-ttu-id="4574a-118">*param-Liste*</span><span class="sxs-lookup"><span data-stu-id="4574a-118">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-119">Gibt alle Parameter an, speichert den abschließenden, variierenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="4574a-119">Specifies all the parameters, save the final, varying, parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4574a-120">*Last-Param-Name*</span><span class="sxs-lookup"><span data-stu-id="4574a-120">*last-param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="4574a-121">Der Name des variierenden Parameters.</span><span class="sxs-lookup"><span data-stu-id="4574a-121">The name of the varying parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4574a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4574a-122">Remarks</span></span>

<span data-ttu-id="4574a-123">Die **\[** [**optionalen**](optional.md) **\]** Attribute oder **\[** [**DefaultValue**](defaultvalue.md) -Attribute können nicht **\]** auf Parameter in einer Funktion angewendet werden, die das **\[ \] vararg** -Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="4574a-123">You cannot apply the **\[**[**optional**](optional.md)**\]** or **\[**[**defaultvalue**](defaultvalue.md)**\]** attributes to any parameters in a function that has the **\[vararg\]** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="4574a-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4574a-124">Examples</span></span>

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a><span data-ttu-id="4574a-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4574a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4574a-126">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="4574a-126">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="4574a-127">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="4574a-127">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="4574a-128">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4574a-128">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="4574a-129">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="4574a-129">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="4574a-130">**optionale**</span><span class="sxs-lookup"><span data-stu-id="4574a-130">**optional**</span></span>](optional.md)
</dt> </dl>

 

 