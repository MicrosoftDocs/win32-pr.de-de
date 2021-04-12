---
description: Beschreibt die Dokument Konventionen zum Lesen von WMI-Skript-API-Themen.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Dokument Konventionen für die Skript-API
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346739"
---
# <a name="document-conventions-for-the-scripting-api"></a><span data-ttu-id="cf89a-103">Dokument Konventionen für die Skript-API</span><span class="sxs-lookup"><span data-stu-id="cf89a-103">Document Conventions for the Scripting API</span></span>

<span data-ttu-id="cf89a-104">Die [Skript-API für die WMI](scripting-api-for-wmi.md) -Referenz verwendet die folgenden Dokument Konventionen:</span><span class="sxs-lookup"><span data-stu-id="cf89a-104">The [Scripting API for WMI](scripting-api-for-wmi.md) reference uses the following document conventions:</span></span>

-   <span data-ttu-id="cf89a-105">Parameter Typen werden mit einem Präfix definiert: b (Boolean), Str (String), I (Integer), obj (Automation-Objekt), var (Variant).</span><span class="sxs-lookup"><span data-stu-id="cf89a-105">Parameter types are defined using a prefix: b (Boolean), str (string), I (integer), obj (Automation object), var (Variant).</span></span>
-   <span data-ttu-id="cf89a-106">Optionale Parameter werden in eckigen Klammern mit ihren Standardwerten platziert, die durch die Zuweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cf89a-106">Optional parameters are placed in square brackets with their default values shown by assignment.</span></span>
-   <span data-ttu-id="cf89a-107">Im Fall von Objekt Parametern geben die Zeichen nach dem Präfix "obj" den Objekttyp an, der erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="cf89a-107">In the case of object parameters, the characters after the "obj" prefix indicate the type of object expected.</span></span>



