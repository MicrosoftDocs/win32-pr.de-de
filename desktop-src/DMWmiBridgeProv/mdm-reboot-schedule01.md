---
title: MDM_Reboot_Schedule01-Klasse
description: Der MDM- \_ Neustart \_ Schedule01class wird verwendet, um einen bestimmten Zeitpunkt für den Neustart eines Geräts zu konfigurieren.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- MDM_Reboot_Schedule01-Klasse
- MDM_Reboot_Schedule01-Klasse, beschrieben
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475291"
---
# <a name="mdm_reboot_schedule01-class"></a><span data-ttu-id="cc377-105">MDM- \_ Neustart \_ Schedule01 Klasse</span><span class="sxs-lookup"><span data-stu-id="cc377-105">MDM\_Reboot\_Schedule01 class</span></span>

<span data-ttu-id="cc377-106">\[Einige Informationen beziehen sich auf Vorabversionen, die vor der kommerziellen Freigabe grundlegend geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cc377-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cc377-107">Microsoft übernimmt keine Garantie, weder ausdrücklich noch stillschweigend, für die hier bereitgestellten Informationen.\]</span><span class="sxs-lookup"><span data-stu-id="cc377-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cc377-108">Die **MDM-Klasse " \_ Reboot \_ Schedule01**" wird verwendet, um einen bestimmten Zeitpunkt für den Neustart eines Geräts zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cc377-108">The **MDM\_Reboot\_Schedule01** class is used to configure a specific time for the reboot of a device.</span></span>

<span data-ttu-id="cc377-109">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="cc377-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc377-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc377-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a><span data-ttu-id="cc377-111">Member</span><span class="sxs-lookup"><span data-stu-id="cc377-111">Members</span></span>

<span data-ttu-id="cc377-112">Die **MDM-Klasse " \_ Reboot \_ Schedule01** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cc377-112">The **MDM\_Reboot\_Schedule01** class has these types of members:</span></span>

-   [<span data-ttu-id="cc377-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc377-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc377-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cc377-114">Properties</span></span>

<span data-ttu-id="cc377-115">Die **MDM \_ Reboot \_ Schedule01** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc377-115">The **MDM\_Reboot\_Schedule01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="cc377-116">Dailywiederkehr Ende</span><span class="sxs-lookup"><span data-stu-id="cc377-116">DailyRecurrent</span></span>](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc377-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cc377-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc377-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cc377-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cc377-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cc377-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc377-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cc377-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc377-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cc377-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc377-122">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cc377-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cc377-123">Gibt den Namen des übergeordneten Knotens an.</span><span class="sxs-lookup"><span data-stu-id="cc377-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="cc377-124">Für diese Klasse ist die Zeichenfolge "Schedule".</span><span class="sxs-lookup"><span data-stu-id="cc377-124">For this class, the string is "Schedule".</span></span>

</dd> <dt>

<span data-ttu-id="cc377-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cc377-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc377-126">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cc377-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc377-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="cc377-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc377-128">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cc377-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cc377-129">Beschreibt den vollständigen Pfad zum übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="cc377-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="cc377-130">Für diese Klasse ist die Zeichenfolge "./Vendor/MSFT/Reboot".</span><span class="sxs-lookup"><span data-stu-id="cc377-130">For this class, the string is "./Vendor/MSFT/Reboot"</span></span>

</dd> <dt>

[<span data-ttu-id="cc377-131">Single</span><span class="sxs-lookup"><span data-stu-id="cc377-131">Single</span></span>](/windows/client-management/mdm/reboot-csp#schedule-single)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc377-132">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="cc377-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc377-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="cc377-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc377-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc377-134">Requirements</span></span>



| <span data-ttu-id="cc377-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc377-135">Requirement</span></span> | <span data-ttu-id="cc377-136">Wert</span><span class="sxs-lookup"><span data-stu-id="cc377-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc377-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cc377-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cc377-138">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cc377-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cc377-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cc377-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cc377-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc377-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="cc377-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="cc377-141">Namespace</span></span><br/>                | <span data-ttu-id="cc377-142">Root \\ CIMV2 \\ MDM- \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cc377-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="cc377-143">MOF</span><span class="sxs-lookup"><span data-stu-id="cc377-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc377-144"><dt>DMWmiBridgeProv1. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cc377-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="cc377-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cc377-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc377-146"><dt>DMWmiBridgeProv.dllfür die \\</dt></span><span class="sxs-lookup"><span data-stu-id="cc377-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

