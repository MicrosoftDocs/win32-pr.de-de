---
title: Code-Attribut
description: Das Attribut \ Code \ ACF bewirkt, dass Client-Stub-Code für Remote Funktionen generiert wird.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- Code Attribute-Mittell
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313031"
---
# <a name="code-attribute"></a><span data-ttu-id="82a42-104">Code-Attribut</span><span class="sxs-lookup"><span data-stu-id="82a42-104">code attribute</span></span>

<span data-ttu-id="82a42-105">Das ACF- **\[ Code \]** Attribut bewirkt, dass Client-Stub-Code für Remote Funktionen generiert wird.</span><span class="sxs-lookup"><span data-stu-id="82a42-105">The **\[code\]** ACF attribute causes client stub code to be generated for remote functions.</span></span>

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a><span data-ttu-id="82a42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="82a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82a42-107">*ACF-Interface-Attribute*</span><span class="sxs-lookup"><span data-stu-id="82a42-107">*ACF-interface-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-108">Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-108">Specifies a list of one or more attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="82a42-109">Gültige Attribute sind entweder [**\[ Automatisches \_ handle \]**](auto-handle.md) oder [**\[ implizites \_ handle \]**](implicit-handle.md) und entweder **\[ \] Code**, [**\[ NoCode \]**](nocode.md)oder [**\[ optimieren \]**](optimize.md).</span><span class="sxs-lookup"><span data-stu-id="82a42-109">Valid attributes include either [**\[auto\_handle\]**](auto-handle.md) or [**\[implicit\_handle\]**](implicit-handle.md) and either **\[code\]**, [**\[nocode\]**](nocode.md), or [**\[optimize\]**](optimize.md).</span></span> <span data-ttu-id="82a42-110">Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-110">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-111">*Schnittstellen Name*</span><span class="sxs-lookup"><span data-stu-id="82a42-111">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-112">Gibt den Namen der Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="82a42-112">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-113">*Dateiname-List*</span><span class="sxs-lookup"><span data-stu-id="82a42-113">*filename-list*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-114">Gibt eine Liste mit einem oder mehreren C-Header Dateinamen an, getrennt durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="82a42-114">Specifies a list of one or more C-header file names, separated by commas.</span></span> <span data-ttu-id="82a42-115">Sie müssen den vollständigen Dateinamen angeben, einschließlich der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="82a42-115">You must supply the full file name, including the extension.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-116">*Type-Attribute-List*</span><span class="sxs-lookup"><span data-stu-id="82a42-116">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-117">Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den angegebenen Typ angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-117">Specifies a list of one or more attributes, separated by commas, that apply to the specified type.</span></span> <span data-ttu-id="82a42-118">Gültige Typattribute sind " [**\[ \] zuordnen**](allocate.md) " und " [**\[ darstellen \_ als \]**](represent-as.md)".</span><span class="sxs-lookup"><span data-stu-id="82a42-118">Valid type attributes include [**\[allocate\]**](allocate.md) and [**\[represent\_as\]**](represent-as.md).</span></span>

</dd> <dt>

<span data-ttu-id="82a42-119">*typeName*</span><span class="sxs-lookup"><span data-stu-id="82a42-119">*typename*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-120">Gibt einen Typ an, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="82a42-120">Specifies a type defined in the IDL file.</span></span> <span data-ttu-id="82a42-121">Typattribute in der ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="82a42-121">Type attributes in the ACF can be applied only to types previously defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-122">*ACF-Function-Attribute*</span><span class="sxs-lookup"><span data-stu-id="82a42-122">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-123">Gibt 0 (null) oder mehr Attribute an, die für die Funktion als Ganzes gelten, z. b. den [**\[ comm- \_ Status \]**](comm-status.md).</span><span class="sxs-lookup"><span data-stu-id="82a42-123">Specifies zero or more attributes that apply to the function as a whole, such as [**\[comm\_status\]**](comm-status.md).</span></span> <span data-ttu-id="82a42-124">Funktions Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="82a42-124">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="82a42-125">Trennen Sie mehrere Funktions Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="82a42-125">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-126">*function-name*</span><span class="sxs-lookup"><span data-stu-id="82a42-126">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-127">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="82a42-127">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-128">*ACF-Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="82a42-128">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-129">Gibt ACF-Attribute an, die auf einen Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-129">Specifies ACF attributes that apply to a parameter.</span></span> <span data-ttu-id="82a42-130">Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="82a42-130">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="82a42-131">Trennen Sie mehrere Parameter Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="82a42-131">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="82a42-132">ACF-Parameter Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="82a42-132">ACF parameter attributes are enclosed in square brackets.</span></span>

