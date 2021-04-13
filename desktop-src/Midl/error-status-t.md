---
title: error_status_t-Attribut
description: Das Error \_ Status \_ t-Schlüsselwort kennzeichnet einen Typ für ein Objekt, das Informationen zum Kommunikations Status oder zum Fehlerstatus enthält.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312216"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="51ae1-104">Fehler \_ Status- \_ t-Attribut</span><span class="sxs-lookup"><span data-stu-id="51ae1-104">error\_status\_t attribute</span></span>

<span data-ttu-id="51ae1-105">Das **Error \_ Status \_ t** -Schlüsselwort kennzeichnet einen Typ für ein Objekt, das Informationen zum Kommunikations Status oder zum Fehlerstatus enthält.</span><span class="sxs-lookup"><span data-stu-id="51ae1-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="51ae1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51ae1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ae1-107">*ACF-Function-Attribute*</span><span class="sxs-lookup"><span data-stu-id="51ae1-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="51ae1-108">Gibt 0 (null) oder mehr ACF-Funktions Attribute an, z. b. den **\[** [**comm- \_ Status**](comm-status.md) **\]** , den **\[** [**Fehler \_ Status**](fault-status.md) **\]** oder **\[** [**NoCode**](nocode.md) **\]**</span><span class="sxs-lookup"><span data-stu-id="51ae1-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="51ae1-109">Funktions Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51ae1-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="51ae1-110">NULL oder mehr Attribute können auf eine Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ae1-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="51ae1-111">Trennen Sie mehrere Funktions Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="51ae1-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="51ae1-112">*function-name*</span><span class="sxs-lookup"><span data-stu-id="51ae1-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="51ae1-113">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="51ae1-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="51ae1-114">*ACF-Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="51ae1-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="51ae1-115">Gibt Attribute an, die auf einen Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ae1-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="51ae1-116">Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="51ae1-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="51ae1-117">Trennen Sie mehrere Parameter Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="51ae1-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="51ae1-118">Parameter Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="51ae1-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="51ae1-119">IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="51ae1-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="51ae1-120">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="51ae1-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="51ae1-121">Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="51ae1-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="51ae1-122">Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="51ae1-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51ae1-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51ae1-123">Remarks</span></span>

<span data-ttu-id="51ae1-124">Der Typ " **Fehler \_ Status \_ t** " wird als Teil der Ausnahme Behandlungs Architektur in IDL verwendet.</span><span class="sxs-lookup"><span data-stu-id="51ae1-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="51ae1-125">Dieser Typ wird einem [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Long**](long.md)-Typ zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="51ae1-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="51ae1-126">Anwendungen, die Fehlersituationen erfassen, verfügen über einen **\[** [**out**](out-idl.md) - **\]** Parameter oder einen Rückgabetyp einer Prozedur, der als **Fehler \_ Status \_ t** angegeben ist, und qualifizieren den **Fehler \_ Status \_ t** mit den **\[** [**\_ Status**](comm-status.md) Attributen "comm" oder " **\]** **\[** [**Fault \_ Status**](fault-status.md) " **\]** in der ACF.</span><span class="sxs-lookup"><span data-stu-id="51ae1-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="51ae1-127">Wenn der Parameter oder der Rückgabetyp nicht mit den Status Attributen " **\[ comm \_ \]** " oder " **\[ Fault \_ \]** " gekennzeichnet wurde, verhält sich der Parameter so, als ob er "Ganzzahl ohne Vorzeichen long" wäre.</span><span class="sxs-lookup"><span data-stu-id="51ae1-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="51ae1-128">Ab Version 2,0 generiert der-Mittelwert Compiler stubzeichen, die die richtige Fehler Behandlungs Architektur enthalten.</span><span class="sxs-lookup"><span data-stu-id="51ae1-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="51ae1-129">Frühere Versionen des compl-Compilers haben jedoch einen Parameter oder einen Rückgabetyp mit dem **Fehler \_ Status \_ t** behandelt, als ob die Attribute " **\[** [**comm \_ Status**](comm-status.md) " **\]** und " **\[** [**Fehler \_ Status**](fault-status.md) " **\]** angewendet wurden, auch wenn dies nicht der Fall war.</span><span class="sxs-lookup"><span data-stu-id="51ae1-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="51ae1-130">Mit mittlerer l 2,0 oder höher müssen Sie explizit die Attribute " **\[ comm \_ Status \]** " und " **\[ Fehler \_ Status \]** " auf den Parameter oder die Prozedur in der ACF anwenden.</span><span class="sxs-lookup"><span data-stu-id="51ae1-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="51ae1-131">Der Typ " **Fehler \_ Status \_ t** " ist einer der vordefinierten Typen der Schnittstellen Definitions Sprache.</span><span class="sxs-lookup"><span data-stu-id="51ae1-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="51ae1-132">Vordefinierte Typen können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, in allgemeinen Deklarationen und in Funktionsdeklaratoren (entweder als Funktions Rückgabetyp oder als Parametertyp Spezifizierer) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51ae1-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="51ae1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51ae1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ae1-134">**Kommunikations \_ Status**</span><span class="sxs-lookup"><span data-stu-id="51ae1-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="51ae1-135">**Fehler \_ Status**</span><span class="sxs-lookup"><span data-stu-id="51ae1-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="51ae1-136">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="51ae1-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="51ae1-137">**lange**</span><span class="sxs-lookup"><span data-stu-id="51ae1-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="51ae1-138">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="51ae1-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="51ae1-139">**typedef**</span><span class="sxs-lookup"><span data-stu-id="51ae1-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="51ae1-140">**Ganzzahl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="51ae1-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




