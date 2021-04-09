---
description: Legt den Energiezustand des Computers fest. Die Verwendung dieser Methode ist veraltet. Verwenden Sie stattdessen die SetPowerState-Methode in der zugehörigen powermanagementservice-Klasse.
ms.assetid: c2196f35-f687-4d82-a068-f8499f77473a
title: SetPowerState-Methode der CIM_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem.SetPowerState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9c9e264e8ec62c1e49e92226d1abc8ac902c0b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042406"
---
# <a name="setpowerstate-method-of-the-cim_computersystem-class"></a><span data-ttu-id="32222-105">SetPowerState-Methode der CIM \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="32222-105">SetPowerState method of the CIM\_ComputerSystem class</span></span>

<span data-ttu-id="32222-106">Legt den Energiezustand des Computers fest.</span><span class="sxs-lookup"><span data-stu-id="32222-106">Sets the power state of the computer.</span></span> <span data-ttu-id="32222-107">Die Verwendung dieser Methode ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="32222-107">The use of this method has been deprecated.</span></span> <span data-ttu-id="32222-108">Verwenden Sie stattdessen die **SetPowerState** -Methode in der zugehörigen **powermanagementservice** -Klasse.</span><span class="sxs-lookup"><span data-stu-id="32222-108">Instead, use the **SetPowerState** method in the associated **PowerManagementService** class.</span></span>

## <a name="syntax"></a><span data-ttu-id="32222-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="32222-109">Syntax</span></span>


```mof
uint32 SetPowerState(
  [in] uint32   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a><span data-ttu-id="32222-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="32222-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32222-111">*PowerState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32222-111">*PowerState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32222-112">Der gewünschte Zustand für das Computersystem.</span><span class="sxs-lookup"><span data-stu-id="32222-112">The desired state for the computer system.</span></span>

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="32222-113">**Vollstrom** (1)</span><span class="sxs-lookup"><span data-stu-id="32222-113">**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="32222-114">**Energiesparmodus-niedriger Energie Modus** (2)</span><span class="sxs-lookup"><span data-stu-id="32222-114">**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="32222-115">**Energiesparmodus-Standby** (3)</span><span class="sxs-lookup"><span data-stu-id="32222-115">**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span data-ttu-id="32222-116">**Energiespar Speicher-andere** (4)</span><span class="sxs-lookup"><span data-stu-id="32222-116">**Power Save - Other** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="32222-117">**Energie Zyklen** (5)</span><span class="sxs-lookup"><span data-stu-id="32222-117">**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="32222-118">**Ausschalten** (6)</span><span class="sxs-lookup"><span data-stu-id="32222-118">**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span data-ttu-id="32222-119">Ruhe **Zustand (7** )</span><span class="sxs-lookup"><span data-stu-id="32222-119">**Hibernate** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span data-ttu-id="32222-120">**Soft Off** (8)</span><span class="sxs-lookup"><span data-stu-id="32222-120">**Soft Off** (8)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="32222-121">*Uhrzeit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32222-121">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32222-122">Time gibt an, wann der Energiezustand festgelegt werden soll, entweder als regulärer Datums-/Uhrzeitwert oder als Intervall Wert (wobei das Intervall beginnt, wenn der Methodenaufruf empfangen wird).</span><span class="sxs-lookup"><span data-stu-id="32222-122">Time indicates when the power state should be set, either as a regular date-time value or as an interval value (where the interval begins when the method invocation is received).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32222-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32222-123">Requirements</span></span>



| <span data-ttu-id="32222-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32222-124">Requirement</span></span> | <span data-ttu-id="32222-125">Wert</span><span class="sxs-lookup"><span data-stu-id="32222-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32222-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32222-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32222-127">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="32222-127">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="32222-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32222-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32222-129">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="32222-129">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="32222-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="32222-130">Namespace</span></span><br/>                | <span data-ttu-id="32222-131">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="32222-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="32222-132">MOF</span><span class="sxs-lookup"><span data-stu-id="32222-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32222-133"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="32222-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="32222-134">DLL</span><span class="sxs-lookup"><span data-stu-id="32222-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32222-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="32222-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="32222-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32222-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32222-137">**CIM- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="32222-137">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

 




