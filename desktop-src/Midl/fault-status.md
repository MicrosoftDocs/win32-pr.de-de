---
title: fault_status-Attribut
description: Das Attribut \ Fault \_ Status \ ACF gibt an, dass ein Fehlercode des Typs Fehler \_ Status \_ t auf einen Fehler der Remote Prozedur hinweist, nicht auf andere Arten von Problemen, wie z. b. Kommunikationsfehler.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status Attribut-Mittel l
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718077"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="ea437-104">Fault \_ Status-Attribut</span><span class="sxs-lookup"><span data-stu-id="ea437-104">fault\_status attribute</span></span>

<span data-ttu-id="ea437-105">Mit dem ACF-Attribut für den **\[ Fehler \_ Status \]** wird angegeben, dass ein Fehlercode des Typs " [**Fehler \_ Status \_ t**](error-status-t.md) " auf einen Fehler der Remote Prozedur hinweist, nicht auf andere Arten von Problemen wie Kommunikationsfehler.</span><span class="sxs-lookup"><span data-stu-id="ea437-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="ea437-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea437-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea437-107">*ACF-Function-Attribute*</span><span class="sxs-lookup"><span data-stu-id="ea437-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ea437-108">Gibt NULL oder mehr ACF-Funktions Attribute an, wie z. b. **\[ Fehler \_ Status \]** und **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ea437-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="ea437-109">Funktions Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ea437-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ea437-110">Beachten Sie, dass 0 (null) oder mehr Attribute auf eine Funktion angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea437-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="ea437-111">Trennen Sie mehrere Funktions Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ea437-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="ea437-112">Beachten Sie auch Folgendes: Wenn der **\[ Fehler \_ Status \]** als Funktions Attribut angezeigt wird, kann er nicht auch als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ea437-113">*function-name*</span><span class="sxs-lookup"><span data-stu-id="ea437-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ea437-114">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="ea437-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="ea437-115">*ACF-Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="ea437-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="ea437-116">Gibt Attribute an, die auf einen Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="ea437-117">Beachten Sie, dass NULL oder mehr Attribute auf den Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ea437-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="ea437-118">Parameter Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="ea437-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="ea437-119">Trennen Sie mehrere Parameter Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="ea437-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="ea437-120">IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="ea437-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="ea437-121">Beachten Sie Folgendes: Wenn der **\[ Fehler \_ Status \]** als Parameter Attribut angezeigt wird, kann er nicht auch als Funktions Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="ea437-122">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="ea437-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="ea437-123">Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="ea437-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="ea437-124">Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ea437-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea437-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ea437-125">Remarks</span></span>

<span data-ttu-id="ea437-126">Das **\[ Fault \_ Status \]** -Attribut kann entweder als Funktions Attribut oder als Parameter Attribut verwendet werden, es kann jedoch nur einmal pro Funktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="ea437-127">Sie kann entweder auf die Funktion selbst oder auf einen Parameter in jeder Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="ea437-128">Das **\[ Fault \_ Status \]** -Attribut kann nur auf Funktionen angewendet werden, die den [**Typfehler \_ Status \_ t**](error-status-t.md)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ea437-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ea437-129">Wenn die Remote Prozedur auf eine Weise fehlschlägt, die bewirkt, dass ein Fehler-PDU zurückgegeben wird, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea437-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="ea437-130">Wenn der **\[ Fehler \_ \] Status** als Parameter Attribut verwendet wird, muss der Parameter ein **\[** [**out**](out-idl.md) - **\]** Parameter vom Typ " [**Error \_ Status \_ t**](error-status-t.md)" sein.</span><span class="sxs-lookup"><span data-stu-id="ea437-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="ea437-131">Wenn ein Server Fehler auftritt, wird der-Parameter auf den Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ea437-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="ea437-132">Wenn der Remote-Befehl erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="ea437-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="ea437-133">Der Parameter, der dem **\[ Fault \_ Status \]** -Attribut zugeordnet ist, muss nicht in der IDL-Datei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="ea437-134">Wenn der-Parameter nicht angegeben wird, wird ein neuer [**out**](out-idl.md) -Parameter vom Typ [**Fehler \_ Status \_ t**](error-status-t.md) nach dem letzten Parameter generiert, der in der DCE-IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ea437-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="ea437-135">Es ist möglich, dass die Attribute " **\[ Fault \_ Status \]** " und " **\[** [**comm \_ Status**](comm-status.md) " **\]** in einer einzelnen Funktion als Funktions Attribute oder Parameter Attribute angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ea437-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="ea437-136">Wenn beide Attribute Funktions Attribute sind oder wenn Sie auf denselben Parameter angewendet werden und kein Fehler auftritt, hat die Funktion oder der Parameter den Wert **Fehler \_ Status \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea437-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="ea437-137">Andernfalls enthält Sie den entsprechenden Statuscode Wert.</span><span class="sxs-lookup"><span data-stu-id="ea437-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="ea437-138">Da die für den **\[ Fehler \_ Status \]** zurückgegebenen Werte sich von den Werten unterscheiden, die für den Kommunikations **\[ \_ Status \]** zurückgegeben werden, werden die zurückgegebenen Werte leicht interpretiert</span><span class="sxs-lookup"><span data-stu-id="ea437-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea437-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea437-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea437-140">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="ea437-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="ea437-141">**Kommunikations \_ Status**</span><span class="sxs-lookup"><span data-stu-id="ea437-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="ea437-142">**Fehler \_ Status \_ t**</span><span class="sxs-lookup"><span data-stu-id="ea437-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="ea437-143">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="ea437-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="ea437-144">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="ea437-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




