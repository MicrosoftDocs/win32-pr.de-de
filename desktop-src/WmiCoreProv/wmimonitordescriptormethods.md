---
description: Enthält Methoden, die den unformatierten Inhalt der Videoeingabe Definition von (VESA) erweiterten erweiterten Display Identification Data (E-EDID) v. 1. x-Standard-128-Byte-Datenblöcken abrufen.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Wmimonitordescriptormethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359207"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="abd69-103">Wmimonitordescriptormethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="abd69-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="abd69-104">Die **wmimonitordescriptormethods** -WMI-Klasse enthält Methoden, die den unformatierten Inhalt der Videoeingabe Definition von (VESA) erweiterten erweiterten Display Identification Data (E-EDID) v. 1. x-Standard-128-Byte-Datenblöcken abrufen.</span><span class="sxs-lookup"><span data-stu-id="abd69-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd69-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="abd69-106">Member</span><span class="sxs-lookup"><span data-stu-id="abd69-106">Members</span></span>

<span data-ttu-id="abd69-107">Die **wmimonitordescriptormethods** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="abd69-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="abd69-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="abd69-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="abd69-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abd69-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="abd69-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="abd69-110">Methods</span></span>

<span data-ttu-id="abd69-111">Die **wmimonitordescriptormethods** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="abd69-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="abd69-112">Methode</span><span class="sxs-lookup"><span data-stu-id="abd69-112">Method</span></span>                                                                                           | <span data-ttu-id="abd69-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abd69-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="abd69-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="abd69-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="abd69-115">Greift auf die Rohdaten für einen angegebenen EDID v. 1. x-deskriptorblock zu.</span><span class="sxs-lookup"><span data-stu-id="abd69-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="abd69-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="abd69-116">Properties</span></span>

<span data-ttu-id="abd69-117">Die **wmimonitordescriptormethods** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="abd69-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abd69-118">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="abd69-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd69-119">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="abd69-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="abd69-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd69-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abd69-121">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="abd69-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="abd69-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="abd69-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abd69-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="abd69-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abd69-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="abd69-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abd69-125">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="abd69-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="abd69-126">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="abd69-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abd69-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd69-127">Requirements</span></span>



| <span data-ttu-id="abd69-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abd69-128">Requirement</span></span> | <span data-ttu-id="abd69-129">Wert</span><span class="sxs-lookup"><span data-stu-id="abd69-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="abd69-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd69-130">Minimum supported client</span></span><br/> | <span data-ttu-id="abd69-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abd69-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="abd69-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd69-132">Minimum supported server</span></span><br/> | <span data-ttu-id="abd69-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abd69-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="abd69-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="abd69-134">Namespace</span></span><br/>                | <span data-ttu-id="abd69-135">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="abd69-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="abd69-136">MOF</span><span class="sxs-lookup"><span data-stu-id="abd69-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abd69-137"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abd69-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="abd69-138">DLL</span><span class="sxs-lookup"><span data-stu-id="abd69-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd69-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd69-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd69-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abd69-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd69-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="abd69-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




