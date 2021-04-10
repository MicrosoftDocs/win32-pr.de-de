---
title: RegistrationInfo-Objekt
description: Skript Objekt, das die administrativen Informationen bereitstellt, die zum Beschreiben der Aufgabe verwendet werden können.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- Registrierungsinformationen Taskplaner, Objekt
- RegistrationInfo-Objekt Taskplaner
- RegistrationInfo-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b7eb50da6b69622f6101fdbae4ad098d88f0366
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040338"
---
# <a name="registrationinfo-object"></a><span data-ttu-id="15c3c-106">RegistrationInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="15c3c-106">RegistrationInfo object</span></span>

<span data-ttu-id="15c3c-107">Skript Objekt, das die administrativen Informationen bereitstellt, die zum Beschreiben der Aufgabe verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="15c3c-107">Scripting object that provides the administrative information that can be used to describe the task.</span></span> <span data-ttu-id="15c3c-108">Diese Informationen umfassen Details wie z. b. eine Beschreibung der Aufgabe, den Autor der Aufgabe, das Datum, an dem der Task registriert ist, und die Sicherheits Beschreibung des Tasks.</span><span class="sxs-lookup"><span data-stu-id="15c3c-108">This information includes details such as a description of the task, the author of the task, the date the task is registered, and the security descriptor of the task.</span></span>

## <a name="members"></a><span data-ttu-id="15c3c-109">Member</span><span class="sxs-lookup"><span data-stu-id="15c3c-109">Members</span></span>

<span data-ttu-id="15c3c-110">Das **RegistrationInfo** -Objekt verfügt über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="15c3c-110">The **RegistrationInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="15c3c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15c3c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15c3c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="15c3c-112">Properties</span></span>

<span data-ttu-id="15c3c-113">Das **RegistrationInfo** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="15c3c-113">The **RegistrationInfo** object has these properties.</span></span>



