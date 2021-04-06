---
title: Principal-Objekt
description: Skript Objekt, das die Sicherheits Anmelde Informationen für einen Prinzipal bereitstellt.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Prinzipal Objekt Taskplaner
- Prinzipal Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858770"
---
# <a name="principal-object"></a><span data-ttu-id="509ea-105">Principal-Objekt</span><span class="sxs-lookup"><span data-stu-id="509ea-105">Principal object</span></span>

<span data-ttu-id="509ea-106">Skript Objekt, das die Sicherheits Anmelde Informationen für einen Prinzipal bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="509ea-106">Scripting object that provides the security credentials for a principal.</span></span> <span data-ttu-id="509ea-107">Diese Sicherheits Anmelde Informationen definieren den Sicherheitskontext für die Tasks, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="509ea-107">These security credentials define the security context for the tasks that are associated with the principal.</span></span>

## <a name="members"></a><span data-ttu-id="509ea-108">Member</span><span class="sxs-lookup"><span data-stu-id="509ea-108">Members</span></span>

<span data-ttu-id="509ea-109">Das **Prinzipal** Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="509ea-109">The **Principal** object has these types of members:</span></span>

-   [<span data-ttu-id="509ea-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="509ea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="509ea-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="509ea-111">Properties</span></span>

<span data-ttu-id="509ea-112">Das **Prinzipal** Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="509ea-112">The **Principal** object has these properties.</span></span>



| <span data-ttu-id="509ea-113">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="509ea-113">Property</span></span>                                                | <span data-ttu-id="509ea-114">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="509ea-114">Access type</span></span>           | <span data-ttu-id="509ea-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="509ea-115">Description</span></span>                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="509ea-116">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="509ea-116">**DisplayName**</span></span>](principal-displayname.md)<br/> | <span data-ttu-id="509ea-117">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-117">Read/write</span></span><br/> | <span data-ttu-id="509ea-118">Ruft den Namen des Prinzipals ab, der in der Taskplaner Benutzeroberfläche angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="509ea-118">Gets or sets the name of the principal that is displayed in the Task Scheduler UI.</span></span><br/>                                                                |
| [<span data-ttu-id="509ea-119">**GroupID**</span><span class="sxs-lookup"><span data-stu-id="509ea-119">**GroupId**</span></span>](principal-groupid.md)<br/>         | <span data-ttu-id="509ea-120">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-120">Read/write</span></span><br/> | <span data-ttu-id="509ea-121">Ruft den Bezeichner der Benutzergruppe ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="509ea-121">Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span><br/>                           |
| [<span data-ttu-id="509ea-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="509ea-122">**Id**</span></span>](principal-id.md)<br/>                   | <span data-ttu-id="509ea-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-123">Read/write</span></span><br/> | <span data-ttu-id="509ea-124">Ruft den Bezeichner des Prinzipals ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="509ea-124">Gets or sets the identifier of the principal.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="509ea-125">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="509ea-125">**LogonType**</span></span>](principal-logontype.md)<br/>     | <span data-ttu-id="509ea-126">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-126">Read/write</span></span><br/> | <span data-ttu-id="509ea-127">Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Tasks erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="509ea-127">Gets or sets the security logon method that is required to run the tasks that are associated with the principal.</span></span><br/>                                  |
| [<span data-ttu-id="509ea-128">**Ausführungs Ebene**</span><span class="sxs-lookup"><span data-stu-id="509ea-128">**RunLevel**</span></span>](principal-runlevel.md)<br/>       | <span data-ttu-id="509ea-129">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-129">Read/write</span></span><br/> | <span data-ttu-id="509ea-130">Ruft den Bezeichner ab oder legt ihn fest, der die Berechtigungsstufe angibt, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="509ea-130">Gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span><br/> |
| [<span data-ttu-id="509ea-131">**UserID**</span><span class="sxs-lookup"><span data-stu-id="509ea-131">**UserId**</span></span>](principal-userid.md)<br/>           | <span data-ttu-id="509ea-132">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="509ea-132">Read/write</span></span><br/> | <span data-ttu-id="509ea-133">Ruft die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.</span><span class="sxs-lookup"><span data-stu-id="509ea-133">Gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="509ea-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="509ea-134">Remarks</span></span>

<span data-ttu-id="509ea-135">Beachten Sie beim Angeben eines Kontos, dass Sie den doppelten umgekehrten Schrägstrich im Code verwenden, um die Domäne und den Benutzernamen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="509ea-135">When specifying an account, remember to properly use the double backslash in code to specify the domain and user name.</span></span> <span data-ttu-id="509ea-136">Verwenden Sie z. b \\ \\ . den Domänen Benutzernamen, um einen Wert für die [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) -Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="509ea-136">For example, use DOMAIN\\\\UserName to specify a value for the [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) property.</span></span>

<span data-ttu-id="509ea-137">Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Sicherheits Anmelde Informationen für einen Prinzipal im [**Principal**](taskschedulerschema-principal-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="509ea-137">When reading or writing XML for a task, the security credentials for a principal are specified in the [**Principal**](taskschedulerschema-principal-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="509ea-138">Wenn eine Aufgabe mit dem at.exe-Befehlszeilen Tool registriert wird und dieses Objekt zum Abrufen von Informationen über den Task verwendet wird, gibt die [**logontype**](principal-logontype.md) -Eigenschaft den Wert 0 zurück, die [**Runlevel**](principal-runlevel.md) -Eigenschaft gibt 0 zurück, und die [**UserID**](principal-userid.md) -Eigenschaft gibt nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="509ea-138">If a task is registered using the at.exe command line tool, and this object is used to retrieve information about the task, then the [**LogonType**](principal-logontype.md) property will return 0, the [**RunLevel**](principal-runlevel.md) property will return 0, and the [**UserId**](principal-userid.md) property will return Nothing.</span></span>

## <a name="examples"></a><span data-ttu-id="509ea-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="509ea-139">Examples</span></span>

<span data-ttu-id="509ea-140">Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="509ea-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="509ea-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="509ea-141">Requirements</span></span>



| <span data-ttu-id="509ea-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="509ea-142">Requirement</span></span> | <span data-ttu-id="509ea-143">Wert</span><span class="sxs-lookup"><span data-stu-id="509ea-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="509ea-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="509ea-144">Minimum supported client</span></span><br/> | <span data-ttu-id="509ea-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="509ea-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="509ea-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="509ea-146">Minimum supported server</span></span><br/> | <span data-ttu-id="509ea-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="509ea-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="509ea-148">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="509ea-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="509ea-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="509ea-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="509ea-150">DLL</span><span class="sxs-lookup"><span data-stu-id="509ea-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="509ea-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="509ea-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





