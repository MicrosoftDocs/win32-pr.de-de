---
description: Stellt die Zuordnung zwischen Ethernet-Erweiterungen und ihren Funktionen dar.
ms.assetid: 6b32235a-175d-48f9-af3a-2d40f748a518
title: Msvm_EthernetSwitchExtensionCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchExtensionCapabilities
- Msvm_EthernetSwitchExtensionCapabilities.ManagedElement
- Msvm_EthernetSwitchExtensionCapabilities.Capabilities
- Msvm_EthernetSwitchExtensionCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 950a8a0288487bf557e9dd201100b2a894417641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760855"
---
# <a name="msvm_ethernetswitchextensioncapabilities-class"></a><span data-ttu-id="34f3c-103">MSVM \_ ethernetzwitchextensionfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="34f3c-103">Msvm\_EthernetSwitchExtensionCapabilities class</span></span>

<span data-ttu-id="34f3c-104">Stellt die Zuordnung zwischen Ethernet-Erweiterungen und ihren Funktionen dar.</span><span class="sxs-lookup"><span data-stu-id="34f3c-104">Represents the association between Ethernet extensions and their capabilities.</span></span>

<span data-ttu-id="34f3c-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34f3c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f3c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="34f3c-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchExtensionCapabilities : CIM_ElementCapabilities
{
  Msvm_InstalledEthernetSwitchExtension  REF ManagedElement;
  Msvm_EthernetSwitchFeatureCapabilities REF Capabilities;
  uint16                                     Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="34f3c-107">Member</span><span class="sxs-lookup"><span data-stu-id="34f3c-107">Members</span></span>

<span data-ttu-id="34f3c-108">Die **MSVM \_ ethernetzwitchextensionfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="34f3c-108">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="34f3c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34f3c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34f3c-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="34f3c-110">Properties</span></span>

<span data-ttu-id="34f3c-111">Die **MSVM-Klasse " \_ ethernetzwitchextensionfunktionalitäten** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34f3c-111">The **Msvm\_EthernetSwitchExtensionCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34f3c-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="34f3c-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34f3c-113">Datentyp: **[ **MSVM \_ ethernetungwitchfeatuerabilitäten**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="34f3c-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="34f3c-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34f3c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34f3c-115">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Funktionen")</span><span class="sxs-lookup"><span data-stu-id="34f3c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="34f3c-116">Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchfeaturecapabili"**](msvm-ethernetswitchfeaturecapabilities.md) , die das dem Switch zugeordnete Objekt "Funktionen" darstellt.</span><span class="sxs-lookup"><span data-stu-id="34f3c-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the capabilities object associated with the switch.</span></span> <span data-ttu-id="34f3c-117">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34f3c-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="34f3c-118">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="34f3c-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34f3c-119">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="34f3c-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="34f3c-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34f3c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34f3c-121">Stellt beschreibende Informationen zu den Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="34f3c-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="34f3c-122">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34f3c-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="34f3c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="34f3c-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="34f3c-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="34f3c-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="34f3c-125"><dt>**Standard**</dt> Wert <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="34f3c-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="34f3c-126">Die zugehörigen Funktionen stellen die Standardfunktionen des verwalteten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="34f3c-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="34f3c-127"><dt>**Aktuell**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="34f3c-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="34f3c-128">Die zugehörigen Funktionen stellen die aktuellen Funktionen des verwalteten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="34f3c-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34f3c-129">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="34f3c-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34f3c-130">Datentyp: **[ **MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md)**</span><span class="sxs-lookup"><span data-stu-id="34f3c-130">Data type: **[**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md)**</span></span>
</dt> <dt>

<span data-ttu-id="34f3c-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="34f3c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="34f3c-132">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("managedelta")</span><span class="sxs-lookup"><span data-stu-id="34f3c-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ManagedElement")</span></span>
</dt> </dl>

<span data-ttu-id="34f3c-133">Ein Verweis auf eine Instanz der [**MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md) -Klasse, die die installierte Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="34f3c-133">A reference to an instance of the [**Msvm\_InstalledEthernetSwitchExtension**](msvm-installedethernetswitchextension.md) class that represents the installed extension.</span></span> <span data-ttu-id="34f3c-134">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="34f3c-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34f3c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34f3c-135">Requirements</span></span>



| <span data-ttu-id="34f3c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34f3c-136">Requirement</span></span> | <span data-ttu-id="34f3c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="34f3c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34f3c-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34f3c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="34f3c-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f3c-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34f3c-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34f3c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="34f3c-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34f3c-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34f3c-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="34f3c-142">Namespace</span></span><br/>                | <span data-ttu-id="34f3c-143">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="34f3c-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34f3c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="34f3c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34f3c-145"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="34f3c-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34f3c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="34f3c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34f3c-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34f3c-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

