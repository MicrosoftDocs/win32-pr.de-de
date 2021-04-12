---
description: Eine abstrakte Basisklasse für Klassen, die Einstellungen für ein Ethernet-switchportfeature darstellen.
ms.assetid: 26c40dd0-fe1e-4432-a177-8a565bf678e6
title: Msvm_EthernetSwitchPortFeatureSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortFeatureSettingData
- Msvm_EthernetSwitchPortFeatureSettingData.InstanceID
- Msvm_EthernetSwitchPortFeatureSettingData.Caption
- Msvm_EthernetSwitchPortFeatureSettingData.Description
- Msvm_EthernetSwitchPortFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0734fa89d99d80e26e4d5fc841bdac89cfd8dfe6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346059"
---
# <a name="msvm_ethernetswitchportfeaturesettingdata-class"></a><span data-ttu-id="d60bd-103">MSVM \_ ethernetzwitchportfeaturesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="d60bd-103">Msvm\_EthernetSwitchPortFeatureSettingData class</span></span>

<span data-ttu-id="d60bd-104">Eine abstrakte Basisklasse für Klassen, die Einstellungen für ein Ethernet-switchportfeature darstellen.</span><span class="sxs-lookup"><span data-stu-id="d60bd-104">Abstract base class for classes that represent settings for an Ethernet switch port feature.</span></span>

<span data-ttu-id="d60bd-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d60bd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d60bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d60bd-106">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPortFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="d60bd-107">Member</span><span class="sxs-lookup"><span data-stu-id="d60bd-107">Members</span></span>

<span data-ttu-id="d60bd-108">Die **MSVM \_ ethernetzwitchportfeaturesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d60bd-108">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d60bd-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d60bd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d60bd-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d60bd-110">Properties</span></span>

<span data-ttu-id="d60bd-111">Die **MSVM \_ ethernetzwitchportfeaturesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d60bd-111">The **Msvm\_EthernetSwitchPortFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d60bd-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d60bd-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d60bd-113">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d60bd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d60bd-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d60bd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d60bd-115">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d60bd-115">A short description of the object.</span></span> <span data-ttu-id="d60bd-116">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d60bd-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d60bd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d60bd-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d60bd-118">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d60bd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d60bd-119">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d60bd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d60bd-120">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="d60bd-120">A description of the object.</span></span> <span data-ttu-id="d60bd-121">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d60bd-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d60bd-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d60bd-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d60bd-123">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d60bd-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d60bd-124">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d60bd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d60bd-125">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d60bd-125">A display name for the object.</span></span> <span data-ttu-id="d60bd-126">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="d60bd-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d60bd-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d60bd-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d60bd-128">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d60bd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d60bd-129">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="d60bd-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d60bd-130">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="d60bd-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d60bd-131">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d60bd-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d60bd-132">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="d60bd-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d60bd-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d60bd-133">Requirements</span></span>



| <span data-ttu-id="d60bd-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d60bd-134">Requirement</span></span> | <span data-ttu-id="d60bd-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d60bd-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d60bd-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d60bd-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d60bd-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d60bd-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d60bd-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d60bd-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d60bd-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d60bd-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d60bd-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d60bd-140">Namespace</span></span><br/>                | <span data-ttu-id="d60bd-141">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d60bd-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d60bd-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d60bd-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d60bd-143"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d60bd-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d60bd-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d60bd-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d60bd-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d60bd-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

