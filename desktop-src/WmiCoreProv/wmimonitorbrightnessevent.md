---
description: Stellt eine Änderung der Helligkeit eines Monitors dar.
ms.assetid: c2eb5630-a52f-4ad4-aaee-1cc8afef8c9e
title: Wmimonitorbrightnessvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessEvent
- WmiMonitorBrightnessEvent.Active
- WmiMonitorBrightnessEvent.Brightness
- WmiMonitorBrightnessEvent.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e53f90627c959db0140b01cf3b3d385afcc6e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349583"
---
# <a name="wmimonitorbrightnessevent-class"></a><span data-ttu-id="9b171-103">Wmimonitorbrightnessvent-Klasse</span><span class="sxs-lookup"><span data-stu-id="9b171-103">WmiMonitorBrightnessEvent class</span></span>

<span data-ttu-id="9b171-104">Die **wmimonitorbrightnesgvent** WMI-Ereignisklasse stellt eine Änderung der Helligkeit eines Monitors dar.</span><span class="sxs-lookup"><span data-stu-id="9b171-104">The **WmiMonitorBrightnessEvent** WMI event class represents a change in the brightness of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b171-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b171-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessEvent : WMIEvent
{
  boolean Active;
  uint8   Brightness;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="9b171-106">Member</span><span class="sxs-lookup"><span data-stu-id="9b171-106">Members</span></span>

<span data-ttu-id="9b171-107">Die **wmimonitorbrightnestarvent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9b171-107">The **WmiMonitorBrightnessEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="9b171-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b171-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b171-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9b171-109">Properties</span></span>

<span data-ttu-id="9b171-110">Die **wmimonitorbrightnessvent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b171-110">The **WmiMonitorBrightnessEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b171-111">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="9b171-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b171-112">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="9b171-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b171-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b171-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b171-114">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="9b171-114">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="9b171-115">**Helligkeit**</span><span class="sxs-lookup"><span data-stu-id="9b171-115">**Brightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b171-116">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9b171-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="9b171-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b171-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b171-118">Aktuelle Monitor Helligkeit als Prozentsatz.</span><span class="sxs-lookup"><span data-stu-id="9b171-118">Current monitor brightness as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="9b171-119">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="9b171-119">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b171-120">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="9b171-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b171-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9b171-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b171-122">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="9b171-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9b171-123">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b171-123">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b171-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9b171-124">Requirements</span></span>



| <span data-ttu-id="9b171-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9b171-125">Requirement</span></span> | <span data-ttu-id="9b171-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9b171-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b171-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9b171-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b171-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b171-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9b171-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9b171-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b171-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b171-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9b171-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b171-131">Namespace</span></span><br/>                | <span data-ttu-id="9b171-132">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="9b171-132">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="9b171-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9b171-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b171-134"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-134"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b171-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9b171-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b171-136"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b171-136"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b171-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b171-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b171-138">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="9b171-138">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="9b171-139">**Wmimonitorhelligkeit**</span><span class="sxs-lookup"><span data-stu-id="9b171-139">**WmiMonitorBrightness**</span></span>](wmimonitorbrightness.md)
</dt> <dt>

[<span data-ttu-id="9b171-140">Empfangen eines WMI-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="9b171-140">Receiving a WMI Event</span></span>](/windows/desktop/WmiSdk/receiving-a-wmi-event)
</dt> </dl>

 

