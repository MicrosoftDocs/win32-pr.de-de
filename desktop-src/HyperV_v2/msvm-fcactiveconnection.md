---
description: Verbindet einen Switchport mit dem Fibre Channel-Endpunkt, mit dem der Port verbunden ist.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345145"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="6d549-103">MSVM- \_ Klasse "ficactiveconnection"</span><span class="sxs-lookup"><span data-stu-id="6d549-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="6d549-104">Verbindet einen Switchport mit dem Fibre Channel-Endpunkt, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6d549-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="6d549-105">Das vorhanden sein dieses Objekts bedeutet, dass der Switchport und der Fibre Channel Endpunkt aktiv verbunden sind und dass der Fibre Channel Port, der dem Fibre Channel Endpunkt zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="6d549-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="6d549-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6d549-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d549-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d549-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="6d549-108">Member</span><span class="sxs-lookup"><span data-stu-id="6d549-108">Members</span></span>

<span data-ttu-id="6d549-109">Die **MSVM \_ fcactiveconnection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="6d549-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="6d549-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d549-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6d549-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d549-111">Properties</span></span>

<span data-ttu-id="6d549-112">Die **MSVM-Klasse " \_ ficactiveconnection** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6d549-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d549-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="6d549-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d549-114">Datentyp: **MSVM \_ fcendpoint**</span><span class="sxs-lookup"><span data-stu-id="6d549-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="6d549-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d549-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d549-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="6d549-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6d549-117">Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den Dienst Zugriffspunkt (SAP) darstellt, der für die Kommunikation oder aktive Kommunikation mit dem abhängigen SAP konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6d549-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="6d549-118">Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um das, das übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="6d549-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="6d549-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="6d549-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d549-120">Datentyp: **MSVM \_ fcendpoint**</span><span class="sxs-lookup"><span data-stu-id="6d549-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="6d549-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d549-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d549-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="6d549-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6d549-123">Ein Verweis auf eine Instanz der [**MSVM \_ fcendpoint**](msvm-fcendpoint.md) -Klasse, die den SAP darstellt, der für die Kommunikation oder aktive Kommunikation mit dem Vorgänger-SAP konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6d549-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="6d549-124">Bei einer unidirektionalen Verbindung ist dieser SAP der empfangende SAP.</span><span class="sxs-lookup"><span data-stu-id="6d549-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="6d549-125">**Isunidirektional**</span><span class="sxs-lookup"><span data-stu-id="6d549-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d549-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="6d549-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6d549-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d549-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d549-128">Wenn diese Eigenschaft den Wert **true** hat, ist diese Verbindung unidirektional. Andernfalls ist diese Verbindung bidirektional.</span><span class="sxs-lookup"><span data-stu-id="6d549-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="6d549-129">Wenn eine Verbindung unidirektional ist, sollte der "Sprecher" als **vorangehende** Verweis definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6d549-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="6d549-130">Bei einer bidirektionalen Verbindung spielt es keine Rolle, ob der ausgewählte Zugriffspunkt der **Vorgänger** oder der **abhängige** ist.</span><span class="sxs-lookup"><span data-stu-id="6d549-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="6d549-131">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="6d549-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6d549-132">**Othertrafficdescription**</span><span class="sxs-lookup"><span data-stu-id="6d549-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d549-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6d549-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d549-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d549-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d549-135">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d549-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6d549-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="6d549-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d549-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6d549-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6d549-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="6d549-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d549-139">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d549-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d549-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d549-140">Requirements</span></span>



| <span data-ttu-id="6d549-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d549-141">Requirement</span></span> | <span data-ttu-id="6d549-142">Wert</span><span class="sxs-lookup"><span data-stu-id="6d549-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d549-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6d549-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6d549-144">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d549-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6d549-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6d549-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6d549-146">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6d549-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d549-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d549-147">Namespace</span></span><br/>                | <span data-ttu-id="6d549-148">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6d549-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6d549-149">MOF</span><span class="sxs-lookup"><span data-stu-id="6d549-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d549-150"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6d549-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d549-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6d549-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d549-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6d549-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

