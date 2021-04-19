---
description: Stellt die Parameter für die Helligkeit eines Computermonitors dar.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Wmimonitorbrightness-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: b8d16c8dc20291a03fb205441c8826c85125970c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369803"
---
# <a name="wmimonitorbrightness-class"></a><span data-ttu-id="98684-103">Wmimonitorbrightness-Klasse</span><span class="sxs-lookup"><span data-stu-id="98684-103">WmiMonitorBrightness class</span></span>

<span data-ttu-id="98684-104">Die **wmimonitorbrightness** WMI-Klasse stellt die Parameter für die Helligkeit eines Computermonitors dar.</span><span class="sxs-lookup"><span data-stu-id="98684-104">The **WmiMonitorBrightness** WMI class represents the brightness parameters of a computer monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="98684-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98684-105">Syntax</span></span>

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a><span data-ttu-id="98684-106">Member</span><span class="sxs-lookup"><span data-stu-id="98684-106">Members</span></span>

<span data-ttu-id="98684-107">Die **wmimonitorbrightness** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="98684-107">The **WmiMonitorBrightness** class has these types of members:</span></span>

-   [<span data-ttu-id="98684-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98684-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98684-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="98684-109">Properties</span></span>

<span data-ttu-id="98684-110">Die **wmimonitorbrightness** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="98684-110">The **WmiMonitorBrightness** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98684-111">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="98684-111">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98684-112">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="98684-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="98684-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98684-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98684-114">Gibt an, ob der Ziel Monitor aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="98684-114">Indicates if the target monitor is active.</span></span>

</dd> <dt>

<span data-ttu-id="98684-115">**Currenthelligkeit**</span><span class="sxs-lookup"><span data-stu-id="98684-115">**CurrentBrightness**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98684-116">Datentyp: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="98684-116">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="98684-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98684-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98684-118">Aktuelle Helligkeit.</span><span class="sxs-lookup"><span data-stu-id="98684-118">Current brightness.</span></span> <span data-ttu-id="98684-119">Dieser Wert muss ein Wert sein, der von *Ebenen* übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="98684-119">This value must be a value taken from *Levels*.</span></span>

<span data-ttu-id="98684-120">Beispiel: 100</span><span class="sxs-lookup"><span data-stu-id="98684-120">Example: 100</span></span>

</dd> <dt>

<span data-ttu-id="98684-121">InstanceName</span><span class="sxs-lookup"><span data-stu-id="98684-121">InstanceName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98684-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98684-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98684-123">Qualifizierer: Schlüssel</span><span class="sxs-lookup"><span data-stu-id="98684-123">Qualifiers: Key</span></span>
</dt> </dl>

<span data-ttu-id="98684-124">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="98684-124">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="98684-125">**Level**</span><span class="sxs-lookup"><span data-stu-id="98684-125">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98684-126">Datentyp: **Uint8** Array</span><span class="sxs-lookup"><span data-stu-id="98684-126">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="98684-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98684-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98684-128">Ein Array, das die möglichen Helligkeits Ebenen enthält.</span><span class="sxs-lookup"><span data-stu-id="98684-128">Array containing the possible brightness levels.</span></span>

<span data-ttu-id="98684-129">Beispiel: \[ 0, 1, 2,..., 100 \] .</span><span class="sxs-lookup"><span data-stu-id="98684-129">Example: \[0, 1, 2, ..., 100\].</span></span>

</dd> <dt>

<span data-ttu-id="98684-130">**Ebenen**</span><span class="sxs-lookup"><span data-stu-id="98684-130">**Levels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98684-131">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98684-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98684-132">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="98684-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98684-133">Die Gesamtanzahl der vom Monitor unterstützten Helligkeitsstufen, wie unter *Ebene* beschrieben.</span><span class="sxs-lookup"><span data-stu-id="98684-133">The total number of brightness levels the monitor supports, as described in *Level*.</span></span>

<span data-ttu-id="98684-134">Beispiel: 101</span><span class="sxs-lookup"><span data-stu-id="98684-134">Example: 101</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="98684-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98684-135">Examples</span></span>

<span data-ttu-id="98684-136">Weitere Informationen und Codebeispiele zur Verwendung dieser Klasse in PowerShell finden Sie unter [Verwenden von PowerShell zum melden und Festlegen der Monitor Helligkeit](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span><span class="sxs-lookup"><span data-stu-id="98684-136">For more information and code samples on using this class in PowerShell, see [Use PowerShell to Report and Set Monitor Brightness](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx).</span></span>

## <a name="requirements"></a><span data-ttu-id="98684-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98684-137">Requirements</span></span>



| <span data-ttu-id="98684-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98684-138">Requirement</span></span> | <span data-ttu-id="98684-139">Wert</span><span class="sxs-lookup"><span data-stu-id="98684-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98684-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98684-140">Minimum supported client</span></span><br/> | <span data-ttu-id="98684-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98684-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98684-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98684-142">Minimum supported server</span></span><br/> | <span data-ttu-id="98684-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98684-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98684-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="98684-144">Namespace</span></span><br/>                | <span data-ttu-id="98684-145">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="98684-145">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="98684-146">MOF</span><span class="sxs-lookup"><span data-stu-id="98684-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98684-147"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="98684-147"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="98684-148">DLL</span><span class="sxs-lookup"><span data-stu-id="98684-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98684-149"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98684-149"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98684-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98684-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98684-151">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="98684-151">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




