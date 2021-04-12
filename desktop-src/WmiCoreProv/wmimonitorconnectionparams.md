---
description: Enthält den Verbindungstyp des Monitors.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Wmimonitorconnectionparser-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216905"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="e1dbd-103">Wmimonitorconnectionparser-Klasse</span><span class="sxs-lookup"><span data-stu-id="e1dbd-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="e1dbd-104">Die wmimonitorconnectionparser-WMI-Klasse enthält den Verbindungstyp des Monitors.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="e1dbd-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1dbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1dbd-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="e1dbd-107">Member</span><span class="sxs-lookup"><span data-stu-id="e1dbd-107">Members</span></span>

<span data-ttu-id="e1dbd-108">Die **wmimonitorconnectionparser** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e1dbd-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="e1dbd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1dbd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1dbd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e1dbd-110">Properties</span></span>

<span data-ttu-id="e1dbd-111">Die **wmimonitorconnectionparser** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1dbd-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="e1dbd-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1dbd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="e1dbd-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1dbd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-120">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="e1dbd-121">**Videooutputtechnology**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1dbd-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1dbd-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e1dbd-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1dbd-124">Verbindungstyp der Video Ausgabe Technologie.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-124">Video output technology connection type.</span></span> <span data-ttu-id="e1dbd-125">Gültige Werte sind in der [D3DKMDT \_ Video \_ Output \_ Technology](https://msdn.microsoft.com/library/ms794498.aspx) -Enumeration dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="e1dbd-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](https://msdn.microsoft.com/library/ms794498.aspx) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1dbd-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e1dbd-126">Requirements</span></span>



| <span data-ttu-id="e1dbd-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e1dbd-127">Requirement</span></span> | <span data-ttu-id="e1dbd-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e1dbd-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1dbd-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e1dbd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e1dbd-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1dbd-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e1dbd-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e1dbd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e1dbd-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1dbd-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e1dbd-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1dbd-133">Namespace</span></span><br/>                | <span data-ttu-id="e1dbd-134">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="e1dbd-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e1dbd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e1dbd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1dbd-136"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e1dbd-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1dbd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e1dbd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1dbd-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1dbd-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1dbd-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1dbd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1dbd-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="e1dbd-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




