---
title: Network Settings-Objekt
description: Gibt für die Skripterstellung die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Network Settings-Objekt Taskplaner
- Network Settings-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477202"
---
# <a name="networksettings-object"></a><span data-ttu-id="eb76b-105">Network Settings-Objekt</span><span class="sxs-lookup"><span data-stu-id="eb76b-105">NetworkSettings object</span></span>

<span data-ttu-id="eb76b-106">Gibt für die Skripterstellung die Einstellungen an, die vom Taskplaner-Dienst zum Abrufen eines Netzwerk Profils verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb76b-106">For scripting, provides the settings that the Task Scheduler service uses to obtain a network profile.</span></span>

## <a name="members"></a><span data-ttu-id="eb76b-107">Member</span><span class="sxs-lookup"><span data-stu-id="eb76b-107">Members</span></span>

<span data-ttu-id="eb76b-108">Das **Network Settings** -Objekt verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eb76b-108">The **NetworkSettings** object has these types of members:</span></span>

-   [<span data-ttu-id="eb76b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb76b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb76b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="eb76b-110">Properties</span></span>

<span data-ttu-id="eb76b-111">Das **Network Settings** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="eb76b-111">The **NetworkSettings** object has these properties.</span></span>



| <span data-ttu-id="eb76b-112">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eb76b-112">Property</span></span>                                        | <span data-ttu-id="eb76b-113">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="eb76b-113">Access type</span></span>           | <span data-ttu-id="eb76b-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb76b-114">Description</span></span>                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb76b-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb76b-115">**Id**</span></span>](networksettings-id.md)<br/>     | <span data-ttu-id="eb76b-116">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb76b-116">Read/write</span></span><br/> | <span data-ttu-id="eb76b-117">Ruft einen GUID-Wert ab, der ein Netzwerk Profil identifiziert, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="eb76b-117">Gets or sets a GUID value that identifies a network profile.</span></span><br/>                        |
| [<span data-ttu-id="eb76b-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="eb76b-118">**Name**</span></span>](networksettings-name.md)<br/> | <span data-ttu-id="eb76b-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="eb76b-119">Read/write</span></span><br/> | <span data-ttu-id="eb76b-120">Ruft den Namen eines Netzwerk Profils ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="eb76b-120">Gets or sets the name of a network profile.</span></span> <span data-ttu-id="eb76b-121">Der Name wird zu Anzeige Zwecken verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb76b-121">The name is used for display purposes.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb76b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb76b-122">Remarks</span></span>

<span data-ttu-id="eb76b-123">Beim Lesen oder schreiben Ihrer eigenen XML-Daten für eine Aufgabe werden Netzwerkeinstellungen mit dem [**networksettings**](taskschedulerschema-networksettings-settingstype-element.md) -Element des Taskplaner-Schemas angegeben.</span><span class="sxs-lookup"><span data-stu-id="eb76b-123">When reading or writing your own XML for a task, network settings are specified using the [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb76b-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eb76b-124">Requirements</span></span>



| <span data-ttu-id="eb76b-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eb76b-125">Requirement</span></span> | <span data-ttu-id="eb76b-126">Wert</span><span class="sxs-lookup"><span data-stu-id="eb76b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb76b-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eb76b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eb76b-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb76b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="eb76b-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eb76b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eb76b-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eb76b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eb76b-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eb76b-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb76b-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb76b-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb76b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eb76b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb76b-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb76b-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb76b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb76b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb76b-136">Taskplaner Objekte</span><span class="sxs-lookup"><span data-stu-id="eb76b-136">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="eb76b-137">Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="eb76b-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





