---
description: Stellt die Einstellungen des Gast Kommunikations Diensts dar.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Msvm_GuestCommunicationServiceSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5506689f5b266c428a790774c1fb98a1b0413b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129752"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a><span data-ttu-id="aa5f4-103">MSVM \_ guestcommunicationservicesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="aa5f4-103">Msvm\_GuestCommunicationServiceSettingData class</span></span>

<span data-ttu-id="aa5f4-104">Stellt die Einstellungen des Gast Kommunikations Diensts dar.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-104">Represents the settings of the guest communication service.</span></span>

<span data-ttu-id="aa5f4-105">Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5f4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5f4-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a><span data-ttu-id="aa5f4-107">Member</span><span class="sxs-lookup"><span data-stu-id="aa5f4-107">Members</span></span>

<span data-ttu-id="aa5f4-108">Die **MSVM \_ guestcommunicationservicesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="aa5f4-108">The **Msvm\_GuestCommunicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="aa5f4-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa5f4-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa5f4-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa5f4-110">Properties</span></span>

<span data-ttu-id="aa5f4-111">Die **MSVM \_ guestcommunicationservicesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-111">The **Msvm\_GuestCommunicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa5f4-112">**Enabledstatepolicy**</span><span class="sxs-lookup"><span data-stu-id="aa5f4-112">**EnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5f4-113">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa5f4-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa5f4-114">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="aa5f4-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="aa5f4-115">Enabledstatepolicy ist eine ganzzahlige Enumeration, die den aktivierten, deaktivierten oder Standardstatus der **MSVM \_ guestcommunicationservicesettingdata** angibt.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-115">EnabledStatePolicy is an integer enumeration that indicates the enabled, disabled or default state of the **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa5f4-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-116"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="aa5f4-117">Der Kommunikationsdienst ist auf den aktivierten Zustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-117">The communication service is set to the enabled state.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa5f4-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-118"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa5f4-119">Der Kommunikationsdienst wird auf den Status "deaktiviert" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-119">The communication service is set to the disabled state.</span></span>

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span data-ttu-id="aa5f4-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>Verzögert **(8** )</span><span class="sxs-lookup"><span data-stu-id="aa5f4-120"><span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Deferred** (8)</span></span>


</dt> <dd>

<span data-ttu-id="aa5f4-121">Der Status des Kommunikations Dienstanbieter hängt von **defaultenabledstatepolicy** in **MSVM \_ guestcommunicationservicesettingdata** ab.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-121">The communication service state depends on **DefaultEnabledStatePolicy** in **Msvm\_GuestCommunicationServiceSettingData**.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa5f4-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa5f4-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa5f4-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aa5f4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa5f4-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="aa5f4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa5f4-125">Die GUID des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="aa5f4-125">The GUID of the service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa5f4-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5f4-126">Requirements</span></span>



| <span data-ttu-id="aa5f4-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa5f4-127">Requirement</span></span> | <span data-ttu-id="aa5f4-128">Wert</span><span class="sxs-lookup"><span data-stu-id="aa5f4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5f4-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5f4-130">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5f4-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="aa5f4-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa5f4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5f4-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa5f4-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aa5f4-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa5f4-133">Namespace</span></span><br/>                | <span data-ttu-id="aa5f4-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa5f4-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa5f4-135">MOF</span><span class="sxs-lookup"><span data-stu-id="aa5f4-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa5f4-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f4-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa5f4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5f4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5f4-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa5f4-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa5f4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa5f4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5f4-140">**CIM- \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="aa5f4-140">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




