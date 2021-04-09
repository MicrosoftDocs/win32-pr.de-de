---
title: retval-Attribut
description: Das Attribut \ retval \ gibt den Parameter an, der den Rückgabewert des Members empfängt.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- retval-Attribut-Mittel l
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858173"
---
# <a name="retval-attribute"></a><span data-ttu-id="633aa-104">retval-Attribut</span><span class="sxs-lookup"><span data-stu-id="633aa-104">retval attribute</span></span>

<span data-ttu-id="633aa-105">Das **\[ retval \]** -Attribut bestimmt den Parameter, der den Rückgabewert des Members empfängt.</span><span class="sxs-lookup"><span data-stu-id="633aa-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="633aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="633aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633aa-107">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="633aa-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="633aa-108">Der Datentyp des Rückgabewerts der Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="633aa-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="633aa-109">*function-name*</span><span class="sxs-lookup"><span data-stu-id="633aa-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="633aa-110">Der Name, der verwendet wird, um die Remote Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="633aa-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="633aa-111">*optionale Attribute*</span><span class="sxs-lookup"><span data-stu-id="633aa-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="633aa-112">NULL oder mehr mittlere Attribute.</span><span class="sxs-lookup"><span data-stu-id="633aa-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="633aa-113">*Datentyp*</span><span class="sxs-lookup"><span data-stu-id="633aa-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="633aa-114">Der Typ der Daten, die durch den-Parameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="633aa-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="633aa-115">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="633aa-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="633aa-116">Der Bezeichnername des Parameters.</span><span class="sxs-lookup"><span data-stu-id="633aa-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="633aa-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="633aa-117">Remarks</span></span>

<span data-ttu-id="633aa-118">Sie können das **\[ retval \]** -Attribut für Parameter von Schnittstellenmembern verwenden, die Methoden oder Get-Eigenschaften beschreiben.</span><span class="sxs-lookup"><span data-stu-id="633aa-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="633aa-119">(Das-Attribut ist für den letzten Parameter einer Methode erforderlich, die über das **\[** [**propget**](propget.md) **\]** -Attribut.) Der-Parameter muss das **\[** [**out**](out-idl.md) **\]** -Attribut aufweisen und muss ein Zeigertyp sein.</span><span class="sxs-lookup"><span data-stu-id="633aa-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="633aa-120">Sie können das **\[** [**optionale**](optional.md) - **\]** Attribut nicht auf einen **\[ retval \]** -Parameter anwenden.</span><span class="sxs-lookup"><span data-stu-id="633aa-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="633aa-121">Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):</span><span class="sxs-lookup"><span data-stu-id="633aa-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="633aa-122">Erforderliche Parameter (Parameter, die nicht über das **\[** [**DefaultValue**](defaultvalue.md) **\]** - **\[** Attribut oder [**optionale**](optional.md) **\]** Attribute verfügen).</span><span class="sxs-lookup"><span data-stu-id="633aa-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="633aa-123">Optionale Parameter mit oder ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut.</span><span class="sxs-lookup"><span data-stu-id="633aa-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="633aa-124">Parameter mit dem **\[** [**optionalen**](optional.md) **\]** -Attribut und ohne das **\[** [**DefaultValue**](defaultvalue.md) - **\]** Attribut.</span><span class="sxs-lookup"><span data-stu-id="633aa-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="633aa-125">**\[**[**LCID**](lcid.md) - **\]** Parameter (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="633aa-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="633aa-126">**\[ retval \]** -Parameter.</span><span class="sxs-lookup"><span data-stu-id="633aa-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="633aa-127">Parameter mit dem **\[ retval \]** -Attribut werden in benutzerorientierten Browsern nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="633aa-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="633aa-128">Flags</span><span class="sxs-lookup"><span data-stu-id="633aa-128">Flags</span></span>

<span data-ttu-id="633aa-129">IDLFLAG \_ fretval</span><span class="sxs-lookup"><span data-stu-id="633aa-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="633aa-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="633aa-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="633aa-131">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="633aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633aa-132">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="633aa-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="633aa-133">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="633aa-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="633aa-134">**LCID**</span><span class="sxs-lookup"><span data-stu-id="633aa-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="633aa-135">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="633aa-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="633aa-136">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="633aa-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="633aa-137">**optionale**</span><span class="sxs-lookup"><span data-stu-id="633aa-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="633aa-138">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="633aa-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="633aa-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="633aa-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="633aa-140">**FUNCFLAGS**</span><span class="sxs-lookup"><span data-stu-id="633aa-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 