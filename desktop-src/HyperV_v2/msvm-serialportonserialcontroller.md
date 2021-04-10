---
description: Ordnet einen seriellen Anschluss einem seriellen Controller zu.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Msvm_SerialPortOnSerialController-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863051"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="d210b-103">MSVM \_ serialportonserialcontroller-Klasse</span><span class="sxs-lookup"><span data-stu-id="d210b-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="d210b-104">Ordnet einen seriellen Anschluss einem seriellen Controller zu.</span><span class="sxs-lookup"><span data-stu-id="d210b-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="d210b-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d210b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d210b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d210b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d210b-107">Member</span><span class="sxs-lookup"><span data-stu-id="d210b-107">Members</span></span>

<span data-ttu-id="d210b-108">Die **MSVM \_ serialportonserialcontroller** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d210b-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="d210b-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d210b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d210b-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d210b-110">Properties</span></span>

<span data-ttu-id="d210b-111">Die **MSVM \_ serialportonserialcontroller** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d210b-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d210b-112">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="d210b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d210b-113">Datentyp: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="d210b-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="d210b-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d210b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d210b-115">Der serielle Controller, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="d210b-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="d210b-116">Diese Eigenschaft wird von [**CIM \_ portondevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d210b-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="d210b-117">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="d210b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d210b-118">Datentyp: **[ **CIM \_ logicalport**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d210b-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="d210b-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d210b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d210b-120">Der Port des seriellen Controllers.</span><span class="sxs-lookup"><span data-stu-id="d210b-120">The port of the serial controller.</span></span> <span data-ttu-id="d210b-121">Diese Eigenschaft wird von [**CIM \_ portondevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d210b-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d210b-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d210b-122">Remarks</span></span>

<span data-ttu-id="d210b-123">Der Zugriff auf die **MSVM \_ serialportonserialcontroller** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="d210b-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d210b-124">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d210b-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d210b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d210b-125">Requirements</span></span>



| <span data-ttu-id="d210b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d210b-126">Requirement</span></span> | <span data-ttu-id="d210b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d210b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d210b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d210b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d210b-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d210b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d210b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d210b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d210b-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d210b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d210b-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="d210b-132">Namespace</span></span><br/>                | <span data-ttu-id="d210b-133">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d210b-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d210b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d210b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d210b-135"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d210b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d210b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d210b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d210b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d210b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d210b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d210b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d210b-139">**CIM- \_ portondevice**</span><span class="sxs-lookup"><span data-stu-id="d210b-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="d210b-140">**CIM- \_ portondevice**</span><span class="sxs-lookup"><span data-stu-id="d210b-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="d210b-141">Serielle Geräteklassen</span><span class="sxs-lookup"><span data-stu-id="d210b-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