</dd> <dt>

<span data-ttu-id="82a42-133">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="82a42-133">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="82a42-134">Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="82a42-134">Specifies a parameter of the function as defined in the IDL file.</span></span> <span data-ttu-id="82a42-135">Jeder Parameter für die Funktion muss in derselben Reihenfolge und mit dem gleichen Namen wie in der IDL-Datei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-135">Each parameter for the function must be specified in the same sequence and with the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82a42-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82a42-136">Remarks</span></span>

<span data-ttu-id="82a42-137">Das **\[ Code \]** -Attribut kann im ACF-Header oder auf eine einzelne Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-137">The **\[code\]** attribute can appear in the ACF header or be applied to an individual function.</span></span>

<span data-ttu-id="82a42-138">Wenn das **\[ Code \]** -Attribut im ACF-Header angezeigt wird, wird Client-Stub-Code für alle Remote Funktionen generiert, die nicht über das [**\[ NoCode \]**](nocode.md) -Funktions Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="82a42-138">When the **\[code\]** attribute appears in the ACF header, client stub code is generated for all remote functions that do not have the [**\[nocode\]**](nocode.md) function attribute.</span></span> <span data-ttu-id="82a42-139">Sie können das **\[ Code \]** -Attribut im-Header für eine einzelne Funktion überschreiben, indem Sie das **\[ NoCode \]** -Attribut als Funktions Attribut angeben.</span><span class="sxs-lookup"><span data-stu-id="82a42-139">You can override the **\[code\]** attribute in the header for an individual function by specifying the **\[nocode\]** attribute as a function attribute.</span></span>

<span data-ttu-id="82a42-140">Wenn das **\[ Code \]** -Attribut in der Attribut Liste der Remote Funktion angezeigt wird, wird der Client-Stub-Code für die Funktion generiert.</span><span class="sxs-lookup"><span data-stu-id="82a42-140">When the **\[code\]** attribute appears in the remote function's attribute list, client stub code is generated for the function.</span></span> <span data-ttu-id="82a42-141">Client-Stub-Code wird nicht generiert, wenn:</span><span class="sxs-lookup"><span data-stu-id="82a42-141">Client stub code is not generated when:</span></span>

-   <span data-ttu-id="82a42-142">Der ACF-Header enthält das [**\[ NoCode \]**](nocode.md) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="82a42-142">The ACF header includes the [**\[nocode\]**](nocode.md) attribute.</span></span>
-   <span data-ttu-id="82a42-143">Das [**\[ NoCode \]**](nocode.md) -Attribut wird auf die-Funktion angewendet.</span><span class="sxs-lookup"><span data-stu-id="82a42-143">The [**\[nocode\]**](nocode.md) attribute is applied to the function.</span></span>
-   <span data-ttu-id="82a42-144">Das [**\[ lokale \]**](local.md) Attribut gilt für die Funktion in der Schnittstellen Datei.</span><span class="sxs-lookup"><span data-stu-id="82a42-144">The [**\[local\]**](local.md) attribute applies to the function in the interface file.</span></span>

<span data-ttu-id="82a42-145">Entweder kann **\[ Code \]** oder [**\[ NoCode \]**](nocode.md) in der Liste der Schnittstellen-oder Funktions Attribute angezeigt werden, aber der von Ihnen gewählte kann nur ein Mal in der Liste angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="82a42-145">Either **\[code\]** or [**\[nocode\]**](nocode.md) can appear in the interface or function attribute list, but the one you choose can appear only once in the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="82a42-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82a42-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82a42-147">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="82a42-147">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="82a42-148">**allocate**</span><span class="sxs-lookup"><span data-stu-id="82a42-148">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="82a42-149">**Automatisches \_ handle**</span><span class="sxs-lookup"><span data-stu-id="82a42-149">**auto\_handle**</span></span>](auto-handle.md)
</dt> <dt>

[<span data-ttu-id="82a42-150">**Kommunikations \_ Status**</span><span class="sxs-lookup"><span data-stu-id="82a42-150">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="82a42-151">**implizites \_ handle**</span><span class="sxs-lookup"><span data-stu-id="82a42-151">**implicit\_handle**</span></span>](implicit-handle.md)
</dt> <dt>

[<span data-ttu-id="82a42-152">**nah**</span><span class="sxs-lookup"><span data-stu-id="82a42-152">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="82a42-153">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="82a42-153">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="82a42-154">**optimiert**</span><span class="sxs-lookup"><span data-stu-id="82a42-154">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="82a42-155">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="82a42-155">**represent\_as**</span></span>](represent-as.md)
</dt> </dl>

 

 




