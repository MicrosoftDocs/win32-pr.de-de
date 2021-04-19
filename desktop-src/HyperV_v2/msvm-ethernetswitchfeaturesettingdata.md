---
description: Eine abstrakte Klasse, die Einstellungen für eine bestimmte Instanz eines Ethernet-Switchfeatures darstellt.
ms.assetid: c1720649-585f-45a9-8329-06787bd8b600
title: Msvm_EthernetSwitchFeatureSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchFeatureSettingData
- Msvm_EthernetSwitchFeatureSettingData.InstanceID
- Msvm_EthernetSwitchFeatureSettingData.Caption
- Msvm_EthernetSwitchFeatureSettingData.Description
- Msvm_EthernetSwitchFeatureSettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a71d9b4a78ffedb6ffc0a0c1e01562ce7638ef65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366523"
---
# <a name="msvm_ethernetswitchfeaturesettingdata-class"></a><span data-ttu-id="2661c-103">MSVM \_ ethernetzwitchfeaturesettingdata-Klasse</span><span class="sxs-lookup"><span data-stu-id="2661c-103">Msvm\_EthernetSwitchFeatureSettingData class</span></span>

<span data-ttu-id="2661c-104">Eine abstrakte Klasse, die Einstellungen für eine bestimmte Instanz eines Ethernet-Switchfeatures darstellt.</span><span class="sxs-lookup"><span data-stu-id="2661c-104">An abstract class that represents settings for a given instance of an Ethernet switch feature.</span></span> <span data-ttu-id="2661c-105">Die Verwaltungs Klasse der Ethernet-Switchfeatures muss von dieser abstrakten Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="2661c-105">Ethernet Switch Features settings management class must derive from this abstract class.</span></span>

<span data-ttu-id="2661c-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2661c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2661c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2661c-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchFeatureSettingData : Msvm_FeatureSettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="2661c-108">Member</span><span class="sxs-lookup"><span data-stu-id="2661c-108">Members</span></span>

<span data-ttu-id="2661c-109">Die **MSVM \_ ethernetzwitchfeaturesettingdata** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2661c-109">The **Msvm\_EthernetSwitchFeatureSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="2661c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2661c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2661c-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2661c-111">Properties</span></span>

<span data-ttu-id="2661c-112">Die **MSVM \_ ethernetzwitchfeaturesettingdata** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2661c-112">The **Msvm\_EthernetSwitchFeatureSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2661c-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2661c-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2661c-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2661c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2661c-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2661c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2661c-116">Eine kurze Beschreibung des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="2661c-116">A short description of the object.</span></span> <span data-ttu-id="2661c-117">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2661c-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2661c-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2661c-118">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2661c-119">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2661c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2661c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2661c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2661c-121">Eine Beschreibung des -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2661c-121">A description of the object.</span></span> <span data-ttu-id="2661c-122">Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2661c-122">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2661c-123">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2661c-123">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2661c-124">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2661c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2661c-125">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2661c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2661c-126">Ein Anzeige Name für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2661c-126">A display name for the object.</span></span> <span data-ttu-id="2661c-127">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2661c-127">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2661c-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2661c-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2661c-129">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2661c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2661c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2661c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2661c-131">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="2661c-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2661c-132">Identifiziert eine Instanz dieser Klasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="2661c-132">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2661c-133">Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="2661c-133">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2661c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2661c-134">Requirements</span></span>



| <span data-ttu-id="2661c-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2661c-135">Requirement</span></span> | <span data-ttu-id="2661c-136">Wert</span><span class="sxs-lookup"><span data-stu-id="2661c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2661c-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2661c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2661c-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2661c-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2661c-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2661c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2661c-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2661c-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2661c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="2661c-141">Namespace</span></span><br/>                | <span data-ttu-id="2661c-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2661c-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2661c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2661c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2661c-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2661c-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2661c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2661c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2661c-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2661c-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

