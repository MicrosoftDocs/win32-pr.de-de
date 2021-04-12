---
title: defaultvalue-Attribut
description: Mit dem Attribut "\ DefaultValue \" können Sie einen Standardwert für einen eingegebenen optionalen Parameter angeben.
ms.assetid: a974a0f7-7b08-4f17-bb28-0e23e6aa97db
keywords:
- DefaultValue-Attribut (Mitte)
topic_type:
- apiref
api_name:
- defaultvalue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04f4efaac16325ec77721665a4dee14c9514a192
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314979"
---
# <a name="defaultvalue-attribute"></a><span data-ttu-id="2fc57-104">defaultvalue-Attribut</span><span class="sxs-lookup"><span data-stu-id="2fc57-104">defaultvalue attribute</span></span>

<span data-ttu-id="2fc57-105">Mit dem **\[ DefaultValue \]** -Attribut können Sie einen Standardwert für einen eingegebenen optionalen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="2fc57-105">The **\[defaultvalue\]** attribute allows you to specify a default value for a typed optional parameter.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        mandatory-param-list, 
        [[attribute-list,] defaultvalue(value)] param-type param-name
        [ , optional-param-list]);
}
```

## <a name="parameters"></a><span data-ttu-id="2fc57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fc57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc57-107">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="2fc57-107">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-108">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="2fc57-108">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-109">*Rückgabetyp*</span><span class="sxs-lookup"><span data-stu-id="2fc57-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-110">Gibt den Rückgabetyp der Funktion an.</span><span class="sxs-lookup"><span data-stu-id="2fc57-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-111">*function-name*</span><span class="sxs-lookup"><span data-stu-id="2fc57-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-112">Gibt den Namen der Funktion an, auf die das **\[ DefaultValue \]** -Attribut angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2fc57-112">Specifies the name of the function to which the **\[defaultvalue\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-113">*obligatorisch-param-List*</span><span class="sxs-lookup"><span data-stu-id="2fc57-113">*mandatory-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-114">Gibt ein oder mehrere erforderliche Parameter an.</span><span class="sxs-lookup"><span data-stu-id="2fc57-114">Specifies on or more required parameters.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-115">*Attribut-List*</span><span class="sxs-lookup"><span data-stu-id="2fc57-115">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-116">Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den-Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc57-116">Specifies a list of one or more attributes, separated by commas, that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-117">*param-Typ*</span><span class="sxs-lookup"><span data-stu-id="2fc57-117">*param-type*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-118">Gibt den Typ des optionalen Parameters an.</span><span class="sxs-lookup"><span data-stu-id="2fc57-118">Indicates the type of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-119">*Param-Name*</span><span class="sxs-lookup"><span data-stu-id="2fc57-119">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-120">Gibt den Namen des optionalen Parameters an.</span><span class="sxs-lookup"><span data-stu-id="2fc57-120">Specifies the name of the optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2fc57-121">*optional-param-List*</span><span class="sxs-lookup"><span data-stu-id="2fc57-121">*optional-param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="2fc57-122">Gibt 0 (null) oder mehr zusätzliche Parameter an, von denen jeder über einen Standardwert verfügen muss.</span><span class="sxs-lookup"><span data-stu-id="2fc57-122">Specifies zero or more additional parameters, each of which must have a default value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fc57-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fc57-123">Remarks</span></span>

<span data-ttu-id="2fc57-124">Der Standardwert, den Sie für den-Parameter angeben, kann eine beliebige Konstante oder ein Ausdruck sein, der zu einer Konstante aufgelöst wird, der durch eine **Variante** dargestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2fc57-124">The default value you specify for the parameter can be any constant, or an expression that resolves to a constant, that can be represented by a **VARIANT**.</span></span> <span data-ttu-id="2fc57-125">Insbesondere kann das **\[ DefaultValue \]** -Attribut nicht auf einen Parameter angewendet werden, bei dem es sich um eine Struktur, ein Array oder einen **SAFEARRAY** -Typ handelt.</span><span class="sxs-lookup"><span data-stu-id="2fc57-125">Specifically, you cannot apply the **\[defaultvalue\]** attribute to a parameter that is a structure, an array, or a **SAFEARRAY** type.</span></span>

<span data-ttu-id="2fc57-126">Der mittlerer l-Compiler akzeptiert die folgende Parameter Reihenfolge (von links nach rechts):</span><span class="sxs-lookup"><span data-stu-id="2fc57-126">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="2fc57-127">Erforderliche Parameter (Parameter, die nicht über das **\[ DefaultValue \]** - **\[** Attribut oder [**optionale**](optional.md) **\]** Attribute verfügen)</span><span class="sxs-lookup"><span data-stu-id="2fc57-127">Required parameters (parameters that do not have the **\[defaultvalue\]** or **\[**[**optional**](optional.md)**\]** attributes),</span></span>
2.  <span data-ttu-id="2fc57-128">optionale Parameter mit oder ohne das **\[ DefaultValue \]** -Attribut</span><span class="sxs-lookup"><span data-stu-id="2fc57-128">optional parameters with or without the **\[defaultvalue\]** attribute,</span></span>
3.  <span data-ttu-id="2fc57-129">Parameter mit dem **\[ optionalen \]** -Attribut und ohne das **\[ DefaultValue \]** -Attribut</span><span class="sxs-lookup"><span data-stu-id="2fc57-129">parameters with the **\[optional\]** attribute and without the **\[defaultvalue\]** attribute,</span></span>
4.  <span data-ttu-id="2fc57-130">**\[**[**LCID**](lcid.md) - **\]** Parameter (falls vorhanden)</span><span class="sxs-lookup"><span data-stu-id="2fc57-130">**\[**[**lcid**](lcid.md)**\]** parameter, if any,</span></span>
5.  <span data-ttu-id="2fc57-131">**\[**[**retval**](retval.md) **\]** Parame</span><span class="sxs-lookup"><span data-stu-id="2fc57-131">**\[**[**retval**](retval.md)**\]** parameter</span></span>

## <a name="examples"></a><span data-ttu-id="2fc57-132">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fc57-132">Examples</span></span>

``` syntax
interface IFace : IUnknown
{
    HRESULT Ex1([defaultvalue(44)] LONG i);
    HRESULT Ex2([defaultvalue(44)] SHORT i);
...
};

