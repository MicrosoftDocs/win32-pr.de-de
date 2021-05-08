---
description: Enthält den Verbindungstyp des Monitors.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: WmiMonitorConnectionParams-Klasse
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
ms.openlocfilehash: a88b80773ec60b161df51fc759cc932d5c53c931
ms.sourcegitcommit: cfcac5a083b72fd7f2a5188166d470cc0e95d02d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2021
ms.locfileid: "109626692"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="51486-103">WmiMonitorConnectionParams-Klasse</span><span class="sxs-lookup"><span data-stu-id="51486-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="51486-104">Die WMI-Klasse WmiMonitorConnectionParams enthält den Verbindungstyp des Monitors.</span><span class="sxs-lookup"><span data-stu-id="51486-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="51486-105">Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="51486-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="51486-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="51486-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="51486-107">Member</span><span class="sxs-lookup"><span data-stu-id="51486-107">Members</span></span>

<span data-ttu-id="51486-108">Die **WmiMonitorConnectionParams-Klasse** verfügt über folgende Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51486-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="51486-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51486-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51486-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51486-110">Properties</span></span>

<span data-ttu-id="51486-111">Die **WmiMonitorConnectionParams-Klasse** verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="51486-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51486-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="51486-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51486-113">Datentyp: **boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="51486-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51486-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51486-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51486-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="51486-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="51486-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="51486-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51486-117">Datentyp: **string**</span><span class="sxs-lookup"><span data-stu-id="51486-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51486-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51486-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51486-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="51486-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="51486-120">Name der spezifischen Überwachungsinstanz.</span><span class="sxs-lookup"><span data-stu-id="51486-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="51486-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="51486-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51486-122">Datentyp: **uint32**</span><span class="sxs-lookup"><span data-stu-id="51486-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="51486-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="51486-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51486-124">Verbindungstyp der Videoausgabetechnologie.</span><span class="sxs-lookup"><span data-stu-id="51486-124">Video output technology connection type.</span></span> <span data-ttu-id="51486-125">Gültige Werte sind in der [D3DKMDT \_ VIDEO \_ OUTPUT \_ TECHNOLOGY-Enumeration](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="51486-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51486-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51486-126">Requirements</span></span>



| <span data-ttu-id="51486-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51486-127">Requirement</span></span> | <span data-ttu-id="51486-128">Wert</span><span class="sxs-lookup"><span data-stu-id="51486-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51486-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51486-129">Minimum supported client</span></span><br/> | <span data-ttu-id="51486-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51486-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="51486-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51486-131">Minimum supported server</span></span><br/> | <span data-ttu-id="51486-132">WindowsServer 2008</span><span class="sxs-lookup"><span data-stu-id="51486-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="51486-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="51486-133">Namespace</span></span><br/>                | <span data-ttu-id="51486-134">Root \\ wmi</span><span class="sxs-lookup"><span data-stu-id="51486-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="51486-135">MOF</span><span class="sxs-lookup"><span data-stu-id="51486-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51486-136"><dt>WmiCore.mof</dt></span><span class="sxs-lookup"><span data-stu-id="51486-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="51486-137">DLL</span><span class="sxs-lookup"><span data-stu-id="51486-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51486-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51486-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51486-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51486-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51486-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="51486-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




