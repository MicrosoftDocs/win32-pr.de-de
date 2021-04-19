---
description: Enthält Methoden, mit denen die Monitor Helligkeit verwaltet wird.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Wmimonitorbrightnessmethods-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363578"
---
# <a name="wmimonitorbrightnessmethods-class"></a><span data-ttu-id="f074c-103">Wmimonitorbrightnessmethods-Klasse</span><span class="sxs-lookup"><span data-stu-id="f074c-103">WmiMonitorBrightnessMethods class</span></span>

<span data-ttu-id="f074c-104">Die **wmimonitorbrightnessmethods** -WMI-Klasse enthält Methoden, mit denen die Monitor Helligkeit verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="f074c-104">The **WmiMonitorBrightnessMethods** WMI class contains methods that manage monitor brightness.</span></span>

## <a name="syntax"></a><span data-ttu-id="f074c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f074c-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="f074c-106">Member</span><span class="sxs-lookup"><span data-stu-id="f074c-106">Members</span></span>

<span data-ttu-id="f074c-107">Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f074c-107">The **WmiMonitorBrightnessMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="f074c-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="f074c-108">Methods</span></span>](#wmimonitorbrightnessmethods-class)
-   [<span data-ttu-id="f074c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f074c-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f074c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f074c-110">Methods</span></span>

<span data-ttu-id="f074c-111">Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f074c-111">The **WmiMonitorBrightnessMethods** class has these methods.</span></span>



| <span data-ttu-id="f074c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="f074c-112">Method</span></span>                                                                                                         | <span data-ttu-id="f074c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f074c-113">Description</span></span>                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="f074c-114">**Wmireverttopolicyhelligkeit**</span><span class="sxs-lookup"><span data-stu-id="f074c-114">**WmiRevertToPolicyBrightness**</span></span>](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | <span data-ttu-id="f074c-115">Legt die Helligkeit auf die Richtlinien Einstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="f074c-115">Sets the brightness back to the policy setting.</span></span><br/>     |
| [<span data-ttu-id="f074c-116">**WMI-talshelligkeit**</span><span class="sxs-lookup"><span data-stu-id="f074c-116">**WmiSetALSBrightness**</span></span>](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | <span data-ttu-id="f074c-117">Legt den Wert für Umgebungslichtsensor-Helligkeit fest.</span><span class="sxs-lookup"><span data-stu-id="f074c-117">Sets the ambient light sensor brightness value.</span></span><br/>     |
| [<span data-ttu-id="f074c-118">**Wmiantalsbrightnessstate**</span><span class="sxs-lookup"><span data-stu-id="f074c-118">**WmiSetALSBrightnessState**</span></span>](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | <span data-ttu-id="f074c-119">Steuert den Helligkeit-Zustand des Umgebungslicht Sensors.</span><span class="sxs-lookup"><span data-stu-id="f074c-119">Controls the ambient light sensor brightness state.</span></span><br/> |
| [<span data-ttu-id="f074c-120">**Wmisethelligkeit**</span><span class="sxs-lookup"><span data-stu-id="f074c-120">**WmiSetBrightness**</span></span>](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | <span data-ttu-id="f074c-121">Legt die Helligkeit des Monitors fest.</span><span class="sxs-lookup"><span data-stu-id="f074c-121">Sets the monitor brightness.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="f074c-122">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f074c-122">Properties</span></span>

<span data-ttu-id="f074c-123">Die **wmimonitorbrightnessmethods** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f074c-123">The **WmiMonitorBrightnessMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f074c-124">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="f074c-124">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f074c-125">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="f074c-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f074c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f074c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f074c-127">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="f074c-127">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="f074c-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f074c-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f074c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f074c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f074c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f074c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f074c-131">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="f074c-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f074c-132">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="f074c-132">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f074c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f074c-133">Requirements</span></span>



| <span data-ttu-id="f074c-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f074c-134">Requirement</span></span> | <span data-ttu-id="f074c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f074c-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f074c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f074c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f074c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f074c-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f074c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f074c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f074c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f074c-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f074c-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="f074c-140">Namespace</span></span><br/>                | <span data-ttu-id="f074c-141">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="f074c-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f074c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="f074c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f074c-143"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f074c-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f074c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f074c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f074c-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f074c-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f074c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f074c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f074c-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="f074c-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