interface QueryDef : IUnknown
{
    HRESULT OpenRecordset( [in, defaultvalue(DBOPENTABLE)]
    LONG Type,
    [out,retval] Recordset **pprst);
}
//  Type is now known to be a LONG type (good for browser in VBA and
//  good for a C/C++ programmer) and has a default value of
//  DBOPENTABLE
```

## <a name="see-also"></a><span data-ttu-id="2fc57-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2fc57-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc57-134">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="2fc57-134">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="2fc57-135">Erstellen einer Typbibliothek mit "Mittel l"</span><span class="sxs-lookup"><span data-stu-id="2fc57-135">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="2fc57-136">**berfläche**</span><span class="sxs-lookup"><span data-stu-id="2fc57-136">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="2fc57-137">**LCID**</span><span class="sxs-lookup"><span data-stu-id="2fc57-137">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="2fc57-138">**optionale**</span><span class="sxs-lookup"><span data-stu-id="2fc57-138">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="2fc57-139">Beispiel für eine ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="2fc57-139">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="2fc57-140">Syntax der ODL-Datei</span><span class="sxs-lookup"><span data-stu-id="2fc57-140">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="2fc57-141">**retval**</span><span class="sxs-lookup"><span data-stu-id="2fc57-141">**retval**</span></span>](retval.md)
</dt> <dt>

[<span data-ttu-id="2fc57-142">FUNCFLAGS</span><span class="sxs-lookup"><span data-stu-id="2fc57-142">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 