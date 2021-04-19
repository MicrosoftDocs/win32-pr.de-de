---
description: Listet die unterstützten Quell Modi für einen Videomonitor in seinem Monitor Deskriptor auf, sofern vorhanden.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Wmimonitorlistedsupportedsourcemodes-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357861"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="98e48-103">Wmimonitorlistedsupportedsourcemodes-Klasse</span><span class="sxs-lookup"><span data-stu-id="98e48-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="98e48-104">**Wmimonitorlistedsupportedsourcemodes** listet die unterstützten Quell Modi für einen Videomonitor in seinem Monitor Deskriptor auf, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98e48-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="98e48-105">Für Monitore, die keine Beschreibung aufweisen, wird diese Liste der Modi basierend auf der Art des Monitors generiert, wie vom Monitor Bustreiber angegeben.</span><span class="sxs-lookup"><span data-stu-id="98e48-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e48-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="98e48-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="98e48-107">Member</span><span class="sxs-lookup"><span data-stu-id="98e48-107">Members</span></span>

<span data-ttu-id="98e48-108">Die **wmimonitorlistedsupportedsourcemodes** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98e48-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="98e48-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98e48-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98e48-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98e48-110">Properties</span></span>

<span data-ttu-id="98e48-111">Die **wmimonitorlistedsupportedsourcemodes** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98e48-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98e48-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="98e48-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e48-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="98e48-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98e48-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98e48-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e48-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="98e48-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="98e48-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="98e48-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e48-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="98e48-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98e48-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98e48-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98e48-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="98e48-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="98e48-120">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="98e48-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="98e48-121">**Monitorsourcemodes**</span><span class="sxs-lookup"><span data-stu-id="98e48-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e48-122">Datentyp: **videomodedescriptor** -Array</span><span class="sxs-lookup"><span data-stu-id="98e48-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="98e48-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98e48-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e48-124">Listet die Monitor Quellmodi auf, die durch Instanzen der [**videomodedescriptor**](videomodedescriptor.md) -Klasse dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="98e48-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="98e48-125">**Numuf monitorsourcemodes**</span><span class="sxs-lookup"><span data-stu-id="98e48-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e48-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e48-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98e48-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98e48-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e48-128">Anzahl der aufgeführten unterstützten Monitor Quellen Modus.</span><span class="sxs-lookup"><span data-stu-id="98e48-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="98e48-129">**Preferredmonitorsourcemodeingedex**</span><span class="sxs-lookup"><span data-stu-id="98e48-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98e48-130">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="98e48-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="98e48-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98e48-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98e48-132">Bevorzugter Monitor Quell Modus-Index.</span><span class="sxs-lookup"><span data-stu-id="98e48-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98e48-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98e48-133">Requirements</span></span>



| <span data-ttu-id="98e48-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98e48-134">Requirement</span></span> | <span data-ttu-id="98e48-135">Wert</span><span class="sxs-lookup"><span data-stu-id="98e48-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98e48-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98e48-136">Minimum supported client</span></span><br/> | <span data-ttu-id="98e48-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98e48-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98e48-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98e48-138">Minimum supported server</span></span><br/> | <span data-ttu-id="98e48-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98e48-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98e48-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="98e48-140">Namespace</span></span><br/>                | <span data-ttu-id="98e48-141">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="98e48-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="98e48-142">MOF</span><span class="sxs-lookup"><span data-stu-id="98e48-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98e48-143"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="98e48-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="98e48-144">DLL</span><span class="sxs-lookup"><span data-stu-id="98e48-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98e48-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98e48-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e48-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98e48-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e48-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="98e48-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




