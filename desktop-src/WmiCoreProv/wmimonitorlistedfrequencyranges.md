---
description: Listet die vom Monitor unterstützten Häufigkeits Bereiche auf.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Wmimonitorlistedfrequencyranges-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357862"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="54ce3-103">Wmimonitorlistedfrequencyranges-Klasse</span><span class="sxs-lookup"><span data-stu-id="54ce3-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="54ce3-104">Die WMI-Klasse **wmimonitorlistedfrequencyranges** listet die vom Monitor unterstützten Häufigkeits Bereiche auf.</span><span class="sxs-lookup"><span data-stu-id="54ce3-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="54ce3-105">Diese Bereiche finden Sie in der Videoeingabe Definition von "velectronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) Block" oder in der Windows INF-Datei, die Gerätetreiber Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="54ce3-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="54ce3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ce3-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="54ce3-107">Member</span><span class="sxs-lookup"><span data-stu-id="54ce3-107">Members</span></span>

<span data-ttu-id="54ce3-108">Die **wmimonitorlistedfrequencyranges** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="54ce3-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="54ce3-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ce3-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54ce3-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="54ce3-110">Properties</span></span>

<span data-ttu-id="54ce3-111">Die **wmimonitorlistedfrequencyranges** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="54ce3-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="54ce3-112">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="54ce3-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ce3-113">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="54ce3-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="54ce3-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ce3-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ce3-115">Gibt den aktiven Monitor an.</span><span class="sxs-lookup"><span data-stu-id="54ce3-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="54ce3-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ce3-117">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="54ce3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54ce3-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ce3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54ce3-119">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="54ce3-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="54ce3-120">Der Name der spezifischen Monitor Instanz.</span><span class="sxs-lookup"><span data-stu-id="54ce3-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-121">**Monitorfreqranges**</span><span class="sxs-lookup"><span data-stu-id="54ce3-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ce3-122">Datentyp: **frequencyrangedescriptor** -Array</span><span class="sxs-lookup"><span data-stu-id="54ce3-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="54ce3-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ce3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ce3-124">Liste der Monitor Häufigkeits Bereiche, die durch Instanzen der [**frequencyrangedescriptor**](frequencyrangedescriptor.md) -Klasse dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54ce3-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="54ce3-125">**Numuf-monitorfreqranges**</span><span class="sxs-lookup"><span data-stu-id="54ce3-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54ce3-126">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="54ce3-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="54ce3-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="54ce3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="54ce3-128">Anzahl der aufgeführten unterstützten Monitor Häufigkeits Bereiche.</span><span class="sxs-lookup"><span data-stu-id="54ce3-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54ce3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54ce3-129">Requirements</span></span>



| <span data-ttu-id="54ce3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54ce3-130">Requirement</span></span> | <span data-ttu-id="54ce3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="54ce3-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54ce3-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54ce3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="54ce3-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54ce3-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="54ce3-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54ce3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="54ce3-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54ce3-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="54ce3-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="54ce3-136">Namespace</span></span><br/>                | <span data-ttu-id="54ce3-137">WMI-Stammdatei \\</span><span class="sxs-lookup"><span data-stu-id="54ce3-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="54ce3-138">MOF</span><span class="sxs-lookup"><span data-stu-id="54ce3-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54ce3-139"><dt>WMI Core. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="54ce3-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="54ce3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="54ce3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54ce3-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54ce3-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ce3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54ce3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ce3-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="54ce3-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




