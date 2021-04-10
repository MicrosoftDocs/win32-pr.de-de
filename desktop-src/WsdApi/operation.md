---
description: Gibt einen Vorgang an, für den Code generiert werden soll.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: Operation-Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042050"
---
# <a name="operation-element"></a><span data-ttu-id="2602b-103">Operation-Element</span><span class="sxs-lookup"><span data-stu-id="2602b-103">operation element</span></span>

<span data-ttu-id="2602b-104">Gibt einen Vorgang an, für den Code generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2602b-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="2602b-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="2602b-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="2602b-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="2602b-106">Attributes</span></span>

<span data-ttu-id="2602b-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="2602b-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2602b-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2602b-108">Child elements</span></span>

<span data-ttu-id="2602b-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="2602b-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2602b-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2602b-110">Parent elements</span></span>



| <span data-ttu-id="2602b-111">Element</span><span class="sxs-lookup"><span data-stu-id="2602b-111">Element</span></span>                                                                                                 | <span data-ttu-id="2602b-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2602b-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2602b-113">**functiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="2602b-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="2602b-114">Generiert Implementierungs Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="2602b-115">**idlfunctiondeklarationen**</span><span class="sxs-lookup"><span data-stu-id="2602b-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="2602b-116">Generiert IDL-Deklarationen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="2602b-117">**messagestructuredefinitions**</span><span class="sxs-lookup"><span data-stu-id="2602b-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="2602b-118">Generiert C-Strukturdefinitionen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="2602b-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="2602b-119">**messagetypedeklarationen**</span><span class="sxs-lookup"><span data-stu-id="2602b-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="2602b-120">Generiert C-Konstante Deklarationen für XML-Schema Tabellen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="2602b-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="2602b-121">**messagetypedefinitions**</span><span class="sxs-lookup"><span data-stu-id="2602b-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="2602b-122">Generiert C-Konstanten für XML-Schema Tabellen für Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="2602b-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="2602b-123">**porttypeer-Deklarationen**</span><span class="sxs-lookup"><span data-stu-id="2602b-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="2602b-124">Generiert C-Konstante Deklarationen für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="2602b-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="2602b-125">**porttypeer Definitionen**</span><span class="sxs-lookup"><span data-stu-id="2602b-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="2602b-126">Generiert C-Konstanten für Porttypen.</span><span class="sxs-lookup"><span data-stu-id="2602b-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="2602b-127">**proxyfunctionimplementierungen**</span><span class="sxs-lookup"><span data-stu-id="2602b-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="2602b-128">Generiert Implementierungen für Proxy Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="2602b-129">**stubdeklarationen**</span><span class="sxs-lookup"><span data-stu-id="2602b-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="2602b-130">Generiert Deklarationen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="2602b-131">**stubdefinitionen**</span><span class="sxs-lookup"><span data-stu-id="2602b-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="2602b-132">Generiert Implementierungen für Stub-Funktionen für Porttyp Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="2602b-133">**"abonnemenfunctiondeklarationen"**</span><span class="sxs-lookup"><span data-stu-id="2602b-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="2602b-134">Generiert Implementierungs Deklarationen für Abonnement-/abonnementproxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="2602b-135">**"abonnemenidlfunctiondeklarationen"**</span><span class="sxs-lookup"><span data-stu-id="2602b-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="2602b-136">Generiert IDL-Deklarationen für Abonnement-/abonnementproxyfunktionen für Port-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="2602b-137">**abonnemenproxyfunctionimplementierungen**</span><span class="sxs-lookup"><span data-stu-id="2602b-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="2602b-138">Generiert Implementierungen für Abonnement-/Abonnement-Proxyfunktionen für Porttyp-Benachrichtigungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2602b-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="2602b-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2602b-139">Remarks</span></span>

<span data-ttu-id="2602b-140">Es kann eine beliebige Anzahl von Vorgängen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2602b-140">Any number of operations may be specified.</span></span> <span data-ttu-id="2602b-141">Wenn keine Vorgänge angegeben werden, wird der Code für alle Vorgänge in allen relevanten Porttypen generiert.</span><span class="sxs-lookup"><span data-stu-id="2602b-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="2602b-142">Wenn Sie das **Operation** -Element verwenden, werden die generierten Methoden auf die im-Vorgang enthaltenen Methoden beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2602b-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="2602b-143">Ein Drucker unterstützt z. b. die folgenden Vorgänge:</span><span class="sxs-lookup"><span data-stu-id="2602b-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="2602b-144">**Printjobbypost**</span><span class="sxs-lookup"><span data-stu-id="2602b-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="2602b-145">**Printjobbyreference**</span><span class="sxs-lookup"><span data-stu-id="2602b-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="2602b-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="2602b-146">**CancelJob**</span></span>
-   <span data-ttu-id="2602b-147">**Getjobelements**</span><span class="sxs-lookup"><span data-stu-id="2602b-147">**GetJobElements**</span></span>
-   <span data-ttu-id="2602b-148">**Getactivejobs**</span><span class="sxs-lookup"><span data-stu-id="2602b-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="2602b-149">**Getjobhistory**</span><span class="sxs-lookup"><span data-stu-id="2602b-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="2602b-150">**Abonniert.**</span><span class="sxs-lookup"><span data-stu-id="2602b-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="2602b-151">**Unabonniert betoprinterconfigchange**</span><span class="sxs-lookup"><span data-stu-id="2602b-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="2602b-152">Wenn Sie jedoch nur die Methoden im Zusammenhang mit den **printjobbypost** -und **getjobelements** -Vorgängen einschließen möchten, verwendet das Code Generierungs Skript die [**idlfunctionscripts**](idlfunctiondeclarations.md) -Elemente wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2602b-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="2602b-153">Dadurch werden IDL-Funktions Deklarationen für alle Methoden generiert, die den beiden Vorgängen zugeordnet sind (z. b. **beginprintjobbypost**, **endprintjobbypost**, **begingetjobelements** und **endgetjobelements**).</span><span class="sxs-lookup"><span data-stu-id="2602b-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="2602b-154">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2602b-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="2602b-155">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="2602b-155">Minimum supported system</span></span><br/> | <span data-ttu-id="2602b-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2602b-156">Windows Vista</span></span> |
| <span data-ttu-id="2602b-157">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="2602b-157">Can be empty</span></span>                        | <span data-ttu-id="2602b-158">Ja</span><span class="sxs-lookup"><span data-stu-id="2602b-158">Yes</span></span>           |



 

 




