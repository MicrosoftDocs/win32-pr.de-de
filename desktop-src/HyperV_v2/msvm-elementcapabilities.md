---
description: Stellt die Zuordnung zwischen verwalteten Elementen und ihren Funktionen dar.
ms.assetid: F083E6D2-CC74-4DAD-8FF7-3FE3CA4EEFFF
title: Msvm_ElementCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementCapabilities
- Msvm_ElementCapabilities.ManagedElement
- Msvm_ElementCapabilities.Capabilities
- Msvm_ElementCapabilities.Characteristics
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d7602de569a51aec73130a4b5f4d3ba339cb29c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348111"
---
# <a name="msvm_elementcapabilities-class"></a><span data-ttu-id="bd0e9-103">MSVM \_ elementfunktionalitäten-Klasse</span><span class="sxs-lookup"><span data-stu-id="bd0e9-103">Msvm\_ElementCapabilities class</span></span>

<span data-ttu-id="bd0e9-104">Stellt die Zuordnung zwischen verwalteten Elementen und ihren Funktionen dar.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-104">Represents the association between managed elements and their capabilities.</span></span>

<span data-ttu-id="bd0e9-105">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd0e9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd0e9-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementCapabilities : CIM_ElementCapabilities
{
  CIM_ManagedElement REF ManagedElement;
  CIM_Capabilities   REF Capabilities;
  uint16                 Characteristics[];
};
```

## <a name="members"></a><span data-ttu-id="bd0e9-107">Member</span><span class="sxs-lookup"><span data-stu-id="bd0e9-107">Members</span></span>

<span data-ttu-id="bd0e9-108">Die **MSVM \_ elementfunktionsklasse** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bd0e9-108">The **Msvm\_ElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="bd0e9-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd0e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd0e9-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bd0e9-110">Properties</span></span>

<span data-ttu-id="bd0e9-111">Die **MSVM \_ elementfunktionalitäten** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-111">The **Msvm\_ElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd0e9-112">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-112">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd0e9-113">Datentyp: **[ **CIM- \_ Funktionen**](/previous-versions//cc136806(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-113">Data type: **[**CIM\_Capabilities**](/previous-versions//cc136806(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="bd0e9-114">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bd0e9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd0e9-115">Qualifizierer: **Schlüssel**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-115">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bd0e9-116">Das dem Element zugeordnete Funktionen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-116">The capabilities object associated with the element.</span></span> <span data-ttu-id="bd0e9-117">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-117">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> <dt>

<span data-ttu-id="bd0e9-118">**Characteristics**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-118">**Characteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd0e9-119">Datentyp: **UInt16** Array</span><span class="sxs-lookup"><span data-stu-id="bd0e9-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bd0e9-120">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bd0e9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd0e9-121">Stellt beschreibende Informationen zu den Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-121">Provides descriptive information about the capabilities.</span></span> <span data-ttu-id="bd0e9-122">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-122">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>



| <span data-ttu-id="bd0e9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bd0e9-123">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="bd0e9-124">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bd0e9-124">Meaning</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="bd0e9-125"><dt>**Standard**</dt> Wert <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd0e9-125"><dt>**Default**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="bd0e9-126">Die zugehörigen Funktionen stellen die Standardfunktionen des verwalteten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-126">The associated capabilities represent the default capabilities of the managed element.</span></span><br/> |
| <span id="Current"></span><span id="current"></span><span id="CURRENT"></span><dl> <span data-ttu-id="bd0e9-127"><dt>**Aktuell**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd0e9-127"><dt>**Current**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="bd0e9-128">Die zugehörigen Funktionen stellen die aktuellen Funktionen des verwalteten Elements dar.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-128">The associated capabilities represent the current capabilities of the managed element.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bd0e9-129">**"Managedelement"**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-129">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd0e9-130">Datentyp: **[ **CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-130">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="bd0e9-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="bd0e9-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd0e9-132">Qualifizierer: **Key**, **Min** (1)</span><span class="sxs-lookup"><span data-stu-id="bd0e9-132">Qualifiers: **Key**, **Min** ( 1 )</span></span>
</dt> </dl>

<span data-ttu-id="bd0e9-133">Das verwaltete Element.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-133">The managed element.</span></span> <span data-ttu-id="bd0e9-134">Diese Eigenschaft wird von [**CIM- \_ Element Funktionen**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)geerbt.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-134">This property is inherited from [**CIM\_ElementCapabilities**](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd0e9-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd0e9-135">Remarks</span></span>

<span data-ttu-id="bd0e9-136">Der Zugriff auf die **MSVM \_ elementfunktionalitäten** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="bd0e9-136">Access to the **Msvm\_ElementCapabilities** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bd0e9-137">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bd0e9-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0e9-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd0e9-138">Requirements</span></span>



| <span data-ttu-id="bd0e9-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd0e9-139">Requirement</span></span> | <span data-ttu-id="bd0e9-140">Wert</span><span class="sxs-lookup"><span data-stu-id="bd0e9-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0e9-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd0e9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0e9-142">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0e9-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd0e9-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd0e9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0e9-144">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd0e9-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd0e9-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="bd0e9-145">Namespace</span></span><br/>                | <span data-ttu-id="bd0e9-146">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bd0e9-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bd0e9-147">MOF</span><span class="sxs-lookup"><span data-stu-id="bd0e9-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd0e9-148"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bd0e9-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd0e9-149">DLL</span><span class="sxs-lookup"><span data-stu-id="bd0e9-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd0e9-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd0e9-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bd0e9-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd0e9-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0e9-152">**CIM- \_ Element Funktionen**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-152">**CIM\_ElementCapabilities**</span></span>](cim-elementcapabilities.md)
</dt> <dt>

[<span data-ttu-id="bd0e9-153">**CIM- \_ Element Funktionen**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-153">**CIM\_ElementCapabilities**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementcapabilities)
</dt> <dt>

[<span data-ttu-id="bd0e9-154">**MSVM- \_ Element Funktionen (v1)**</span><span class="sxs-lookup"><span data-stu-id="bd0e9-154">**Msvm\_ElementCapabilities (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-elementcapabilities)
</dt> </dl>

 

