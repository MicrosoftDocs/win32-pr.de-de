---
description: Eine Beziehung, die angibt, dass zwei oder mehr Geräte miteinander verbunden sind.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343355"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a><span data-ttu-id="02619-103">CIM_DeviceConnection-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="02619-103">CIM_DeviceConnection class (Hyper-V management)</span></span>

<span data-ttu-id="02619-104">Eine Beziehung, die angibt, dass zwei oder mehr Geräte miteinander verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="02619-104">A relationship that indicates that two or more devices are connected together.</span></span>

## <a name="syntax"></a><span data-ttu-id="02619-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02619-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a><span data-ttu-id="02619-106">Member</span><span class="sxs-lookup"><span data-stu-id="02619-106">Members</span></span>

<span data-ttu-id="02619-107">Die **CIM- \_ deviceconnetction** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="02619-107">The **CIM\_DeviceConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="02619-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02619-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02619-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="02619-109">Properties</span></span>

<span data-ttu-id="02619-110">Die **CIM- \_ deviceconnetction** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="02619-110">The **CIM\_DeviceConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02619-111">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="02619-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02619-112">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="02619-112">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="02619-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02619-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02619-114">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="02619-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="02619-115">Ein Gerät</span><span class="sxs-lookup"><span data-stu-id="02619-115">A device.</span></span>

</dd> <dt>

<span data-ttu-id="02619-116">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="02619-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02619-117">Datentyp: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="02619-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="02619-118">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02619-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02619-119">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="02619-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="02619-120">Ein zweites Gerät, das mit dem anderen Gerät verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="02619-120">A second device that is connected to the other device.</span></span>

</dd> <dt>

<span data-ttu-id="02619-121">**Aushandateddatawidth**</span><span class="sxs-lookup"><span data-stu-id="02619-121">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02619-122">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02619-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02619-123">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02619-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02619-124">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port Association \| 001,3 "), **Punit** (" Bit ")</span><span class="sxs-lookup"><span data-stu-id="02619-124">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.3"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="02619-125">Wenn mehrere Bus-und Verbindungsdaten breiten möglich sind, wird von der aushandateddatawidth-Eigenschaft der Wert definiert, der zwischen den Geräten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02619-125">When several bus and connection data widths are possible, the NegotiatedDataWidth property defines the one that is in use between the Devices.</span></span> <span data-ttu-id="02619-126">Die Daten Breite wird in Bits angegeben.</span><span class="sxs-lookup"><span data-stu-id="02619-126">Data width is specified in bits.</span></span> <span data-ttu-id="02619-127">Wenn die Daten Breite nicht ausgehandelt wird oder diese Informationen für die Geräteverwaltung nicht verfügbar oder nicht wichtig sind, sollte die-Eigenschaft auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="02619-127">If data width is not negotiated, or if this information is not available or not important to Device management, the property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="02619-128">**Aushandatedspeed**</span><span class="sxs-lookup"><span data-stu-id="02619-128">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02619-129">Datentyp: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="02619-129">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="02619-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="02619-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02619-131">Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits pro Sekunde"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| Bus Port Association \| 001,2 "), **Punit** (" Bit/Sekunde ")</span><span class="sxs-lookup"><span data-stu-id="02619-131">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port Association\|001.2"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="02619-132">Wenn mehrere Bus-und Verbindungsgeschwindigkeiten möglich sind, definiert diese Eigenschaft die verwendete Geschwindigkeit zwischen den Geräten in Bits pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="02619-132">When several bus and connection speeds are possible, this property defines the speed that is in use between the devices, in bits per second.</span></span> <span data-ttu-id="02619-133">Wenn Verbindungs-oder Busgeschwindigkeiten nicht ausgehandelt werden oder diese Informationen nicht verfügbar oder nicht für die Geräteverwaltung wichtig sind, sollte die-Eigenschaft auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="02619-133">If connection or bus speeds are not negotiated, or if this information is not available, or not important to device management, the property should be set to "0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02619-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02619-134">Requirements</span></span>



| <span data-ttu-id="02619-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02619-135">Requirement</span></span> | <span data-ttu-id="02619-136">Wert</span><span class="sxs-lookup"><span data-stu-id="02619-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02619-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02619-137">Minimum supported client</span></span><br/> | <span data-ttu-id="02619-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="02619-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="02619-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02619-139">Minimum supported server</span></span><br/> | <span data-ttu-id="02619-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02619-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="02619-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="02619-141">Namespace</span></span><br/>                | <span data-ttu-id="02619-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="02619-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02619-143">MOF</span><span class="sxs-lookup"><span data-stu-id="02619-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02619-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="02619-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02619-145">DLL</span><span class="sxs-lookup"><span data-stu-id="02619-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02619-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02619-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02619-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02619-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02619-148">**CIM- \_ Abhängigkeit**</span><span class="sxs-lookup"><span data-stu-id="02619-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

