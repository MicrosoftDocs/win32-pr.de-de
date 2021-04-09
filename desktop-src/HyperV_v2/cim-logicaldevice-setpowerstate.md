---
description: Legt den Energiezustand des Geräts fest. Die Verwendung dieser Methode ist veraltet. Verwenden Sie stattdessen die SetPowerState-Methode in der zugehörigen powermanagementservice-Klasse.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: SetPowerState-Methode der CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a29f71806747e6d63f53618acd09d472ac8bdea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960275"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a><span data-ttu-id="b5541-105">SetPowerState-Methode der CIM_LogicalDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="b5541-105">SetPowerState method of the CIM_LogicalDevice class (Hyper-V management)</span></span>

<span data-ttu-id="b5541-106">Legt den Energiezustand des Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="b5541-106">Sets the power state of the Device.</span></span> <span data-ttu-id="b5541-107">Die Verwendung dieser Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="b5541-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="b5541-108">Verwenden Sie stattdessen die **SetPowerState** -Methode in der zugehörigen **powermanagementservice** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="b5541-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5541-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5541-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="b5541-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5541-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5541-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5541-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5541-112">Der festzulegende Energiezustand.</span><span class="sxs-lookup"><span data-stu-id="b5541-112">The power state to set.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="b5541-113">**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="b5541-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b5541-114">**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="b5541-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b5541-115">**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="b5541-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="b5541-116">**Energiespar Speicher-andere** (4)</span><span class="sxs-lookup"><span data-stu-id="b5541-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b5541-117">**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="b5541-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b5541-118">**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="b5541-118">**Power Off** (6)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b5541-119">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5541-119">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5541-120">Time gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="b5541-120">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5541-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5541-121">Return value</span></span>

<span data-ttu-id="b5541-122">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b5541-122">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5541-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5541-123">Requirements</span></span>



| <span data-ttu-id="b5541-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5541-124">Requirement</span></span> | <span data-ttu-id="b5541-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b5541-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5541-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5541-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5541-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b5541-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b5541-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5541-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5541-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b5541-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b5541-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5541-130">Namespace</span></span><br/>                | <span data-ttu-id="b5541-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="b5541-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b5541-132">MOF</span><span class="sxs-lookup"><span data-stu-id="b5541-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5541-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b5541-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5541-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b5541-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5541-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5541-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5541-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5541-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5541-137">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="b5541-137">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




