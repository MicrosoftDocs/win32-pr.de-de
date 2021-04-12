---
title: NoCode-Attribut
description: Das Attribut \ NoCode \ wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Client-Stub-Code zu verhindern.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- NoCode-Attribut (Mittelwert)
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312210"
---
# <a name="nocode-attribute"></a><span data-ttu-id="66941-104">NoCode-Attribut</span><span class="sxs-lookup"><span data-stu-id="66941-104">nocode attribute</span></span>

<span data-ttu-id="66941-105">Das **\[ NoCode \]** -Attribut wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Client-Stub-Code zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="66941-105">The **\[nocode\]** attribute is used in ACF headers or with individual functions to prevent the generation of client stub code.</span></span>

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="66941-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="66941-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66941-107">*ACF-Interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="66941-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-108">Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="66941-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="66941-109">Gültige Attribute sind entweder **\[** [**Automatisches \_ handle**](auto-handle.md) **\]** oder **\[** [**implizites \_ handle**](implicit-handle.md) **\]** und entweder **\[** [**Code**](code.md) **\]** oder **\[ NoCode \]**.</span><span class="sxs-lookup"><span data-stu-id="66941-109">Valid attributes include either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]** and either **\[**[**code**](code.md)**\]** or **\[nocode\]**.</span></span> <span data-ttu-id="66941-110">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="66941-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="66941-111">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="66941-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-112">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="66941-112">Specifies the name of the interface.</span></span> <span data-ttu-id="66941-113">Im DCE-Kompatibilitätsmodus muss der Schnittstellen Name mit dem Namen der Schnittstelle, die in der IDL-Datei angegeben ist, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="66941-113">In DCE-compatibility mode, the interface name must match the name of the interface specified in the IDL file.</span></span> <span data-ttu-id="66941-114">Wenn Sie den-Compilerschalter [**/ACF**](-acf.md)verwenden, können sich der Schnittstellen Name in der ACF und der Schnittstellen Name in der IDL-Datei unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="66941-114">When you use the MIDL compiler switch [**/acf**](-acf.md), the interface name in the ACF and the interface name in the IDL file can be different.</span></span>

</dd> <dt>

