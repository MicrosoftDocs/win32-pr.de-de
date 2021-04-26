---
description: Gibt einen Vorgang an, für den Code generiert werden soll.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: operation-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c0e4562241f5f437554d0af28dc8bca482512ea
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994316"
---
# <a name="operation-element"></a><span data-ttu-id="f6d21-103">operation-Element</span><span class="sxs-lookup"><span data-stu-id="f6d21-103">operation element</span></span>

<span data-ttu-id="f6d21-104">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6d21-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="f6d21-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="f6d21-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="f6d21-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="f6d21-106">Attributes</span></span>

<span data-ttu-id="f6d21-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="f6d21-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f6d21-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6d21-108">Child elements</span></span>

<span data-ttu-id="f6d21-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="f6d21-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="f6d21-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f6d21-110">Parent elements</span></span>



| <span data-ttu-id="f6d21-111">Element</span><span class="sxs-lookup"><span data-stu-id="f6d21-111">Element</span></span>                                                                                                 | <span data-ttu-id="f6d21-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6d21-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6d21-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="f6d21-114">Generiert Implementierungsdeklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="f6d21-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="f6d21-116">Generiert IDL-Deklarationen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="f6d21-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f6d21-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="f6d21-118">Generiert C-Strukturdefinitionen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="f6d21-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="f6d21-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="f6d21-120">Generiert C-Konstantendeklarationen für XML-Schematabellen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="f6d21-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="f6d21-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f6d21-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="f6d21-122">Generiert C-Konstanten für XML-Schematabellen für Nachrichtentypen.</span><span class="sxs-lookup"><span data-stu-id="f6d21-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="f6d21-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="f6d21-124">Generiert C-Konstantendeklarationen für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="f6d21-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="f6d21-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f6d21-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="f6d21-126">Generiert C-Konstanten für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="f6d21-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="f6d21-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="f6d21-128">Generiert Implementierungen für Proxyfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="f6d21-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="f6d21-130">Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="f6d21-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="f6d21-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="f6d21-132">Generiert Implementierungen für Stubfunktionen für Porttypvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="f6d21-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="f6d21-134">Generiert Implementierungsdeklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="f6d21-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="f6d21-136">Generiert IDL-Deklarationen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="f6d21-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="f6d21-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="f6d21-138">Generiert Implementierungen für Subscribe/Unsubscribe-Proxyfunktionen für Porttypbenachrichtigungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="f6d21-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="f6d21-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f6d21-139">Remarks</span></span>

<span data-ttu-id="f6d21-140">Eine beliebige Anzahl von Vorgängen kann angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f6d21-140">Any number of operations may be specified.</span></span> <span data-ttu-id="f6d21-141">Wenn keine Vorgänge angegeben werden, wird Code für alle Vorgänge in allen relevanten Porttypen generiert.</span><span class="sxs-lookup"><span data-stu-id="f6d21-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="f6d21-142">Durch  die Verwendung des Vorgangselements werden die generierten Methoden auf die im Vorgang enthaltenen Methoden beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f6d21-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="f6d21-143">Beispielsweise unterstützt ein Drucker diese Vorgänge unter anderem:</span><span class="sxs-lookup"><span data-stu-id="f6d21-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="f6d21-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="f6d21-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="f6d21-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="f6d21-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="f6d21-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="f6d21-146">**CancelJob**</span></span>
-   <span data-ttu-id="f6d21-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="f6d21-147">**GetJobElements**</span></span>
-   <span data-ttu-id="f6d21-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="f6d21-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="f6d21-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="f6d21-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="f6d21-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="f6d21-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="f6d21-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="f6d21-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="f6d21-152">Das Codegenerierungsskript verwendet die [**idlFunctionDeclarations-Elemente**](idlfunctiondeclarations.md) wie folgt, um nur die Methoden im Zusammenhang mit den **Vorgängen PrintJobByPost** und **GetJobElements** zu enthalten:</span><span class="sxs-lookup"><span data-stu-id="f6d21-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="f6d21-153">Dadurch werden idl-Funktionsdeklarationen für alle Methoden generiert, die den beiden Vorgängen zugeordnet sind (z. B. **BeginPrintJobByPost,** **EndPrintJobByPost,** **BeginGetJobElements** und **EndGetJobElements).**</span><span class="sxs-lookup"><span data-stu-id="f6d21-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="f6d21-154">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="f6d21-154">Element information</span></span>



| <span data-ttu-id="f6d21-155">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="f6d21-155">Label</span></span> | <span data-ttu-id="f6d21-156">Wert</span><span class="sxs-lookup"><span data-stu-id="f6d21-156">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="f6d21-157">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="f6d21-157">Minimum supported system</span></span><br/> | <span data-ttu-id="f6d21-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6d21-158">Windows Vista</span></span> |
| <span data-ttu-id="f6d21-159">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="f6d21-159">Can be empty</span></span>                        | <span data-ttu-id="f6d21-160">Ja</span><span class="sxs-lookup"><span data-stu-id="f6d21-160">Yes</span></span>           |



 

 




