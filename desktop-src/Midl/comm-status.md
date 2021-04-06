---
title: comm_status-Attribut
description: Das Attribut \ comm \_ Status \ ACF bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status Attribut-Mittel l
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718779"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="fd900-104">comm- \_ Status Attribut</span><span class="sxs-lookup"><span data-stu-id="fd900-104">comm\_status attribute</span></span>

<span data-ttu-id="fd900-105">Das **\[ \_ Status \]** -ACF-Attribut von comm bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="fd900-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="fd900-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd900-107">*ACF-Function-Attribute*</span><span class="sxs-lookup"><span data-stu-id="fd900-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="fd900-108">Gibt NULL oder mehr ACF-Funktions Attribute an, wie z. b. den **\[ comm- \_ Status \]** und **\[** [**NoCode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="fd900-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="fd900-109">Funktions Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fd900-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="fd900-110">NULL oder mehr Attribute können auf eine Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="fd900-111">Trennen Sie mehrere Funktions Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="fd900-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="fd900-112">Beachten Sie Folgendes: Wenn der Kommunikations **\[ \_ Status \]** als Funktions Attribut angezeigt wird, kann er nicht auch als Parameter Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fd900-113">*function-name*</span><span class="sxs-lookup"><span data-stu-id="fd900-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd900-114">Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="fd900-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="fd900-115">*ACF-Parameter-Attribute*</span><span class="sxs-lookup"><span data-stu-id="fd900-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="fd900-116">Gibt Attribute an, die auf einen Parameter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="fd900-117">Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fd900-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="fd900-118">Trennen Sie mehrere Parameter Attribute durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="fd900-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="fd900-119">Parameter Attribute werden in eckige Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fd900-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="fd900-120">IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="fd900-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="fd900-121">Beachten Sie Folgendes: Wenn der Kommunikations **\[ \_ Status \]** als Parameter Attribut angezeigt wird, kann er nicht auch als Funktions Attribut angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fd900-122">*Parameter Name*</span><span class="sxs-lookup"><span data-stu-id="fd900-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fd900-123">Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="fd900-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="fd900-124">Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fd900-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd900-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd900-125">Remarks</span></span>

<span data-ttu-id="fd900-126">Das **\[ comm \_ - \] Status** Attribut kann entweder als Funktions Attribut oder als Parameter Attribut verwendet werden, es kann jedoch nur einmal pro Funktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="fd900-127">Sie kann entweder auf die Funktion oder auf einen Parameter in jeder Funktion angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="fd900-128">Das **\[ comm \_ - \] Status** Attribut kann nur auf Funktionen angewendet werden, die den [**Typfehler \_ Status \_ t**](error-status-t.md)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fd900-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="fd900-129">Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fd900-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="fd900-130">Wenn der **\[ \_ Status \] "comm** " als Parameter Attribut verwendet wird, muss der Parameter in der IDL-Datei definiert werden, und er muss ein **\[** [**out**](out-idl.md) - **\]** Parameter vom Typ " [**Error \_ Status \_ t**](error-status-t.md)" sein.</span><span class="sxs-lookup"><span data-stu-id="fd900-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="fd900-131">Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird der-Parameter auf den Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd900-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="fd900-132">Wenn der Remote-Befehl erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.</span><span class="sxs-lookup"><span data-stu-id="fd900-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="fd900-133">Die Attribute " **\[ comm \_ \] Status** " und " **\[** [**Fehler \_ Status**](fault-status.md) " können **\]** in einer einzelnen Funktion, entweder als Funktions Attribute oder Parameter Attribute, angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fd900-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="fd900-134">Wenn beide Attribute Funktions Attribute sind oder wenn Sie auf denselben Parameter angewendet werden und kein Fehler auftritt, hat die Funktion oder der Parameter den Wert **Fehler \_ Status \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd900-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="fd900-135">Andernfalls enthält Sie den entsprechenden Statuswert für den **\[ comm \_ \]** -oder **\[ Fehler \_ Status \]** .</span><span class="sxs-lookup"><span data-stu-id="fd900-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="fd900-136">Da die für den Kommunikations **\[ \_ Status \]** zurückgegebenen Werte sich von den für den **\[ Fehler \_ \] Status** zurückgegebenen Werten unterscheiden, werden die zurückgegebenen Werte leicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="fd900-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd900-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd900-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd900-138">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="fd900-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="fd900-139">**Fehler \_ Status \_ t**</span><span class="sxs-lookup"><span data-stu-id="fd900-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="fd900-140">**Fehler \_ Status**</span><span class="sxs-lookup"><span data-stu-id="fd900-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="fd900-141">**NoCode**</span><span class="sxs-lookup"><span data-stu-id="fd900-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="fd900-142">**vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="fd900-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




