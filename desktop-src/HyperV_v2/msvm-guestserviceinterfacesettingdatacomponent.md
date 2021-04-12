---
description: Association-Klasse zwischen einer Gast Dienst-Schnittstellen Komponente und der Gast Dienst Ressource.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Msvm_GuestServiceInterfaceSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 988975fea1fd519a5e3917faeb73d345334d74b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214764"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a><span data-ttu-id="9d58f-103">MSVM \_ guestserviceinterfacesettingdatacomponent-Klasse</span><span class="sxs-lookup"><span data-stu-id="9d58f-103">Msvm\_GuestServiceInterfaceSettingDataComponent class</span></span>

<span data-ttu-id="9d58f-104">Association-Klasse zwischen einer Gast Dienst-Schnittstellen Komponente und der Gast Dienst Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d58f-104">Association class between a guest service interface component and the guest service resource.</span></span>

<span data-ttu-id="9d58f-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d58f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d58f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d58f-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9d58f-107">Member</span><span class="sxs-lookup"><span data-stu-id="9d58f-107">Members</span></span>

<span data-ttu-id="9d58f-108">Die **MSVM \_ guestserviceinterfacesettingdatacomponent** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9d58f-108">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9d58f-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d58f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d58f-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9d58f-110">Properties</span></span>

<span data-ttu-id="9d58f-111">Die **MSVM \_ guestserviceinterfacesettingdatacomponent** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d58f-111">The **Msvm\_GuestServiceInterfaceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d58f-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9d58f-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-113">Datentyp: **MSVM \_ guestserviceinterfacekompononentsettingdata**</span><span class="sxs-lookup"><span data-stu-id="9d58f-113">Data type: **Msvm\_GuestServiceInterfaceComponentSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d58f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-115">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="9d58f-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-116">Ein [**MSVM \_ guestserviceinterfacecomponentsettingdata**](msvm-guestserviceinterfacecomponentsettingdata.md) -Element, das auf die Komponente der Gast Dienst Schnittstelle verweist.</span><span class="sxs-lookup"><span data-stu-id="9d58f-116">A [**Msvm\_GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md) referencing the guest service interface component.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9d58f-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-118">Datentyp: **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="9d58f-118">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9d58f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-120">Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9d58f-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-121">[**CIM \_ SettingData**](cim-settingdata.md) , die auf die Gast Dienst Ressource verweist.</span><span class="sxs-lookup"><span data-stu-id="9d58f-121">A [**CIM\_SettingData**](cim-settingdata.md) that references the guest service resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d58f-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d58f-122">Requirements</span></span>



| <span data-ttu-id="9d58f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d58f-123">Requirement</span></span> | <span data-ttu-id="9d58f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9d58f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d58f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d58f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d58f-126">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d58f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9d58f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d58f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d58f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9d58f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9d58f-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d58f-129">Namespace</span></span><br/>                | <span data-ttu-id="9d58f-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="9d58f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9d58f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9d58f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d58f-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d58f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9d58f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d58f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9d58f-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d58f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d58f-136">**CIM- \_ Komponente**</span><span class="sxs-lookup"><span data-stu-id="9d58f-136">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