<span data-ttu-id="66941-115">*Dateiname-List*</span><span class="sxs-lookup"><span data-stu-id="66941-115">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-116">Gibt eine durch Kommas getrennte Liste mit einem oder mehreren C-sprach Header Dateinamen an.</span><span class="sxs-lookup"><span data-stu-id="66941-116">Specifies a list of one or more C-language header file names, separated by commas.</span></span> <span data-ttu-id="66941-117">Der vollständige Dateiname, einschließlich der Erweiterung, muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="66941-117">The full file name, including the extension, must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="66941-118">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="66941-118">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-119">Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den angegebenen Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="66941-119">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="66941-120">Gültige Typattribute sind " **\[** [**zuordnen**](allocate.md)" **\]** .</span><span class="sxs-lookup"><span data-stu-id="66941-120">Valid type attributes include **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="66941-121">*typeName*</span><span class="sxs-lookup"><span data-stu-id="66941-121">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-122">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="66941-122">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="66941-123">Typattribute in der ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="66941-123">Type attributes in the ACF can only be applied to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="66941-124">*ACF-Function-Attribute*</span><span class="sxs-lookup"><span data-stu-id="66941-124">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-125">Gibt Attribute an, die auf die Funktion als Ganzes angewendet werden, z. b. den **\[** [**comm- \_ Status**](comm-status.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="66941-125">Specifies attributes that apply to the function as a whole, such as **\[**[**comm\_status**](comm-status.md)**\]**.</span></span> <span data-ttu-id="66941-126">Funktions Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="66941-126">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="66941-127">Trennen Sie mehrere Funktions Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="66941-127">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="66941-128">*function-name*</span><span class="sxs-lookup"><span data-stu-id="66941-128">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-129">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="66941-129">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="66941-130">*ACF-Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="66941-130">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-131">Gibt ACF-Attribute an, die auf einen Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="66941-131">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="66941-132">Beachten Sie, dass NULL oder mehr Attribute auf den Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="66941-132">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="66941-133">Trennen Sie mehrere Parameter Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="66941-133">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="66941-134">ACF-Parameter Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="66941-134">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="66941-135">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="66941-135">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66941-136">Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="66941-136">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="66941-137">Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden und denselben Namen verwenden, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="66941-137">Each parameter for the function must be specified in the same sequence and using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66941-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66941-138">Remarks</span></span>

<span data-ttu-id="66941-139">Das **\[ NoCode \]** -Attribut kann im ACF-Header oder auf eine einzelne Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="66941-139">The **\[nocode\]** attribute can appear in the ACF header, or it can be applied to an individual function.</span></span>

<span data-ttu-id="66941-140">Wenn das **\[ NoCode \]** -Attribut im ACF-Header angezeigt wird, wird der Client-Stub-Code für keine Remote Funktion generiert, es sei denn, er verfügt über das **\[** [**Code**](code.md) **\]** Funktions Attribut.</span><span class="sxs-lookup"><span data-stu-id="66941-140">When the **\[nocode\]** attribute appears in the ACF header, client stub code is not generated for any remote function unless it has the **\[**[**code**](code.md)**\]** function attribute.</span></span> <span data-ttu-id="66941-141">Sie können das **\[ NoCode \]** -Attribut im-Header für eine einzelne Funktion überschreiben, indem Sie das **\[ Code \]** -Attribut als Funktions Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="66941-141">You can override the **\[nocode\]** attribute in the header for an individual function by specifying the **\[code\]** attribute as a function attribute.</span></span>

<span data-ttu-id="66941-142">Wenn das **\[ NoCode \]** -Attribut in der Attribut Liste der Funktion angezeigt wird, wird kein Client-Stub-Code für die Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="66941-142">When the **\[nocode\]** attribute appears in the function's attribute list, no client stub code is generated for the function.</span></span>

<span data-ttu-id="66941-143">Client-Stub-Code wird nicht generiert, wenn:</span><span class="sxs-lookup"><span data-stu-id="66941-143">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="66941-144">Der ACF-Header enthält das **\[ NoCode \]** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="66941-144">The ACF header includes the **\[nocode\]** attribute.</span></span>
-   <span data-ttu-id="66941-145">Das **\[ NoCode \]** -Attribut wird auf die-Funktion angewendet.</span><span class="sxs-lookup"><span data-stu-id="66941-145">The **\[nocode\]** attribute is applied to the function.</span></span>
-   <span data-ttu-id="66941-146">Das **\[** [**lokale**](local.md) **\]** Attribut gilt für die Funktion in der Schnittstellen Datei.</span><span class="sxs-lookup"><span data-stu-id="66941-146">The **\[**[**local**](local.md)**\]** attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="66941-147">Entweder **\[** [](code.md) **\]** kann Code oder **\[ NoCode \]** in der Attribut Liste einer Funktion angezeigt werden, und der von Ihnen gewählte Wert kann genau einmal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="66941-147">Either **\[**[**code**](code.md)**\]** or **\[nocode\]** can appear in a function's attribute list, and the one you choose can appear exactly once.</span></span>

<span data-ttu-id="66941-148">Das **\[ NoCode \]** -Attribut wird ignoriert, wenn serverstubobjekte generiert werden.</span><span class="sxs-lookup"><span data-stu-id="66941-148">The **\[nocode\]** attribute is ignored when server stubs are generated.</span></span> <span data-ttu-id="66941-149">Sie können Sie nicht anwenden, wenn Sie serverstubdaten im DCE-Kompatibilitätsmodus erstellen.</span><span class="sxs-lookup"><span data-stu-id="66941-149">You cannot apply it when generating server stubs in DCE-compatibility mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="66941-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66941-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66941-151">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="66941-151">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="66941-152">**/acf**</span><span class="sxs-lookup"><span data-stu-id="66941-152">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="66941-153">**allocate**</span><span class="sxs-lookup"><span data-stu-id="66941-153">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="66941-154">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="66941-154">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="66941-155">**Ordnung**</span><span class="sxs-lookup"><span data-stu-id="66941-155">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="66941-156">**Kommunikations \_ Status**</span><span class="sxs-lookup"><span data-stu-id="66941-156">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="66941-157">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="66941-157">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> </dl>

 

 