| <span data-ttu-id="cf89a-108">Object-Parameter</span><span class="sxs-lookup"><span data-stu-id="cf89a-108">Object parameter</span></span>      | <span data-ttu-id="cf89a-109">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="cf89a-109">Object type</span></span>                                          |
|-----------------------|------------------------------------------------------|
| <span data-ttu-id="cf89a-110">*Wbemdatetime*</span><span class="sxs-lookup"><span data-stu-id="cf89a-110">*WbemDatetime*</span></span>        | [<span data-ttu-id="cf89a-111">**Swap-DateTime**</span><span class="sxs-lookup"><span data-stu-id="cf89a-111">**SWbemDateTime**</span></span>](swbemdatetime.md)               |
| <span data-ttu-id="cf89a-112">*Wbemeventsource*</span><span class="sxs-lookup"><span data-stu-id="cf89a-112">*WbemEventSource*</span></span>     | [<span data-ttu-id="cf89a-113">**"Errbemeventsource"**</span><span class="sxs-lookup"><span data-stu-id="cf89a-113">**SWbemEventSource**</span></span>](swbemeventsource.md)         |
| <span data-ttu-id="cf89a-114">*Wbemlocator*</span><span class="sxs-lookup"><span data-stu-id="cf89a-114">*WbemLocator*</span></span>         | [<span data-ttu-id="cf89a-115">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="cf89a-115">**SWbemLocator**</span></span>](swbemlocator.md)                 |
| <span data-ttu-id="cf89a-116">*Wbemmethod*</span><span class="sxs-lookup"><span data-stu-id="cf89a-116">*WbemMethod*</span></span>          | [<span data-ttu-id="cf89a-117">**Swap-Methode**</span><span class="sxs-lookup"><span data-stu-id="cf89a-117">**SWbemMethod**</span></span>](swbemmethod.md)                   |
| <span data-ttu-id="cf89a-118">*Wbemmethodset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-118">*WbemMethodSet*</span></span>       | [<span data-ttu-id="cf89a-119">**Swap-methodset**</span><span class="sxs-lookup"><span data-stu-id="cf89a-119">**SWbemMethodSet**</span></span>](swbemmethodset.md)             |
| <span data-ttu-id="cf89a-120">*Wbemnamedvalueset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-120">*WbemNamedValueSet*</span></span>   | [<span data-ttu-id="cf89a-121">**Austausch Elementname**</span><span class="sxs-lookup"><span data-stu-id="cf89a-121">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)     |
| <span data-ttu-id="cf89a-122">*Wbemubjekt*</span><span class="sxs-lookup"><span data-stu-id="cf89a-122">*WbemObject*</span></span>          | [<span data-ttu-id="cf89a-123">**Austausch Objekt**</span><span class="sxs-lookup"><span data-stu-id="cf89a-123">**SWbemObject**</span></span>](swbemobject.md)                   |
| <span data-ttu-id="cf89a-124">*Wbemubjectex*</span><span class="sxs-lookup"><span data-stu-id="cf89a-124">*WbemObjectEx*</span></span>        | [<span data-ttu-id="cf89a-125">**Austauschen von "errbemubjectex"**</span><span class="sxs-lookup"><span data-stu-id="cf89a-125">**SWbemObjectEx**</span></span>](swbemobjectex.md)               |
| <span data-ttu-id="cf89a-126">*Wbemubjectpath*</span><span class="sxs-lookup"><span data-stu-id="cf89a-126">*WbemObjectPath*</span></span>      | [<span data-ttu-id="cf89a-127">**Errbemubjectpath**</span><span class="sxs-lookup"><span data-stu-id="cf89a-127">**SWbemObjectPath**</span></span>](swbemobjectpath.md)           |
| <span data-ttu-id="cf89a-128">*Wbemubjectset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-128">*WbemObjectSet*</span></span>       | [<span data-ttu-id="cf89a-129">**Austauschen von "errbemubjectset"**</span><span class="sxs-lookup"><span data-stu-id="cf89a-129">**SWbemObjectSet**</span></span>](swbemobjectset.md)             |
| <span data-ttu-id="cf89a-130">*Wbemprivilege*</span><span class="sxs-lookup"><span data-stu-id="cf89a-130">*WbemPrivilege*</span></span>       | [<span data-ttu-id="cf89a-131">**Austausch Berechtigung**</span><span class="sxs-lookup"><span data-stu-id="cf89a-131">**SWbemPrivilege**</span></span>](swbemprivilege.md)             |
| <span data-ttu-id="cf89a-132">*Wbemprivilegeset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-132">*WbemPrivilegeSet*</span></span>    | [<span data-ttu-id="cf89a-133">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="cf89a-133">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)       |
| <span data-ttu-id="cf89a-134">*Wbemproperty*</span><span class="sxs-lookup"><span data-stu-id="cf89a-134">*WbemProperty*</span></span>        | [<span data-ttu-id="cf89a-135">**Swap Property**</span><span class="sxs-lookup"><span data-stu-id="cf89a-135">**SWbemProperty**</span></span>](swbemproperty.md)               |
| <span data-ttu-id="cf89a-136">*Wbempropertyset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-136">*WbemPropertySet*</span></span>     | [<span data-ttu-id="cf89a-137">**Swap PropertySet**</span><span class="sxs-lookup"><span data-stu-id="cf89a-137">**SWbemPropertySet**</span></span>](swbempropertyset.md)         |
| <span data-ttu-id="cf89a-138">*Wbemqualifizierer*</span><span class="sxs-lookup"><span data-stu-id="cf89a-138">*WbemQualifier*</span></span>       | [<span data-ttu-id="cf89a-139">**Austausch Qualifizierer**</span><span class="sxs-lookup"><span data-stu-id="cf89a-139">**SWbemQualifier**</span></span>](swbemqualifier.md)             |
| <span data-ttu-id="cf89a-140">*Wbemqualifierset*</span><span class="sxs-lookup"><span data-stu-id="cf89a-140">*WbemQualifierSet*</span></span>    | [<span data-ttu-id="cf89a-141">**Swap-qualifierset**</span><span class="sxs-lookup"><span data-stu-id="cf89a-141">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)       |
| <span data-ttu-id="cf89a-142">*Wbemerfrischendes ableitem*</span><span class="sxs-lookup"><span data-stu-id="cf89a-142">*WbemRefreshableItem*</span></span> | [<span data-ttu-id="cf89a-143">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="cf89a-143">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md) |
| <span data-ttu-id="cf89a-144">*Wbemfreshsher*</span><span class="sxs-lookup"><span data-stu-id="cf89a-144">*WbemRefresher*</span></span>       | [<span data-ttu-id="cf89a-145">**Swap-Aktualisierungs Programm**</span><span class="sxs-lookup"><span data-stu-id="cf89a-145">**SWbemRefresher**</span></span>](swbemrefresher.md)             |
| <span data-ttu-id="cf89a-146">*WbemServices*</span><span class="sxs-lookup"><span data-stu-id="cf89a-146">*WbemServices*</span></span>        | [<span data-ttu-id="cf89a-147">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="cf89a-147">**SWbemServices**</span></span>](swbemservices.md)               |
| <span data-ttu-id="cf89a-148">*Wbemservicesex*</span><span class="sxs-lookup"><span data-stu-id="cf89a-148">*WbemServicesEx*</span></span>      | [<span data-ttu-id="cf89a-149">**Swap Service Ex**</span><span class="sxs-lookup"><span data-stu-id="cf89a-149">**SWbemServicesEx**</span></span>](swbemservicesex.md)           |



 

<span data-ttu-id="cf89a-150">Der folgende Code zeigt z. b., wie Sie Variablen für verschiedene Objekttypen benennen:</span><span class="sxs-lookup"><span data-stu-id="cf89a-150">For example, the following code shows how to name variables for different types of objects:</span></span>


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



