---
description: Verbindet einen Switchport mit dem LAN-Endpunkt, mit dem der Port verbunden ist.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867307"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="3df32-103">MSVM \_ ActiveConnection-Klasse</span><span class="sxs-lookup"><span data-stu-id="3df32-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="3df32-104">Verbindet einen Switchport mit dem LAN-Endpunkt, mit dem der Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="3df32-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="3df32-105">Das vorhanden sein dieses Objekts bedeutet, dass der Switchport und der LAN-Endpunkt aktiv verbunden sind und der Ethernet-Port, der dem LAN-Endpunkt zugeordnet ist, über den Switchport mit dem Netzwerk kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="3df32-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="3df32-106">Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3df32-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3df32-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3df32-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="3df32-108">Member</span><span class="sxs-lookup"><span data-stu-id="3df32-108">Members</span></span>

<span data-ttu-id="3df32-109">Die **MSVM \_ ActiveConnection** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3df32-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="3df32-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3df32-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3df32-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3df32-111">Properties</span></span>

<span data-ttu-id="3df32-112">Die **MSVM \_ ActiveConnection** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3df32-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3df32-113">**Vorgänger**</span><span class="sxs-lookup"><span data-stu-id="3df32-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df32-114">Datentyp: **[ **MSVM \_ lanendpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3df32-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3df32-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3df32-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df32-116">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")</span><span class="sxs-lookup"><span data-stu-id="3df32-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3df32-117">Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](msvm-lanendpoint.md) -Klasse, die den Dienst Zugriffspunkt (SAP) darstellt, der für die Kommunikation oder aktive Kommunikation mit dem abhängigen SAP konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3df32-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="3df32-118">Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um das, das übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="3df32-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="3df32-119">**Dependent**</span><span class="sxs-lookup"><span data-stu-id="3df32-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df32-120">Datentyp: **[ **CIM \_ lanendpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="3df32-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3df32-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3df32-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3df32-122">Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")</span><span class="sxs-lookup"><span data-stu-id="3df32-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3df32-123">Ein Verweis auf eine Instanz der [**MSVM \_ lanendpoint**](cim-lanendpoint.md) -Klasse, die den SAP darstellt, der für die Kommunikation konfiguriert ist oder aktiv mit dem Vorgänger-SAP kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="3df32-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="3df32-124">Bei einer unidirektionalen Verbindung handelt es sich bei diesem SAP um den, der empfängt.</span><span class="sxs-lookup"><span data-stu-id="3df32-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="3df32-125">**Isunidirektional**</span><span class="sxs-lookup"><span data-stu-id="3df32-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df32-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="3df32-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3df32-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3df32-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df32-128">Wenn diese Eigenschaft den Wert **true** hat, ist diese Verbindung unidirektional. Andernfalls ist diese Verbindung bidirektional.</span><span class="sxs-lookup"><span data-stu-id="3df32-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="3df32-129">Wenn eine Verbindung unidirektional ist, sollte der "Sprecher" als **vorangehende** Verweis definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3df32-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="3df32-130">Bei einer bidirektionalen Verbindung spielt es keine Rolle, ob der ausgewählte Zugriffspunkt der **Vorgänger** oder der **abhängige** ist.</span><span class="sxs-lookup"><span data-stu-id="3df32-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="3df32-131">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt.</span><span class="sxs-lookup"><span data-stu-id="3df32-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3df32-132">**Othertrafficdescription**</span><span class="sxs-lookup"><span data-stu-id="3df32-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df32-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3df32-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3df32-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3df32-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df32-135">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3df32-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3df32-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="3df32-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3df32-137">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3df32-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3df32-138">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3df32-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3df32-139">Diese Eigenschaft wird von [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))geerbt, aber nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3df32-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3df32-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3df32-140">Remarks</span></span>

<span data-ttu-id="3df32-141">Der Zugriff auf die **MSVM \_ ActiveConnection** -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="3df32-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="3df32-142">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="3df32-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="3df32-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3df32-143">Examples</span></span>

<span data-ttu-id="3df32-144">Weitere Informationen finden Sie unter [Abfragen von Netzwerk Objekten](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3df32-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3df32-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3df32-145">Requirements</span></span>



| <span data-ttu-id="3df32-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3df32-146">Requirement</span></span> | <span data-ttu-id="3df32-147">Wert</span><span class="sxs-lookup"><span data-stu-id="3df32-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3df32-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3df32-148">Minimum supported client</span></span><br/> | <span data-ttu-id="3df32-149">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3df32-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3df32-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3df32-150">Minimum supported server</span></span><br/> | <span data-ttu-id="3df32-151">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3df32-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3df32-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="3df32-152">Namespace</span></span><br/>                | <span data-ttu-id="3df32-153">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="3df32-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3df32-154">MOF</span><span class="sxs-lookup"><span data-stu-id="3df32-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3df32-155"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3df32-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3df32-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3df32-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3df32-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3df32-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3df32-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3df32-159">**CIM \_ ActiveConnection**</span><span class="sxs-lookup"><span data-stu-id="3df32-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="3df32-160">[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3df32-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