| <span data-ttu-id="15c3c-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="15c3c-114">Property</span></span>                                                                     | <span data-ttu-id="15c3c-115">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="15c3c-115">Access type</span></span>           | <span data-ttu-id="15c3c-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15c3c-116">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c3c-117">**Autor**</span><span class="sxs-lookup"><span data-stu-id="15c3c-117">**Author**</span></span>](registrationinfo-author.md)<br/>                         | <span data-ttu-id="15c3c-118">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-118">Read/write</span></span><br/> | <span data-ttu-id="15c3c-119">Ruft den Autor der Aufgabe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-119">Gets or sets the author of the task.</span></span><br/>                                                                                            |
| [<span data-ttu-id="15c3c-120">**Datum**</span><span class="sxs-lookup"><span data-stu-id="15c3c-120">**Date**</span></span>](registrationinfo-date.md)<br/>                             | <span data-ttu-id="15c3c-121">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-121">Read/write</span></span><br/> | <span data-ttu-id="15c3c-122">Ruft das Datum und die Uhrzeit der Registrierung der Aufgabe ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-122">Gets or sets the date and time when the task is registered.</span></span><br/>                                                                     |
| [<span data-ttu-id="15c3c-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="15c3c-123">**Description**</span></span>](registrationinfo-description.md)<br/>               | <span data-ttu-id="15c3c-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-124">Read/write</span></span><br/> | <span data-ttu-id="15c3c-125">Ruft die Beschreibung der Aufgabe ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-125">Gets or sets the description of the task.</span></span><br/>                                                                                       |
| [<span data-ttu-id="15c3c-126">**Dokumentation**</span><span class="sxs-lookup"><span data-stu-id="15c3c-126">**Documentation**</span></span>](registrationinfo-documentation.md)<br/>           | <span data-ttu-id="15c3c-127">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-127">Read/write</span></span><br/> | <span data-ttu-id="15c3c-128">Ruft eine zusätzliche Dokumentation für den Task ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-128">Gets or sets any additional documentation for the task.</span></span><br/>                                                                         |
| [<span data-ttu-id="15c3c-129">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="15c3c-129">**SecurityDescriptor**</span></span>](registrationinfo-securitydescriptor.md)<br/> |                       | <span data-ttu-id="15c3c-130">Ruft die Sicherheits Beschreibung der Aufgabe ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-130">Gets or sets the security descriptor of the task.</span></span><br/>                                                                               |
| [<span data-ttu-id="15c3c-131">**`Source`**</span><span class="sxs-lookup"><span data-stu-id="15c3c-131">**Source**</span></span>](registrationinfo-source.md)<br/>                         | <span data-ttu-id="15c3c-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-132">Read/write</span></span><br/> | <span data-ttu-id="15c3c-133">Ruft ab oder legt fest, wo die Aufgabe aus stammt.</span><span class="sxs-lookup"><span data-stu-id="15c3c-133">Gets or sets where the task originated from.</span></span> <span data-ttu-id="15c3c-134">Beispielsweise kann eine Aufgabe aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer stammen.</span><span class="sxs-lookup"><span data-stu-id="15c3c-134">For example, a task may originate from a component, service, application, or user.</span></span><br/> |
| [<span data-ttu-id="15c3c-135">**RT**</span><span class="sxs-lookup"><span data-stu-id="15c3c-135">**URI**</span></span>](registrationinfo-uri.md)<br/>                               | <span data-ttu-id="15c3c-136">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-136">Read/write</span></span><br/> | <span data-ttu-id="15c3c-137">Ruft den URI der Aufgabe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-137">Gets or sets the URI of the task.</span></span><br/>                                                                                               |
| [<span data-ttu-id="15c3c-138">**Version**</span><span class="sxs-lookup"><span data-stu-id="15c3c-138">**Version**</span></span>](registrationinfo-version.md)<br/>                       | <span data-ttu-id="15c3c-139">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-139">Read/write</span></span><br/> | <span data-ttu-id="15c3c-140">Ruft die Versionsnummer der Aufgabe ab oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-140">Gets or sets the version number of the task.</span></span><br/>                                                                                    |
| [<span data-ttu-id="15c3c-141">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="15c3c-141">**XmlText**</span></span>](registrationinfo-xmltext.md)<br/>                       | <span data-ttu-id="15c3c-142">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="15c3c-142">Read/write</span></span><br/> | <span data-ttu-id="15c3c-143">Ruft eine XML-formatierte Version der Registrierungsinformationen für den Task ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="15c3c-143">Gets or sets an XML-formatted version of the registration information for the task.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="15c3c-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15c3c-144">Remarks</span></span>

<span data-ttu-id="15c3c-145">Registrierungsinformationen können verwendet werden, um eine Aufgabe über die Taskplaner-Benutzeroberfläche oder als Suchkriterium zu identifizieren, wenn die registrierten Tasks aufgezählt werden.</span><span class="sxs-lookup"><span data-stu-id="15c3c-145">Registration information can be used to identify a task through the Task Scheduler UI, or as search criteria when enumerating over the registered tasks.</span></span>

<span data-ttu-id="15c3c-146">Beim Lesen oder Schreiben von XML für eine Aufgabe werden Registrierungsinformationen für die Aufgabe im [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) -Element des Taskplaner Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="15c3c-146">When reading or writing XML for a task, registration information for the task is specified in the [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="15c3c-147">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15c3c-147">Examples</span></span>

<span data-ttu-id="15c3c-148">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="15c3c-148">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15c3c-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15c3c-149">Requirements</span></span>



| <span data-ttu-id="15c3c-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15c3c-150">Requirement</span></span> | <span data-ttu-id="15c3c-151">Wert</span><span class="sxs-lookup"><span data-stu-id="15c3c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c3c-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15c3c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="15c3c-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c3c-153">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15c3c-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15c3c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="15c3c-155">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c3c-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="15c3c-156">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="15c3c-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="15c3c-157"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15c3c-157"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15c3c-158">DLL</span><span class="sxs-lookup"><span data-stu-id="15c3c-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15c3c-159"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c3c-159"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





