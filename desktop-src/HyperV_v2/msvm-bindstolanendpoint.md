---
description: Diese Zuordnung richtet einen Dienst Zugriffspunkt (Service Access Point, SAP) als Anforderer für Protokoll Dienste von einem Protokoll Endpunkt ein.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960574"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="2b653-103">MSVM \_ bindstolanendpoint-Klasse</span><span class="sxs-lookup"><span data-stu-id="2b653-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="2b653-104">Diese Zuordnung richtet einen Dienst Zugriffspunkt (Service Access Point, SAP) als Anforderer für Protokoll Dienste von einem Protokoll Endpunkt ein.</span><span class="sxs-lookup"><span data-stu-id="2b653-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="2b653-105">In der Regel wird diese Zuordnung zwischen SAPs und Endpunkten auf einem einzelnen System ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b653-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="2b653-106">Da es sich bei einem Protokoll Endpunkt um eine Art von SAP handelt, kann diese Bindung verwendet werden, um eine Schicht von zwei Protokollen einzurichten, wobei die obere Ebene durch die **abhängige** und die untere Ebene dargestellt wird, die durch den **Vorgänger** repräsentiert wird.</span><span class="sxs-lookup"><span data-stu-id="2b653-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="2b653-107">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2b653-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b653-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b653-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="2b653-109">Member</span><span class="sxs-lookup"><span data-stu-id="2b653-109">Members</span></span>

<span data-ttu-id="2b653-110">Die **MSVM \_ bindstolanendpoint** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2b653-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="2b653-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b653-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b653-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2b653-112">Properties</span></span>

<span data-ttu-id="2b653-113">Die **MSVM \_ bindstolanendpoint** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2b653-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b653-114">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="2b653-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b653-115">Datentyp: **[ **MSVM \_ lanendpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="2b653-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2b653-116">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b653-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b653-117">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="2b653-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2b653-118">Ein Verweis auf eine [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klasse, die den Switchport darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b653-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="2b653-119">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2b653-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="2b653-120">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="2b653-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b653-121">Datentyp: **[ **MSVM \_ vlanendpoint**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="2b653-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="2b653-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b653-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b653-123">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="2b653-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2b653-124">Ein Verweis auf den [**MSVM- \_ vlanendpoint**](msvm-vlanendpoint.md) , der dem Switchport zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2b653-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="2b653-125">Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)geerbt.</span><span class="sxs-lookup"><span data-stu-id="2b653-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="2b653-126">**FrameType**</span><span class="sxs-lookup"><span data-stu-id="2b653-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b653-127">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b653-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b653-128">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="2b653-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b653-129">Beschreibt die rahmenmethode für den SAP-oder-Endpunkt der oberen Ebene, der an den LAN-Endpunkt gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="2b653-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="2b653-130">Diese Eigenschaft wird von **CIM \_ bindstolanendpoint** geerbt und ist immer auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2b653-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b653-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b653-131">Requirements</span></span>



| <span data-ttu-id="2b653-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b653-132">Requirement</span></span> | <span data-ttu-id="2b653-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2b653-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b653-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b653-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2b653-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b653-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2b653-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b653-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2b653-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b653-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b653-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="2b653-138">Namespace</span></span><br/>                | <span data-ttu-id="2b653-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b653-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2b653-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2b653-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b653-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2b653-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b653-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2b653-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b653-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b653-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

