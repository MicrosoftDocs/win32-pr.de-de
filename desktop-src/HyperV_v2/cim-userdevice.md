---
description: Stellt ein logisches Gerät dar, das es einem Benutzer ermöglicht, Daten auf dem Computersystem einzugeben, anzuzeigen oder zu hören.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: CIM_UserDevice-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864111"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="5edcf-103">CIM_UserDevice-Klasse (Hyper-V-Verwaltung)</span><span class="sxs-lookup"><span data-stu-id="5edcf-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="5edcf-104">Stellt ein logisches Gerät dar, das es einem Benutzer ermöglicht, Daten auf dem Computersystem einzugeben, anzuzeigen oder zu hören.</span><span class="sxs-lookup"><span data-stu-id="5edcf-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5edcf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5edcf-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="5edcf-106">Member</span><span class="sxs-lookup"><span data-stu-id="5edcf-106">Members</span></span>

<span data-ttu-id="5edcf-107">Die **CIM \_ userdevice** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5edcf-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="5edcf-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5edcf-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5edcf-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5edcf-109">Properties</span></span>

<span data-ttu-id="5edcf-110">Die **CIM \_ userdevice** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5edcf-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5edcf-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="5edcf-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5edcf-112">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="5edcf-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5edcf-113">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="5edcf-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5edcf-114">**true** , wenn das Gerät gesperrt ist und Benutzereingaben oder-Ausgaben verhindert. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="5edcf-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5edcf-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5edcf-115">Requirements</span></span>



| <span data-ttu-id="5edcf-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5edcf-116">Requirement</span></span> | <span data-ttu-id="5edcf-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5edcf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5edcf-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5edcf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5edcf-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5edcf-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5edcf-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5edcf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5edcf-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5edcf-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5edcf-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="5edcf-122">Namespace</span></span><br/>                | <span data-ttu-id="5edcf-123">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5edcf-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5edcf-124">MOF</span><span class="sxs-lookup"><span data-stu-id="5edcf-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5edcf-125"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5edcf-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5edcf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5edcf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5edcf-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5edcf-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5edcf-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5edcf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5edcf-129">**CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="5edcf-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




